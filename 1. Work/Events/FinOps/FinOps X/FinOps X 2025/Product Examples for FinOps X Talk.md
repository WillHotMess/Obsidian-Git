
---
# Configure optimization settings

Define the optimization policy for requests and limits at the cluster, namespace, or workload level

Policy-based optimization ensures consistency across workloads and gives teams the control they need over their work - for example:

- Platform teams can set organization-wide default optimization values
- Development teams can fine-tune settings using annotations on namespaces, Deployments, StatefulSets, and other workload resources

This topic explains how to configure optimization settings at the cluster, namespace, or workload levels using annotation syntax.

For a list and description of what you can configure, see the [Optimization settings and descriptions](https://docs.stormforge.io/optimize-live/configure/settings/) topic.

#### Key points:[](https://docs.stormforge.io/optimize-live/configure/#key-points)

- Think of settings at the **cluster**, **namespace**, and **workload** levels as a hierarchy of configuration.
    - **Cluster-level defaults** apply to all workloads in a cluster. The cluster administrator defines cluster-wide defaults that are used when a more specific policy is not defined. Default values set at this level have the **lowest precedence and can be overridden** by values set at the namespace and workload levels.
        
    - **Namespace-level configuration** sets default values for all workloads in a namespace, overriding existing cluster defaults. Namespace owners can adjust these policies, or define their own, by using annotations on the namespace.
        
    - **Workload-level configuration** customizes the optimization behavior for individual workloads. Workload owners can further adjust or make exceptions to optimization policies, by using annotations on the actual workload objects (Deployments, StatefulSets, and others).
        

##### Quickstart: Copy a template[](https://docs.stormforge.io/optimize-live/configure/#quickstart-templates)

- Choose a template
- Cluster
- Namespace
- Workload

Each tab contains a template that contains the annotations for each optimization setting.

- Copy the **Cluster** template to set cluster-level defaults
- Copy the **Namespace** template to set namespace-level defaults
- Copy the **Workload** template to set workload-specific defaults defaults

**When editing annotations:**

- Enclose all values in double quotation marks (`"..."`).
- **Best practice:** When editing _container-specific_ resources, specify the value to apply to _all or most containers_ first, followed by container-specific exceptions, as in these examples:
    - When annotating a workload or namespace:  
        `live.stormforge.io/containers.cpu.optimization-policy: "RequestsAndLimits,logwriter=DoNotOptimize"`

---
# Getting started with configuring Optimize Live

Learn about the 5 most important optimization settings

  6 minute read  

## Getting started[](https://docs.stormforge.io/optimize-live/configure/configure-opt-settings/#getting-started)

Optimize Live performs best when it is properly configured with goals, constraints, and requirements appropriate for the workloads it is optimizing. One of the first steps you should take when deploying Optimize Live is to **review the available configuration options, and adjust settings as needed to suit your organization’s requirements.**

Optimization settings can be applied as cluster-scoped defaults, namespace-scoped defaults, or directly to individual workloads. Making sure your cluster-scoped default values are aligned with your organization’s requirements first provides the most return for your effort. You can carve out exceptions to these settings for particular namespaces or workloads later.

Sometimes the simplest way to identify adjustments that should be made is to just start applying recommendations, then examine the results and make configuration adjustments until any undesirable behavior has been resolved. This guide, however, aims to minimize the time spent in that process by giving you **guidance on how to craft an informed initial optimization configuration suited to your organization’s goals, and tailored for workload types relevant to you.**

### The 5 most important optimization settings[](https://docs.stormforge.io/optimize-live/configure/configure-opt-settings/#the-5-most-important-optimization-settings)

Some optimization settings are more important than others. These are the top five options to learn about and consider setting cluster default values for when you’re first getting started with StormForge.

- [Optimization goal](https://docs.stormforge.io/optimize-live/configure/configure-opt-settings/#optimization-goal)
- [Recommendation schedule](https://docs.stormforge.io/optimize-live/configure/configure-opt-settings/#rec-schedule)
- [Minimum and maximum bounds](https://docs.stormforge.io/optimize-live/configure/configure-opt-settings/#min-max-bounds)
- [Limit handling](https://docs.stormforge.io/optimize-live/configure/configure-opt-settings/#limit-handling)
- [Auto-deploy](https://docs.stormforge.io/optimize-live/configure/configure-opt-settings/#auto-deploy)

How each of these options are set can have a big impact on Optimize Live’s behavior.

#### Optimization goal[](https://docs.stormforge.io/optimize-live/configure/configure-opt-settings/#optimization-goal)

Optimize Live’s goal setting, **which you can configure separately for CPU and memory**, is a hint to the recommendation engine about how you would like it to balance the competing objectives of reliability and cost savings when generating resource request recommendations.

The default goal is `Balanced`, which is a middle ground between `Savings` and `Reliability`. Optimize Live always strives to ensure workloads have sufficient resource allocation for their observed actual usage. The `Reliability` goal puts more weight on the maximum observed usage when forecasting and recommending requests, while the `Savings` goal results in recommendations more tolerant of possible occasional bursting.

It’s a common practice to select the `Savings` optimization goal for non-prod environments, the `Balanced` goal for production, and the `Reliability` goal for specifically identified mission-critical namespaces and workloads.

#### Recommendation schedule[](https://docs.stormforge.io/optimize-live/configure/configure-opt-settings/#rec-schedule)

The `schedule` setting dictates how frequently Optimize Live evaluates workloads and updates their resource recommendations.

Optimize Live uses machine learning to forecast resource usage and create request recommendations that satisfy predicted resource usage for the upcoming _schedule period_ – the length of time between a recommendation being generated and the time the following recommendation is scheduled.

Pick a schedule that reflects how often you want to, or are willing to, automatically update resource requests for your workloads. A `@daily` or `@weekly` schedule produces good results for most organizations while incurring minimal resizing overhead. Resizing overhead can be further reduced by configuring [auto-deploy thresholds](https://docs.stormforge.io/optimize-live/configure/settings/auto-deploy/#thresholds).

#### Minimum and Maximum Bounds[](https://docs.stormforge.io/optimize-live/configure/configure-opt-settings/#min-max-bounds)

By default, Optimize Live is not configured with any minimum or maximum bounds. Unless your organization prefers to set minimum or maximum bounds, recommendations are made based only on the usage observed for each workload, for each resource.

Sizing bounds let you define the upper and lower values for CPU and memory that are always be allocated to even the smallest, nearly-idle workload, and ceiling values above which CPU and memory requests are never raised (at least not automatically).

Choosing a minimum bound ensures that you never receive recommendations with values lower than you’re comfortable with. Be aware that setting minimums which are too high may hinder Optimize Live’s ability to reduce waste.

As a general starting point, we suggest trying out the following minimum bound values.

- Minimum CPU request: `10m`
- Minimum memory request: `64Mi`

It’s not critical to set maximums, but if you prefer to, we suggest setting them based on the largest node or workload size permitted in your organization. For example:

- Maximum CPU request: `15000m` (or `15`), if the largest node type in the cluster has 16 cores
- Maximum memory request: `54Gi`, if the largest node type in the cluster has 64Gi of memory

#### Limit Handling[](https://docs.stormforge.io/optimize-live/configure/configure-opt-settings/#limit-handling)

Different organizations have different policies about how to (or not) configure limits. As such, Optimize Live can be configured to match whichever limits practices your organization adheres to.

Optimize Live offers several different options, called Optimization Policies, for what to do with limits when it makes adjustments to request settings:

- `RequestsRaiseLimitsIfNeeded` (default): This policy uses an adaptive behavior that works well for most organizations. Optimize Live adjusts its behavior based on how limits are configured on the workload already.
    
    - If no limits are set, Optimize Live won’t set them.
    - If limits are set but they are high enough already, Optimize Live will leave them at their existing values.
    - If limits are set but Optimize Live wants to increase requests, it will raise the limit if needed to accommodate the higher requests.
    
    Notably, Optimize Live will never lower limits when using this option.
    
    This policy and the following alternative options are described in more detail in the [Optimization policy](https://docs.stormforge.io/optimize-live/configure/settings/containers/#opt-policy) section of the Containers topic.
    
- `RequestsAndLimits`: Always set limits, according to limits configuration.
    
- `RequestsOnly`: Never set or change limits.
    
- `DoNotOptimize`: Indicates to Optimize Live to leave a particular resource completely alone.
    

#### Auto-deploy[](https://docs.stormforge.io/optimize-live/configure/configure-opt-settings/#auto-deploy)

Whether or not to automatically deploy recommendations, or apply recommended settings, is the lynchpin of realizing Optimize Live’s value.

When you first roll out Optimize Live, auto-deploy is `Disabled` on all workloads. As you validate that the recommended settings look good, you can manually apply recommendations on canary workloads, then start enabling auto-deploy for workloads or namespaces one at a time until you’ve built up confidence in the tool. If you would like, you could alternatively set `auto-deploy` to `Enabled` as a cluster default, and opt out individual namespaces or workloads instead of opting them in.

The rollout strategy for enabling the auto-deploy setting in particular is likely to be organization dependent. For now, the important thing to know is that this is effectively the “on” switch for Optimize Live’s automated management mode. Be thoughtful in deciding when and where to turn it on first.

## Cluster defaults template[](https://docs.stormforge.io/optimize-live/configure/configure-opt-settings/#cluster-defaults-template)

To get started with configuring your own cluster defaults, you can copy the following cluster-defaults ConfigMap template, which defines these foundational configuration settings. This template has been populated with all of the values suggested in this guide, and is ready for you to copy, make any adjustments you need, and apply to your cluster.

```yaml
apiVersion: v1
kind: ConfigMap
metadata:
  name: cluster-defaults
  namespace: stormforge-system
data:
  cluster-defaults.yaml: |

    # WORKLOAD SETTINGS
    live.stormforge.io/schedule: "@daily"
    live.stormforge.io/auto-deploy: "Disabled" # Set to "Enabled" to enable auto-deploy

    # CONTAINER SETTINGS
    live.stormforge.io/containers.cpu.optimization-policy: "RequestsRaiseLimitsIfNeeded"
    live.stormforge.io/containers.memory.optimization-policy: "RequestsRaiseLimitsIfNeeded"

    live.stormforge.io/containers.cpu.requests.min: "10m"
    live.stormforge.io/containers.memory.requests.min: "64Mi"
    #live.stormforge.io/containers.cpu.requests.max: "15000m"
    #live.stormforge.io/containers.memory.requests.max: "54Gi"

    # Limit bounds only apply if Optimize Live is going to change the limits.
    live.stormforge.io/containers.cpu.limits.min: "2000m"
    live.stormforge.io/containers.memory.limits.min: "384Mi"
    live.stormforge.io/containers.cpu.limits.max: "16000m"
    live.stormforge.io/containers.memory.limits.max: "60Gi"
```

Copy

For more information about applying cluster-default configuration, see the [Configure clusters](https://docs.stormforge.io/optimize-live/configure/cluster-defaults/) topic.

## Container-specific settings[](https://docs.stormforge.io/optimize-live/configure/configure-opt-settings/#container-specific-settings)

In this guide so far, we’ve talked about default settings very generally. As you begin to refine your configuration, note that appropriate settings can vary container-to-container inside a Pod.

Optimize Live’s configuration permits you to adjust many optimization settings on a container-by-container basis. See the topics under [Configure optimization](https://docs.stormforge.io/optimize-live/configure/) for more details.

Last modified January 23, 2025

--- 
# Configure optimization defaults for the cluster

Configure default optimization settings for the cluster

The purpose of this topic is to describe how to use the `cluster-defaults` ConfigMap to configure default optimization settings for a cluster.

#### Topics:[](https://docs.stormforge.io/optimize-live/configure/cluster-defaults/#topics)

- [Configure default optimization settings for all workloads in the cluster](https://docs.stormforge.io/optimize-live/configure/cluster-defaults/#configure-defaults)
    - [Using `kubectl apply`](https://docs.stormforge.io/optimize-live/configure/cluster-defaults/#defaults-using-kubectl-apply)
    - [Using `kubectl edit`](https://docs.stormforge.io/optimize-live/configure/cluster-defaults/#defaults-using-kubectl-edit)

## Configure default optimization settings for all workloads in the cluster[](https://docs.stormforge.io/optimize-live/configure/cluster-defaults/#configure-defaults)

Cluster-level defaults:

- Define the default optimization settings for all workloads in a cluster
- Are specified in a ConfigMap named `cluster-defaults` in the `stormforge-system` namespace
- Have the lowest configuration precedence and can be overridden by namespace annotations or by annotations on individual workload resources

### Setting cluster default values using `kubectl apply`[](https://docs.stormforge.io/optimize-live/configure/cluster-defaults/#defaults-using-kubectl-apply)

1. Create a YAML file that defines a ConfigMap called `cluster-defaults`, with a `cluster-defaults.yaml` data key, and the settings you want to set in annotation syntax.
    
    For a complete list of annotations for Optimize Live settings, see the the [Optimization settings and descriptions](https://docs.stormforge.io/optimize-live/configure/settings/) topic.
    
    Your file will look something like this:
    
    ```yaml
    apiVersion: v1
    kind: ConfigMap
    metadata:
      name: cluster-defaults
      namespace: stormforge-system
    data:
      cluster-defaults.yaml: |
        live.stormforge.io/schedule: "P1D"
        live.stormforge.io/auto-deploy: "Disabled"
        live.stormforge.io/containers.cpu.requests.min: "20m"
        live.stormforge.io/containers.cpu.requests.max: "16000m"
    ...
    ```
    
    Copy
    
2. Apply the file:
    
    ```shell
    kubectl apply -f FILENAME -n stormforge-system
    ```
    
    Copy
    
3. Restart the StormForge Agent:
    
    ```shell
    kubectl rollout restart deployment stormforge-agent-workload-controller -n stormforge-system 
    ```
    
    Copy
    
    To check the status of the restart, run:
    
    ```sh
    kubectl rollout status deployment stormforge-agent-workload-controller -n stormforge-system -w
    ```
    
    Copy
    
    Any previous cluster-level default values are now removed, and your new defaults are in effect unless they are overridden at the namespace or workload level.
    
4. Optional: Confirm your changes by running the following command and then reviewing the `cluster-defaults.yaml` item in the **Data** section of the output:
    
    ```shell
    kubectl describe configmap cluster-defaults -n stormforge-system 
    ```
    
    Copy
    

### Setting cluster default values using `kubectl edit`[](https://docs.stormforge.io/optimize-live/configure/cluster-defaults/#defaults-using-kubectl-edit)

If the `cluster-defaults` ConfigMap has already been created, you can edit the ConfigMap directly.

1. Run the folllowing command:
    
    ```shell
    kubectl edit configmap cluster-defaults -n stormforge-system
    ```
    
    Copy
    
    If you see a `Error from server (NotFound): configmaps "cluster-defaults" not found` message, no cluster-level defaults are set. You must first create and apply a cluster defaults YAML file as described [above](https://docs.stormforge.io/optimize-live/configure/cluster-defaults/#defaults-using-kubectl-apply).
    
    If you don’t see an error message, continue to the next step.
    
2. In the `.data.cluster-defaults.yaml` section, add, edit, or remove annotation strings as needed.
    
    As an example, your annotations in the `cluster-defaults` ConfigMap might look something like this excerpt when you’re done:
    
    ```yaml
    # Please edit the object below. Lines beginning with a '#' will be ignored,
    # and an empty file will abort the edit. If an error occurs while saving this file will be
    # reopened with the relevant failures.
    #
    apiVersion: v1
    kind: ConfigMap
    data:
      cluster-defaults.yaml: |
        live.stormforge.io/auto-deploy: "Enabled"
        live.stormforge.io/cpu.optimization-goal: "Reliability"
        live.stormforge.io/memory.optimization-goal: "Reliability"
    ...
    ```
    
    Copy
    
    #### Tip
    
    To save time, you can copy the complete list of annotations from the sample ConfigMap YAML excerpt on the **Cluster** tab in the [Copy a template](https://docs.stormforge.io/optimize-live/configure/#quickstart-templates) section of the configuration topic.
    
3. Save your changes.
    
4. Restart the StormForge Agent:
    
    ```shell
    kubectl rollout restart deployment stormforge-agent-workload-controller -n stormforge-system
    ```
    
    Copy
    
    To check the status of the restart, run:
    
    ```sh
    kubectl rollout status deployment stormforge-agent-workload-controller -n stormforge-system -w
    ```
    
    Copy
    
    Any previous cluster-level default values are now removed, and your new defaults are in effect unless they are overridden at the namespace or workload level.
    
5. Optional: Confirm your changes by running the following command and then reviewing the annotations in the **Data** section of the output:
    
    ```shell
    kubectl describe configmap cluster-defaults -n stormforge-system 
    ```

---

# Configure optimization defaults for namespaces

Configure optimization settings for namespaces and workloads using annotations

The purpose of this topic is to describe how to use annotations to configure optimization settings.

#### Topics:[](https://docs.stormforge.io/optimize-live/configure/annotate-namespaces/#topics)

- [Configure default optimization settings for all workloads in a namespace](https://docs.stormforge.io/optimize-live/configure/annotate-namespaces/#annot-ns)
    - [Using YAML manifests](https://docs.stormforge.io/optimize-live/configure/annotate-namespaces/#annot-ns-yaml)
    - [Using `kubectl annotate`](https://docs.stormforge.io/optimize-live/configure/annotate-namespaces/#annot-ns-kubectl-annotate)

## Configure default optimization settings for all workloads in a namespace[](https://docs.stormforge.io/optimize-live/configure/annotate-namespaces/#annot-ns)

To configure settings for all workloads in a namesapce, edit the Namespace definition or run `kubectl annotate`.

Namespace-level defaults:

- Define the default optimization settings for all workloads in a namespace
- Override any equivalent cluster-level defaults
- Are specified using annotations on the namespace
- Fill in any settings not provided by annotations on the workloads themselves

### Using YAML manifests[](https://docs.stormforge.io/optimize-live/configure/annotate-namespaces/#annot-ns-yaml)

1. Open the namespace definition in your favorite editor. This is commonly done using commands like these (remember to replace NAMESPACE and FILENAME with your own values):
    
    ```shell
    kubectl get namespace NAMESPACE -o yaml > FILENAME && $EDITOR FILENAME
    ```
    
    Copy
    
    or:
    
    ```shell
    kubectl edit namespace NAMESPACE
    ```
    
    Copy
    
2. Edit the `metadata.annotations` section to include the annotations you need. For a complete list of annotations for Optimize Live settings, see the the [Optimization settings and descriptions](https://docs.stormforge.io/optimize-live/configure/settings/) topic.
    
    Your file will look something like this:
    
    ```yaml
    apiVersion: v1
    kind: Namespace
    metadata:
      name: example-namespace-name
      annotations:
        live.stormforge.io/schedule: "@daily"
        live.stormforge.io/auto-deploy: "Enabled"
    ...
    ```
    
    Copy
    
    #### Tip
    
    To save time, you can copy the complete list of annotations from the sample Namespace YAML excerpt on the **Namespace** tab in the [Copy a template](https://docs.stormforge.io/optimize-live/configure/#quickstart-templates) section of the configuration topic.
    
3. Save your changes.
    
4. If you chose to run the `kubectl get namespace NAMESPACE -o yaml > FILENAME ...` command in step 1, apply your changes.
    
    ```shell
    kubectl apply -f FILENAME
    ```
    
    Copy
    
5. Optional: Confirm your changes by running the following command and then reviewing the annotations in the `metadata.annotations` section of the output:
    
    ```shell
    kubectl get namespace NAMESPACE -o yaml
    ```
    
    Copy
    

### Using the `kubectl annotate` command[](https://docs.stormforge.io/optimize-live/configure/annotate-namespaces/#annot-ns-kubectl-annotate)

1. Run the `kubectl annotate` command and include the annotation:value pairs you want to set.
    
    As an example, a `kubectl annotate` might look something like this (remember to replace NAMESPACE with your appropriate value):
    
    ```shell
    kubectl annotate namespace NAMESPACE \
      live.stormforge.io/schedule="P1D" \
      live.stormforge.io/auto-deploy="Disabled" \
      live.stormforge.io/containers.cpu.requests.min="20m" \
      live.stormforge.io/containers.cpu.requests.max="16000m"
    ```
    
    Copy
    
    #### Tip
    
    To save time, you can copy the complete list of annotations from the sample Namespace YAML excerpt on the **Namespace** tab in the [Copy a template](https://docs.stormforge.io/optimize-live/configure/#quickstart-templates) section of the configuration topic. Be sure to replace the `:` separator from the template with `=` as shown in the sample command above.
    
2. Optional: To confirm your changes, run the following command and review the annotations in the `.metadata.annotations` section of the output:
    
    ```shell
    kubectl get namespace NAMESPACE -o yaml
    ```

--- 
# Configure optimization for individual workloads

Configure optimization settings for namespaces and workloads using annotations

The purpose of this topic is to describe how to use annotations to configure optimization settings.

#### Topics:[](https://docs.stormforge.io/optimize-live/configure/annotate-workloads/#topics)

- [Configure optimization settings for a specific workload](https://docs.stormforge.io/optimize-live/configure/annotate-workloads/#annot-wl)
    - [Using YAML manifests](https://docs.stormforge.io/optimize-live/configure/annotate-workloads/#annot-wl-yaml)
    - [Using `kubectl annotate`](https://docs.stormforge.io/optimize-live/configure/annotate-workloads/#annot-wl-kubectl-annotate)

## Configure optimization settings for a specific workload[](https://docs.stormforge.io/optimize-live/configure/annotate-workloads/#annot-wl)

To configure settings an individual workload, edit the resource definition or run `kubectl annotate`.

Workload optimization settings are defined by annotations in the `metadata.annotations` section of a Deployment, StatefulSet, or other supported workload resource type.

Workload optimization settings:

- Directly define configuration settings for a workload
- Are specified using annotations on workload resources, such as Deployments or StatefulSets
- Override equivalent values configured as defaults for the namespace or cluster

### Using YAML manifests[](https://docs.stormforge.io/optimize-live/configure/annotate-workloads/#annot-wl-yaml)

1. Open the workload definition in your favorite editor. This is commonly done using commands like these (remember to replace DEPLOYMENT and FILENAME with your own values):
    
    ```shell
    kubectl get deployment DEPLOYMENT -o yaml > FILENAME && $EDITOR FILENAME
    ```
    
    Copy
    
    or:
    
    ```shell
    kubectl edit deployment DEPLOYMENT
    ```
    
    Copy
    
2. Edit the `metadata.annotations` section to include the annotations you need. For a complete list of annotations for Optimize Live settings, see the the [Optimization settings and descriptions](https://docs.stormforge.io/optimize-live/configure/settings/) topic.
    
    Your file will look something like this:
    
    ```yaml
    apiVersion: apps/v1 # // just an example; represents any
    kind: Deployment    # \\ supported workload resource type
    metadata:
      name: example-workload-name
      annotations:
        live.stormforge.io/schedule: "@daily"
        live.stormforge.io/auto-deploy: "Enabled"
    ...
    ```
    
    Copy
    
    #### Tip
    
    To save time, you can copy the complete list of annotations from the sample Deployment YAML excerpt on the **Workload** tab in the [Copy a template](https://docs.stormforge.io/optimize-live/configure/#quickstart-templates) section of the configuration topic.
    
3. Save your changes.
    
4. If you chose to run the `kubectl get deployment DEPLOYMENT -o yaml > FILENAME ...` command in step 1, apply your changes.
    
    ```shell
    kubectl apply -f FILENAME
    ```
    
    Copy
    
5. Optional: Confirm your changes by running the following command and then reviewing the annotations in the `metadata.annotations` section of the output:
    
    ```shell
    kubectl get deployment DEPLOYMENT -o yaml
    ```
    
    Copy
    

### Using the `kubectl annotate` command[](https://docs.stormforge.io/optimize-live/configure/annotate-workloads/#annot-wl-kubectl-annotate)

1. Run the `kubectl annotate` command and include the `annotation=value` pairs you want to set.
    
    The kubernetes object you annotate should be the workload resource itself, such as a Deployment or StatefulSet.
    
    As an example, a `kubectl annotate` for a Deployment workload might look something like this (remember to replace NAME with your appropriate value):
    
    ```shell
    kubectl annotate deployment NAME \
      live.stormforge.io/schedule="@daily" \
      live.stormforge.io/auto-deploy="Enabled" \
      live.stormforge.io/containers.cpu.requests.min="20m" \
      live.stormforge.io/containers.cpu.requests.max="16000m"
    ```
    
    Copy
    
    #### Tip
    
    To save time, you can copy the pairs you need from the sample Namespace YAML excerpt on the **Namespace** tab in the [Copy a template](https://docs.stormforge.io/optimize-live/configure/#quickstart-templates) section of the configuration topic. Be sure to replace the `:` separator from the template with `=` as shown in the sample command above.
    
2. Optional: To confirm your changes, run the following command and review the annotations in the `.metadata.annotations` section of the output:
    
    ```shell
    kubectl get deployment NAME -o yaml
    ```

--- 
# Optimization goal

Recommendations are based on your risk tolerance and goal

Optimize Live always recommends values that minimally satisfy both savings and reliability, but you can set goals to shift the balance in favor of one or the other based on your risk tolerance and optimization goals.

The optimization goal applies to the entire workload.

### Optimization goal[](https://docs.stormforge.io/optimize-live/configure/settings/goal/#opt-goal)

Used in determining recommended values based on your goals and risk tolerance.

|Annotation|Default value|
|---|---|
|`live.stormforge.io/cpu.optimization-goal`|`"Balanced"`|
|`live.stormforge.io/memory.optimization-goal`|`"Balanced"`|

##### Description[](https://docs.stormforge.io/optimize-live/configure/settings/goal/#opt-goal-description)

The optimization goal for a resource indicates which of two competing criteria to maximize when computing recommended request values: cost savings or workload reliability. Optimize Live will always produce values that minimally satisfy both criteria, but the goal setting can be used to shift the balance in favor of one or the other.

###### Valid values[](https://docs.stormforge.io/optimize-live/configure/settings/goal/#opt-goal-valid-values)

- `Balanced` (default): Provides a balanced approach to achieving cost savings and workload reliability.
- `Savings`: Provides recommendations that are closer to actual CPU or memory usage. Consider this option when you want to maximize your resource savings.
- `Reliability`: Minimizes the risk of usage bursting over request values or hitting CPU or memory limits. Consider this option for business-critical applications.

##### Key points[](https://docs.stormforge.io/optimize-live/configure/settings/goal/#opt-goal-key-points)

- CPU and memory optimization goals can differ. For example, if your organization can tolerate throttling when containers exceed CPU limits but cannot tolerate restarts when containers exceed memory limits, you can set a **Savings** goal for CPU and a **Reliability** goal for memory.

Last modified June 6, 2024

---
# Schedule

Learning period and schedule settings define when Optimize Live generates recommendations

Optimize Live observes new workloads for a set period of time, or _learning period_, and generates recommendations at the interval defined by the _schedule_.

Recommendations generated during the learning period are referred to as _preliminary recommendations_: you can review them and apply them on demand (by clicking **Apply Now** on the workload details page), but they cannot be auto-deployed, even if [auto-deploy](https://docs.stormforge.io/optimize-live/configure/settings/auto-deploy/#auto-deploy) is enabled.

For new workloads, preliminary recommendations are **hourly for the first 23 hours. After 23 hours, they’re generated as defined by the recommendation schedule** - by default, once daily (`@daily`), for the remainder of the learning period and beyond.

For more details and examples showing how these settings are related, see the [Schedule](https://docs.stormforge.io/optimize-live/concepts/#schedule), [Learning period](https://docs.stormforge.io/optimize-live/concepts/#learning-period), and [Preliminary recommendations](https://docs.stormforge.io/optimize-live/concepts/#prel-recs-concepts) sections in the Concepts topic.

#### Recommendation settings:[](https://docs.stormforge.io/optimize-live/configure/settings/schedule/#recommendation-settings)

- [Recommendation schedule](https://docs.stormforge.io/optimize-live/configure/settings/schedule/#schedule)
- [Learning period](https://docs.stormforge.io/optimize-live/configure/settings/schedule/#learning-period)

### Schedule[](https://docs.stormforge.io/optimize-live/configure/settings/schedule/#schedule)

The schedule on which Optimize Live generates new recommendations for a workload.

|Annotation|Default value|
|---|---|
|`live.stormforge.io/schedule`|`"@daily"` (equivalent to `P1D`)|

##### Description[](https://docs.stormforge.io/optimize-live/configure/settings/schedule/#schedule-description)

Recommendations are generated automatically for workloads on a schedule, defined by a schedule string. The shortest valid recommendation schedule is once an hour.

The schedule also affects every recommendation’s TTL, or time-to-live. The TTL is how long the recommended values are considered valid for. After a recommendation’s TTL expires, the recommended values are replaced by new values from an updated recommendation.

To prevent the restarting of many workloads at the same time, Optimize Live staggers the generation and applying of recommendations throughout the schedule period (when the schedule is an ISO 8601 Duration string or equivalent schedule macro). Examples:

- `@daily` or `P1D`: recommendations are generated and applied across 24 hours
    
- `PT12H`: recommendations are generated and applied across 12 hours
    
    If you require more precise timing for when recommendations are applied, use a cron expression as described below.
    

##### Duration expressions[](https://docs.stormforge.io/optimize-live/configure/settings/schedule/#duration-expressions)

Valid ISO 8601 [Duration](https://en.wikipedia.org/wiki/ISO_8601#Durations) strings can be specified.

###### Examples[](https://docs.stormforge.io/optimize-live/configure/settings/schedule/#schedule-duration-examples)

- `PT1H` – Once an hour
- `P1D` – Once a day
- `P7D` – Once a week

##### Cron expressions[](https://docs.stormforge.io/optimize-live/configure/settings/schedule/#cron-expressions)

[Cron](https://en.wikipedia.org/wiki/Cron) strings can be used to designate schedules with more specific requirements, such as day-of-week. Cron expressions should specify five fields. For day-of-week, friendly terms such as `WED` or `THU` are acceptable in place of numbers. Optimize Live recognizes the special value `H` in a field to mean “hash” this value, and use a deterministic, but functionally random value for that field.

Cron times must always be specified in UTC.

###### Examples[](https://docs.stormforge.io/optimize-live/configure/settings/schedule/#schedule-cron-examples)

- `H H * * THU` – Once every Thursday
- `30 0 * * SAT,MON` – 12:30am each Saturday and each Monday UTC
- `H H(0-2) * * *` – Every day between 12:00am and 2:59am UTC
- `H H(7-9) * * SATL` - Between 7:00am and 9:59am UTC on the last Saturday of the month

##### Schedule macros[](https://docs.stormforge.io/optimize-live/configure/settings/schedule/#schedule-macros)

Macros are shorthand that can be used as syntactic sugar for common schedules. The available macros are described below and compared with their duration and cron equivalents.

|Macro|Duration|Cron|Description|
|---|---|---|---|
|`@never`|`P0D`|N/A|Do not generate recommendations automatically|
|`@hourly`|`PT1H`|`H * * * *`|Once every hour|
|`@daily`|`P1D`|`H H * * *`|Once every day|
|`@weekly`|`P7D`|`H H * * H`|Once every week|
|`@midnight`|N/A|`H H(0-2) * * *`|Every day between 12:00am and 2:59am UTC|

##### Key points[](https://docs.stormforge.io/optimize-live/configure/settings/schedule/#schedule-key-points)

- Each workload can have one and only one schedule string defined for it, of either a duration, cron expression, or schedule macro.
- Exact times are not guaranteed for recommendation generation. For exact cron strings, recommendations are generated within an hour of the time specified.
- To avoid concentrated pod churn when new recommendations are applied, use schedules that spread optimization over a period of time. The `H` capability in cron expressions or using non-specific durations can both help achieve an appropriate scheduling distribution.

### Learning period[](https://docs.stormforge.io/optimize-live/configure/settings/schedule/#learning-period)

Acts as an automation gate, defining how long Optimize Live observes a new workload before providing recommendations that can be auto-deployed.

|Annotation|Default value|
|---|---|
|`live.stormforge.io/learning-period`|`"P7D"`|

##### Description[](https://docs.stormforge.io/optimize-live/configure/settings/schedule/#learning-period-description)

During this observation or _learning period_, Optimize Live generates _preliminary recommendations_ based on the metrics it has collected. Preliminary recommendations are not auto-deployed, but they can be applied on demand.

If you want to automatically deploy recommendations sooner-for example, for short-running workloads, branch-based deploys, or other ephemeral environments-you can shorten the learning period. Otherwise, it typically isn’t necessary to change this value.

The shortest valid duration is one day (`P1D`).

Recommendations generated after the learning period is complete are deployed automatically if [auto-deploy](https://docs.stormforge.io/optimize-live/configure/settings/auto-deploy/#auto-deploy) is enabled.

##### Duration expressions[](https://docs.stormforge.io/optimize-live/configure/settings/schedule/#learning-period-duration-examples)

Only valid ISO 8601 [Duration](https://en.wikipedia.org/wiki/ISO_8601#Durations) strings can be specified.

###### Examples[](https://docs.stormforge.io/optimize-live/configure/settings/schedule/#learning-period-examples)

- “`P1D`” – One day (minimum value)
- “`P3D`” – Three days
- “`P7D`” – One week (default)
- ---

# Reliability response

Configure Optimize Live to respond to OOM events with a temporary memory bump-up

As changes in memory usage occur, Optimize Live detects and reports out-of-memory (OOM) events on all workload types as it collects metrics. You can configure Optimize Live to respond to OOM events by applying a temporary memory bump-up and indicate when the bump-up is to be applied.

#### Note:

Note: Optimize Live tracks and reports OOM events on all workload types. However, at this time, temporary memory bump-ups are supported for Deployments and ReplicaSets only. Memory bump-ups are not supported at this time for Statefulsets, Daemonsets, and CronJobs.

### Out-of-memory events response[](https://docs.stormforge.io/optimize-live/configure/settings/reliability/#oom)

Defines the values that Optimize Live uses to calculate the temporary memory bump-up added to a container’s memory requests after an OOM event, and indicates when to apply the bump-up.

|Annotation|Default value|
|---|---|
|`live.stormforge.io/reliability.oom.memory-bump-up.period`|`"P4D"`|
|`live.stormforge.io/reliability.oom.memory-bump-up.percent`|`"0"`|
|`live.stormforge.io/reliability.oom.memory-bump-up.min`|`"0Mi"`|
|`live.stormforge.io/reliability.oom.memory-bump-up.max`|`"2Gi"`|
|`live.stormforge.io/reliability.oom.memory-bump-up.apply-immediately`|`"Never"`|

##### Description[](https://docs.stormforge.io/optimize-live/configure/settings/reliability/#oom-description)

**To prevent unexpected results, this feature is disabled by default.**

When a container in a workload is OOMkilled, Optimize Live immediately generates a recommendation using the configured memory bump-up percent (default value is `"0"`), and if configured to do so, applies this recommendation immediately (default value is `"Never"`).

These two default values disable memory bump-ups in order to prevent unexpected results or downtime from applying recommendations outside of a schedule.

The bump-up is calculated for—and applied to—OOMKilled containers only. **The calculated bump-up respects an OOMKilled container’s configured memory bounds, optimization policy, and limits-to-requests ratio (LRR).**

The `live.stormforge.io/reliability.oom.memory-bump-up.*` annotations can be configured based on the workload resource kind, using the following syntax:

```yaml
"100Mi,resource:daemonsets=0Mi"
"100Mi,resource:daemonsets=0Mi"
```

Copy

and

```yaml
"Always,resource:jobs=Never"
```

Copy

###### How to configure bump-ups[](https://docs.stormforge.io/optimize-live/configure/settings/reliability/#oom-enable-bump-ups)

You can configure memory bump-ups at the [cluster](https://docs.stormforge.io/optimize-live/configure/cluster-defaults/), [namespace](https://docs.stormforge.io/optimize-live/configure/annotate-namespaces/), or [workload](https://docs.stormforge.io/optimize-live/configure/annotate-workloads/) level.

To configure bump-ups, complete these high-level steps:

1. Set `live.stormforge.io/reliability.oom.memory-bump-up.percent` to an integer value greater than 0.
2. Set `live.stormforge.io/reliability.oom.memory-bump-up.apply-immediately` to `Always` or `IfAutoDeployEnabled` (see [Valid values](https://docs.stormforge.io/optimize-live/configure/settings/reliability/#oom-valid-values) below).
3. Optional: Set the bump-up min and max values. See default values above.
4. At this time, the following additional configuration is required. You must:
    - Disable memory bump-ups for Daemonsets.
    - Disable auto-deploy for DaemonSets and StatefulSets.

A recommended default configuration is provided in the [examples](https://docs.stormforge.io/optimize-live/configure/settings/reliability/#oom-examples) section later in this topic.

###### Bump-up period[](https://docs.stormforge.io/optimize-live/configure/settings/reliability/#oom-bump-up-period)

The bump-up period defines how long Optimize Live calculates and applies memory bump-ups for each OOMKilled container in a workload. When a container in a workload is OOMKilled, the container’s bump-up period begins and recommendations contain the memory bump-up values. The container’s bump-up period resets on subsequent OOMKills.

When a container’s bump-up period ends, bump-ups are no longer calculated and recommendations are based on the observed resource usage.

There is typically no need to change the bump-up peroiod. You might choose to extend it if you want to be particularly conservative about memory, or you might lower it for workloads that you expect to see occasional OOM activity from due to intentional design or known issues.

###### Reporting and tracking[](https://docs.stormforge.io/optimize-live/configure/settings/reliability/#oom-report-track)

All OOM events are tracked and counted, regardless of the workload type.

You can view OOM events as follows:

- **By estate and cluster:** On the Reports page, see the OOM Events graph. You can filter by cluster and time period at the top of the page.
    
- **By container:** On the workload details page, click the **Recommendation** tab and then click a container name. OOM events are shown as timeline markers (to within 5 minutes of accuracy) along the x-axis of a container’s Average Memory Usage, Requests, and Limits graph.
    
    After a bump-up is applied, you can see the immediate increase in the recommended and current requests on a container’s Average Memory Usage, Requests, and Limits graph on the workload details page. If configured to apply the bump-up immediately after an OOM event, this increase also corresponds to the OOM event marker on the graph’s x-axis.
    

###### Valid values[](https://docs.stormforge.io/optimize-live/configure/settings/reliability/#oom-valid-values)

- `live.stormforge.io/reliability.oom.memory-bump-up.period`
    - [ISO-8601 duration](https://en.wikipedia.org/wiki/ISO_8601#Durations) string defining how long Optimize Live will add a memory bump-up to recommendations after an OOM event. Typically measured in days; default is “`P4D`”. There is typically no need to change this value (see [Bump-up period](https://docs.stormforge.io/optimize-live/configure/settings/reliability/#oom-bump-up-period) above).
- `live.stormforge.io/reliability.oom.memory-bump-up.percent`
    - String representing a percentage to increase the memory setting as a response to an OOM event
    - Valid values: “`0`” to “`100`”
- `live.stormforge.io/reliability.oom.memory-bump-up.min` and `live.stormforge.io/reliability.oom.memory-bump-up.max`:
    - A positive quantity with a Kubernetes memory unit, such as `"2Gi"`
    - Represents a min and max amount to add to a container’s memory requests
    - Setting a minimum > 0 reduces pod churn
- `live.stormforge.io/reliability.oom.memory-bump-up.apply-immediately`:
    - `Never`: Memory bump-ups are never applied immediately. If auto-deploy is enabled for the workload, the bump-up is included in the next _scheduled_ recommendation (as long as the bump-up period is in effect) to prevent unexpected downtime during peak hours.
    - `IfAutoDeployEnabled`: Memory bump-ups are applied immediately if auto-deploy is enabled for the workload. If auto-deploy is not enabled, any recommendation applied on demand within the bump-up-period has the bump-up percentage added to it.
    - `Always`: Memory bump-ups are always applied immediately and automatically after OOM events. This ensures the workload recovers quickly and decreases the possibility of future OOM events.

##### Examples[](https://docs.stormforge.io/optimize-live/configure/settings/reliability/#oom-examples)

- Recommended default OOM response: Bump up memory by 20%, minimum increase 100Mi, maximum increase 2Gi, apply the bump-up immediately if auto-deploy is enabled for the workload:
    
    - If auto-deploy is _not_ enabled for the workload, the bump-up is applied the next time a recommendation is applied on demand.
    
    ```yaml
    live.stormforge.io/reliability.oom.memory-bump-up.percent: "20,resource:daemonsets=0"
    live.stormforge.io/reliability.oom.memory-bump-up.min: "100Mi,resource:daemonsets=0Mi"
    live.stormforge.io/reliability.oom.memory-bump-up.max: "2Gi"
    live.stormforge.io/reliability.oom.apply-memory-bump-up-immediately: "IfAutoDeployEnabled,resource:daemonsets=Never,resource:statefulsets=Never"
    live.stormforge.io/reliability.oom.memory-bump-up.period: "P4D" 
    ```
    
    Copy
    
- Bump up memory by 20%, minimum increase 100Mi, maximum increase 2Gi, never apply the new recommendation immediately:
    
    - If auto-deploy is enabled, the next scheduled recommendation will contain the bump-up values if the bump-up period is still in effect.
    - If auto-deploy is _not_ enabled and the recommendation is applied on demand during the bump-up period, the bump-up values are applied. If the bump-up period is over, recommended values are based on observed resource usage.
    
    ```yaml
    live.stormforge.io/reliability.oom.memory-bump-up.percent: "20,resource:daemonsets=0"
    live.stormforge.io/reliability.oom.memory-bump-up.min: "100Mi,resource:daemonsets=0Mi"
    live.stormforge.io/reliability.oom.memory-bump-up.max: "2Gi"
    live.stormforge.io/reliability.oom.apply-memory-bump-up-immediately: "Never,resource:daemonsets=Never,resource:statefulsets=Never"
    live.stormforge.io/reliability.oom.memory-bump-up.period: "P4D"
    ```
    
    Copy
    
- Disable bump-ups
    
    ```yaml
    live.stormforge.io/reliability.oom.memory-bump-up.percent: "0"
    live.stormforge.io/reliability.oom.memory-bump-up.min: "0"
    live.stormforge.io/reliability.oom.memory-bump-up.max: "2Gi"
    live.stormforge.io/reliability.oom.apply-memory-bump-up-immediately: "Never"
    ```
    
    Copy
    

Last modified December 17, 2024

-- - 
# Containers

These settings define how individual containers are optimized

Container-level settings are applied to workloads, just like workload-level settings, but they specify values that can vary from container to container within a workload.

#### Container-level settings:[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#container-level-settings)

- [Optimization policy](https://docs.stormforge.io/optimize-live/configure/settings/containers/#opt-policy)
- [Limit-to-request ratio](https://docs.stormforge.io/optimize-live/configure/settings/containers/#lrr)
- [Min and max for requests](https://docs.stormforge.io/optimize-live/configure/settings/containers/#requests-min-max)
- [Min and max for limits](https://docs.stormforge.io/optimize-live/configure/settings/containers/#limits-min-max)
- [Patch paths](https://docs.stormforge.io/optimize-live/configure/settings/containers/#patch-path)

For details about how to set these values using annotations, see one of these topics: [Configure clusters](https://docs.stormforge.io/optimize-live/configure/cluster-defaults/), [Configure namespaces](https://docs.stormforge.io/optimize-live/configure/annotate-namespaces/), or [Configure workloads](https://docs.stormforge.io/optimize-live/configure/annotate-workloads/).

## Container-level settings syntax[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#container-level-settings-syntax)

When specifying configuration values for container-level settings, you can specify a default value for all containers, one or more values for specific named containers, or a comma-separated list.

- **Default** (`"RequestsRaiseLimitsIfNeeded"`): default values for all containers are simple strings with a valid value for the setting. The default value is used for any containers that do not have a named value.
- **Named** (`"istio-proxy=DoNotOptimize"`): named container settings apply the value to containers with the given name. The name is specified first, followed by an `=` sign, then the value to apply to that container.
- **Comma-separated** (`"RequestsRaiseLimitsIfNeeded,istio-proxy=DoNotOptimize"`): an optional default, and one or more named values, can be specified as a comma-separated list. When specifying multiple values, start with the default (if you are including one), then list each named container value.

### Annotation examples[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#annotation-examples)

```yaml
live.stormforge.io/containers.cpu.requests.min: "10m"
live.stormforge.io/containers.cpu.requests.max: "16000m,jenkins=4000m,logshipper=20m"
live.stormforge.io/containers.memory.requests.min: "128Mi,jenkins=1Gi"
live.stormforge.io/containers.memory.requests.max: "logshipper=512Mi"
```

Copy

## Container settings[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#container-settings)

The following settings specify per-container values.

---

### Optimization policy[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#opt-policy)

Indicates what to optimize for a container, for each resource (CPU and memory).

|Annotation|Default value|
|---|---|
|`live.stormforge.io/containers.cpu.optimization-policy`|`"RequestsRaiseLimitsIfNeeded"`|
|`live.stormforge.io/containers.memory.optimization-policy`|`"RequestsRaiseLimitsIfNeeded"`|

##### Description[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#opt-policy-description)

The configured optimization policy for a resource dictates how (and whether) Optimize Live will recommend and make changes to a resource (CPU or memory). There are several ways organizations might like to manage limits, and there are use cases for choosing not to optimize a workload or container at all. Selecting an appropriate value for this setting should enable organizations to implement the resource management style of their choice.

###### Valid values[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#opt-policy-valid-values)

- `RequestsRaiseLimitsIfNeeded` (default): Always optimize requests. Optimize limits only if they already exist:
    - If limits are set and are high enough already, leave them at their existing values.
        
    - If limits are lower than the recommended values, raise the limits to the recommended values.
        
    - If limits are higher than what Optimize Live recommends, do not modify them. Optimize Live will never lower a limit when using this policy.
        
    - If no limits are set, don’t set them.
        
        Optimize Live calculates its recommended limits as follows:  
        `min(max-limit, recommended-requests × limit-request-ratio)`
        
- `RequestsAndLimits`: Optimize both requests and limits. If limits don’t exist, Optimize Live will add them.
- `RequestsOnly`: Optimize requests only and do not modify limits. If limits are set, the existing limits will act as a constraint on the maximum value that Optimize Live can recommend for requests.
- `DoNotOptimize`: Optimize neither requests nor limits. Optimize Live will not suggest modifications to any existing settings for the resource.

##### Key points[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#opt-policy-key-points)

- Optimization policy defines how and whether requests and limits will be optimized.
    
- Injected containers cannot be optimized without extra configuration. One way to handle this is to set both the CPU and memory policies for injected sidecar containers to `DoNotOptimize`. For example:
    
    ```yaml
    live.stormforge.io/containers.cpu.optimization-policy: "istio-proxy=DoNotOptimize"
    live.stormforge.io/containers.memory.optimization-policy: "istio-proxy=DoNotOptimize"
    ```
    
    Copy
    

---

### Limit-to-request ratio (LRR)[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#lrr)

This value is used to calculate limits when the optimization policy is set to `RequestsRaiseLimitsIfNeeded` or `RequestsAndLimits`.

|Annotation|Default value|
|---|---|
|`live.stormforge.io/containers.cpu.limits.limit-request-ratio`|`"2.0"`|
|`live.stormforge.io/containers.memory.limits.limit-request-ratio`|`"2.0"`|

##### Description[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#lrr-description)

When Optimize Live is configured to set limits, the limit it sets is computed as the recommended request value multiplied by the LRR. This ratio can be adjusted separately for each resource, CPU or memory.

###### Valid values[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#lrr-valid-values)

- `"2.0"` (default)
- `"1.0"` (Guaranteed QoS)
- Any value >= `"1.0"` to a maximum of two decimal places

###### Key points[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#lrr-key-points)

- If the `RequestsOnly` or `DoNotOptimize` policy is in use, the LRR setting has no effect.
- Using an LRR that permits bursting, such as `"2.0"`, lets workloads occasionally exceed their request values without being throttled or OOM-killed. This is advisable when automating request settings, because it gives Optimize Live time to come back and adjust resource requests as necessary, rather than the workload being immediately OOM-killed or unnecessarily throttled.

---

### Minimum and maximum bounds for requests[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#requests-min-max)

Values indicate the lower bound and upper bound of the range for CPU or memory requests.

|Annotation|Default value|
|---|---|
|`live.stormforge.io/containers.cpu.requests.min`|None|
|`live.stormforge.io/containers.cpu.requests.max`|None|
|`live.stormforge.io/containers.memory.requests.min`|None|
|`live.stormforge.io/containers.memory.requests.max`|None|

##### Description[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#requests-min-max-description)

The minimum and maximum **request** bounds for each resource act as a constraint on what request values Optimize Live will recommend, regardless of the observed usage for the resource. These bounds can be used to set a floor below which requests will never drop and a ceiling above which Optimize Live will never raise them.

When used as defaults for the cluster, request bounds can be used to implement default automation policies such as “never allocate less than 10m of CPU” or “never allocate more than 16Gi of memory without a specific exception”. Exceptions can then be implemented by overriding the cluster default settings on a per-namespace or per-workload basis.

###### Valid values[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#requests-min-max-valid-values)

Any positive Kubernetes quantity, appropriate to the resource. Examples:

- `"10m"` (for CPU)
- `"32Gi"` (for memory)

---

### Minimum and maximum bounds for limits[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#limits-min-max)

Values indicate the lower bound and upper bound of the range for CPU or memory limits.

|Annotation|Default value|
|---|---|
|`live.stormforge.io/containers.cpu.limits.min`|None|
|`live.stormforge.io/containers.cpu.limits.max`|None|
|`live.stormforge.io/containers.memory.limits.min`|None|
|`live.stormforge.io/containers.memory.limits.max`|None|

##### Description[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#limits-min-max-description)

The minimum and maximum **limit** bounds for each resource act as a constraint on what limit values Optimize Live will set, regardless of the request value for the resource. These bounds can be used to set a floor below which limits will never drop and a ceiling above which Optimize Live will never raise limits.

When used as defaults for the cluster, limit bounds can be used to implement default automation policies such as “never set a CPU limit of less than 1 full core” or “never limit memory to less than 512Mi”.

###### Valid values[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#limits-min-max-valid-values)

Any positive Kubernetes quantity, appropriate to the resource. Examples:

- `"1000m"` (for CPU)
- `"512Mi"` (for memory)

---

### Patch paths[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#patch-path)

A patchPath maps a container resource value from a recommendation to where it belongs in the patchTarget.

|Annotation|Default value|
|---|---|
|`live.stormforge.io/containers.cpu.requests.patch-path`|None|
|`live.stormforge.io/containers.cpu.limits.patch-path`|None|
|`live.stormforge.io/containers.memory.requests.patch-path`|None|
|`live.stormforge.io/containers.memory.limits.patch-path`|None|

##### Description[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#patch-path-description)

For built-in Kubernetes workload types, StormForge knows which fields correspond to request and limit values and can automatically generate patches. When generating patches for workloads owned by custom resource types (CRDs), the patch path settings let you specify which CRD fields StormForge will update with recommended request or limit values.

###### Valid values[](https://docs.stormforge.io/optimize-live/configure/settings/containers/#patch-path-values)

String. Examples:

- `"/spec/resources/requests/cpu"`
- `"/spec/resources/limits/cpu"`
- `"/spec/resources/requests/memory"`
- `"/spec/resources/limits/memory"`
- `"/spec/resources/limits/cpu,fluentd=/spec/fluentd/resources/limits/cpu"`
---
# HPA target utilization

This setting defines range for HPA target utilization

### HPA target utilization[](https://docs.stormforge.io/optimize-live/configure/settings/hpa/#hpa-target)

Specifies the lower bound and upper bound of the range within which Optimize Live can set HPA target utilization.

|Annotation|Default value|
|---|---|
|`live.stormforge.io/hpa.cpu.target-utilization.min`|None|
|`live.stormforge.io/hpa.cpu.target-utilization.max`|None|
|`live.stormforge.io/hpa.memory.target-utilization.min`|None|
|`live.stormforge.io/hpa.memory.target-utilization.max`|None|

##### Description[](https://docs.stormforge.io/optimize-live/configure/settings/hpa/#hpa-target-description)

HPA target utilization min and max are constraints that prevent Optimize Live from recommending HPA target utilization values outside of the defined bounds. The target utilization constraints are specified separately for CPU and for memory. These settings have an effect only if an HPA is enabled for a workload, and only if the HPA scales on CPU or scales on memory.

###### Valid values[](https://docs.stormforge.io/optimize-live/configure/settings/hpa/#hpa-target-valid-values)

- Integer strings from `"0"` to `"100"`
---
# Runtime

These settings define how runtime-specific recommendations are applied to workloads

## Java runtime[](https://docs.stormforge.io/optimize-live/configure/settings/runtime/#java)

You can define how Optimize Live applies JVM max heap size recommendations to JVM containers.

The Java max heap recommendation settings apply to workloads identified as JVM workloads that Optimize Live is able to collect JVM metrics for. For non-Java workloads, these settings will have no effect.

StormForge by default assumes that Java applications use the `-XX:MaxRamPercentage` heap size management mechanism, and that changing the container’s memory limit will therefore change the effective max heap size. StormForge will attempt to use this relationship to optimize heap size without changing any configuration for your app.

If an app does not use `-XX:MaxRamPercentage`, you will need to adjust the [max heap patch path](https://docs.stormforge.io/optimize-live/configure/settings/runtime/#maxheap-patchpath) setting to define another way of automating the heap size.

For more information about Java recommendations, see [Java heap size](https://docs.stormforge.io/optimize-live/recommendations/java/).

### Max heap patch path[](https://docs.stormforge.io/optimize-live/configure/settings/runtime/#maxheap-patchpath)

Specifies where the value for Java Max Heap should be in the Optimize Live patch.

|Annotation|Default value|
|---|---|
|`live.stormforge.io/containers.java.max-heap.patch-path`|`-`|

##### Description[](https://docs.stormforge.io/optimize-live/configure/settings/runtime/#description)

This setting controls how Optimize Live applies its recommended max heap value to workloads.

If you don’t configure a patch-path, Optimize Live won’t directly update a specific value for max heap anywhere in the workload. Instead, Optimize Live will take the JVM’s observed `MaxRamPercentage` as a constant and adjust the container’s memory limit in order to change the heap size.

If you configure a patch-path, Optimize Live will instead inject the recommended max heap value into the workload at the location you specify.

|In order to:|Set patch-path to:|
|---|---|
|Use the memory limit to effect changes to heap size|`-` (or None)|
|Set heap values using an environment variable|`{{ .EnvVarPath "STORMFORGE_JAVA_ARGS" }}`|
|Set heap value in a custom field (JSON pointer)|`/spec/{{ .ContainerName }}/jvm-max-heap`|

### Max heap patch format[](https://docs.stormforge.io/optimize-live/configure/settings/runtime/#maxheap-patchformat)

Specifies how to format the Java Max Heap recommended value in Optimize Live patches.

|Annotation|Default value|
|---|---|
|`live.stormforge.io/containers.java.max-heap.patch-format`|None|

##### Description[](https://docs.stormforge.io/optimize-live/configure/settings/runtime/#description-1)

The format Optimize Live uses when it injects a recommended value into a workload can be customized by setting a patch-format.

If you don’t configure a specific patch-format, Optimize Live’s default behavior is to produce a `MaxRamPercentage` setting (`-XX:MaxRamPercentage=VALUE`) if the workload has a memory limit. If the workload does not have a memory limit, it will produce a `MaxHeapSize` setting (`-XX:MaxHeapSize=VALUE`) instead.

This setting has no effect when [patch-path](https://docs.stormforge.io/optimize-live/configure/settings/runtime/#maxheap-patchpath) is set to `-`.

|In order to:|Set patch-format to:|
|---|---|
|Let Optimize Live pick how to output max heap setting|None|
|Produce a `-XX:MaxRamPercentage` setting|`{{ jvmOption "-XX:MaxRamPercentage" (round (.MemoryLimit.AsApproximateFloat64 \| divf .Value.AsApproximateFloat64 \| mulf 100) 2 1) }}`|
|Produce a `-XX:MaxHeapSize` setting|`{{- jvmOption "-XX:MaxHeapSize" .Value }}`|

### Minimum and maximum bounds for max heap[](https://docs.stormforge.io/optimize-live/configure/settings/runtime/#maxheap-bounds)

Values indicate the lower bound and upper bound of the range for Java max heap.

|Annotation|Default value|
|---|---|
|`live.stormforge.io/containers.java.max-heap.min`|None|
|`live.stormforge.io/containers.java.max-heap.max`|None|

##### Description[](https://docs.stormforge.io/optimize-live/configure/settings/runtime/#description-2)

The minimum and maximum bounds for Java max heap acts a constraint on what max heap values Optimize Live will recommend, regardless of the observed heap usage. These bounds can be used to set a floor below which the max heap should never drop and a ceiling above which Optimize Live will never raise it.

When used as defaults for the cluster, max heap bounds can be used to implement default automation policies such as “never set max heap of less than 128Mi” or “never set max heap higher than 8192Gi”.

---
# Requests and limits

Recommendations for CPU and memory resource settings

  2 minute read  

Every StormForge recommendation includes CPU and memory requests that the machine learning has determined to be optimal for each container in a workload.

Optimize Live generates CPU and memory recommendations using our patent pending machine learning. Our machine learning examines each container’s resource usage metrics, and monitors usage patterns and scaling behavior to come up with the optimal CPU and memory resource settings.

## Requests[](https://docs.stormforge.io/optimize-live/recommendations/requests-and-limits/#requests)

Request recommendations for CPU and memory are based on observed resource usage, constrained by optimization settings. After the machine learning generates recommendation candidates, an effective recommendation is created by:

1. Selecting a recommendation candidate based on each workload’s configured [Optimization Goal](https://docs.stormforge.io/optimize-live/configure/settings/goal/).
2. Applying all of the configured constraints, such as [min and max request bounds](https://docs.stormforge.io/optimize-live/configure/settings/containers/#requests-min-max).

## Limits[](https://docs.stormforge.io/optimize-live/recommendations/requests-and-limits/#limits)

Limit recommendations for CPU and memory are optional, and StormForge offers a high degree of control over whether and how to set limits. If you would like to include limits in a recommendation, the recommended limits will usually be created by:

1. Multiplying the recommended request value by a configurable [limit-to-request-ratio](https://docs.stormforge.io/optimize-live/configure/settings/containers/#lrr), or LRR.
2. Applying all of the configured constraints, such as [min and max limit bounds](https://docs.stormforge.io/optimize-live/configure/settings/containers/#limits-min-max).

Whether and how to recommend limits is controlled by [Optimization Policy](https://docs.stormforge.io/optimize-live/configure/settings/containers/#opt-policy).

## HPA and target utilization[](https://docs.stormforge.io/optimize-live/recommendations/requests-and-limits/#hpa-and-target-utilization)

StormForge is compatible with existing horizontal pod autoscalers. If a workload has an HPA, StormForge’s recommendation will include updates to the HPA target utilization values(s) that ensure StormForge’s vertical scaling activity will not cause conflict with, and will not be negated by, the HPA.

The purpose of the adjustments StormForge recommends for HPA target utilization is to preserve observed scaling behavior, while vertically resizing pods within it.

The range within StormForge is allowed to adjust the HPA’s target utilization can be constrained by [min and max bounds](https://docs.stormforge.io/optimize-live/configure/settings/hpa/).

---
# Pod scheduling

Automated node affinity for proportional resource scheduling

  2 minute read  

StormForge recommendations can optionally include node affinity, hard or soft, that influences the scheduler to place workloads on specific kinds of nodes.

The goal of this feature is to provide better node utilization and bin packing by placing workloads on nodes that match their CPU and memory characteristics. Optimize Live categorizes every workload according to its `CPU:Memory` request ratio, then adds node affinity for node types with similar `CPU:Memory` resource ratios.

## Pre-work[](https://docs.stormforge.io/optimize-live/recommendations/pod-scheduling/#pre-work)

At present, this feature mandates the use of specific labels and node `CPU:Memory` resource ratios. In a future release, labels, node categories, and `CPU:Memory` ratios will all be configurable.

In order to use the feature you will need to add a specific instance category label to your nodes, with a value indicating the named `CPU:Memory` ratio it most closely aligns with. By default the label and values needed are:

**Category label:**

||
|---|
|stormforge.io/instance-category|

**Category label values:**

|Title|Label value|`CPU:Mem` ratio|
|---|---|---|
|Compute Optimized|compute-optimized|`1:2`|
|General Purpose|general-purpose|`1:4`|
|Memory Optimized|memory-optimized|`1:8`|

The `CPU:Memory` ratio units are cores to gibibytes (Gi).

## Using pod scheduling recommendations[](https://docs.stormforge.io/optimize-live/recommendations/pod-scheduling/#using-pod-scheduling-recommendations)

After configuring your node labels or node groups, you can use Optimize Live to apply right-sizing recommendations that include node affinity to help the scheduler more tightly binpack your nodes.

1. At the bottom of the recommendation details page for each workload you will see an “instance category” as part of the recommendation.
    
    ![View category](https://docs.stormforge.io/img/docs/recommendations/10-view-category.png)
    
2. On the patches tab for a workload you can preview what the patch will look like if you enable applying our recommended instance categories.
    
    ![Preview affinity patch](https://docs.stormforge.io/img/docs/recommendations/20-preview-affinity-patch.png)
    
3. Finally, you can enable automatic application of the instance category recommendations by setting configuration via annotations. We display the configuration in the UI under the pod scheduling section.
    
    ![Configure pod scheduling](https://docs.stormforge.io/img/docs/recommendations/30-configure-pod-scheduling.png)
    
4. The simplest way to test that the node affinities are working as expected is to go to the patches tab, preview the patch with recommended instance category, and then download and apply with `kubectl patch`.
    
    - After you have confirmed that the node affinity patches work as expected you can continue with enabling the feature and automatically deploying.