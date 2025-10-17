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



20.231.246.122, 20.231.246.54, 40.121.19.105, 40.121.18.246, 40.121.18.166, 40.121.18.60, 40.121.18.21, 40.121.18.44, 40.121.18.41, 40.121.18.248, 40.121.18.82, 40.121.19.108, 20.231.247.19, 40.121.19.125, 40.121.18.46, 40.117.125.130, 40.121.18.52, 40.121.18.33, 40.121.18.238, 40.121.19.2, 40.121.19.122, 40.121.19.19, 40.121.18.114, 20.231.246.253, 40.121.18.255, 40.121.18.164, 40.117.121.106, 40.121.18.27, 40.121.18.156, 40.121.18.117, 40.121.18.197, 40.121.18.133, 40.121.18.112, 40.121.18.106, 20.241.227.6, 40.121.19.89, 40.121.19.83, 40.121.18.131, 40.121.18.201, 40.121.18.170, 40.121.18.242, 13.92.130.42, 40.121.19.42, 40.121.18.73, 40.121.18.43, 20.241.226.169, 51.8.12.17, 4.156.180.142, 20.242.162.124, 40.121.19.74, 40.121.19.40, 40.121.18.62, 40.121.18.244, 20.127.248.50, 20.241.171.30, 20.169.229.88, 20.169.229.46, 20.169.229.29, 20.169.229.38, 20.169.229.62, 20.169.229.109, 20.169.229.92, 20.169.229.27, 20.169.229.51, 20.169.229.42, 20.241.172.248, 48.216.192.198, 40.90.243.232, 40.90.242.126, 135.237.112.47, 51.8.74.190, 4.157.197.142, 172.210.91.191, 172.210.90.42, 40.90.243.227, 40.90.243.72, 20.241.172.250, 52.234.235.220, 57.152.55.92, 172.212.36.156, 172.210.121.45, 172.214.2.208, 51.8.15.68, 172.210.90.119, 134.33.213.81, 128.203.83.220, 20.241.192.93, 20.246.203.138, 172.212.121.150, 172.171.186.158, 52.249.213.152, 74.179.213.114, 4.246.239.152, 4.156.216.65, 4.157.231.174, 172.171.168.136, 20.185.213.14, 20.246.203.140, 13.82.216.169, 13.82.216.172, 13.82.216.149, 52.170.33.171, 57.152.61.92