https://railway.com/deploy/SicyT1?referralCode=hoN-Mz

Here are the consolidated instructions for deploying n8n on Azure Container Apps, including the updates from the community comments.

### Step 1: Set Up the Container App
1.  Navigate to the Azure Portal and search for **Container App**, then select **Create**.
2.  Choose your subscription and either select an existing resource group or create a new one.
3.  Name your container app (e.g., "n8n-container") and select the desired region.
4.  In the container setup section, choose **Container Image** as the source and select **Docker Hub**.
5.  For the image name, enter `n8nio/n8n:latest`.
6.  Configure the CPU and memory. A good starting point is **1 CPU** and **2GB of memory**. You can select either the **Consumption** or a **Fixed Workload** plan.

### Step 2: Set Environment Variables
Configure the following environment variables in your container app's settings to ensure proper security and functionality.

*   **N8N_ENCRYPTION_KEY:** A strong, unique key to secure sensitive credential data.
*   **GENERIC_TIMEZONE:** Your preferred timezone (e.g., "America/New_York").
*   **WEBHOOK_URL:** The publicly accessible URL for your n8n instance. This can be the URL provided by Azure or a custom domain.
*   **N8N_HOST:** Your domain name without the "https://". This ensures user invitation links are generated correctly.
*   **TRUST_PROXY:** Set this value to `true`.
*   **N8N_BASIC_AUTH:** Set up basic authentication credentials for initial access.
*   **N8N_ENFORCE_SETTINGS_FILE_PERMISSIONS:** Set this value to `true` for enhanced security.

For connecting to a PostgreSQL database, add these additional variables:
*   **DB_TYPE:** Set to `postgres`.
*   **DB_HOST:** The hostname or IP address of your PostgreSQL database server.
*   **DB_PORT:** The port for your PostgreSQL database (typically `5432`).
*   **DB_DATABASE:** The name of the database.
*   **DB_USER:** Your PostgreSQL username.
*   **DB_PASSWORD:** Your PostgreSQL password.

### Step 3: Enable Ingress
To make your n8n instance accessible from the internet, you must configure the ingress settings.

1.  Navigate to the **Ingress** section of your container app.
2.  Set Ingress to **Enabled**.
3.  Allow traffic from **Anywhere**.
4.  Set the Target port to `5678`, which is the default port for n8n.
5.  Enable **HTTP transport auto**.

### Step 4: Configure Database Networking
If you are using an Azure for PostgreSQL database, you need to allow your container app to connect to it.

1.  In your container app's settings, go to **Custom Domains** to find your container's outbound IP address.
2.  In the Azure portal, navigate to your PostgreSQL instance and select **Networking**.
3.  Add a new firewall rule. Use the container's IP address you found as both the start and end IP to grant it access.

### Step 5: Review and Create
After confirming all settings are correct, click **Create**. Azure will provision and deploy your n8n instance. Once the deployment is complete, your instance will be live and ready for use.

[1](https://community.n8n.io/t/deploy-n8n-on-azure-container-apps/71010)