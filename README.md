# flask_5_tailwind
Gaining hands-on experience in video hosting, creating a Flask app styled with Tailwind CSS, and deploying it to a cloud platform. I will leverage CDN services in Google Cloud or Azure to optimize video delivery, ensuring a seamless user experience for viewers worldwide.

Flask App Link: https://mannflaskapp.azurewebsites.net/

## Design Rationale and Principles Followed
I used an online healthcare informatics program video for display on both the CDN and the Flask app.


## Azure Cloud CDN and Video Hosting


## Azure Cloud Deployment
I deployed the application using Azure App Services with the following steps:
1. To run the flask application via Azure App Service. Use the following command curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash to initiate Azure Cli package installation.

2. Then, in your Google Shell terminal, use the following commands az  and az login--use-device-code., type in "az." You are then going to click the URL from the terminal and enter the code to authenticate. Use your Stony Brook account and press continue. You can then exit out of that tab and go back to the Google Shell environment. You will see that you were successfully authenticated.

3. Then insert the command az account list --output table into your terminal. You are going to be given a list of different subscription IDs. To change this ID to the "Azure for Students" one, use the command az account set --subscription subscriptionId.

4.  Now, log into the Azure Web Portal and create a new resource group under the "Resource Groups" tab. Ensure your resource group is under the "Azure for Students" subscription and has a simple name with no white space and no special characters.

5. Then redirect to the Google Shell Environment and in the terminal use the command az group list.

6. To launch the azure web application, insert the command'''az webapp up --name-insert resource group here-flask --runtime PYTHON:3.9 --sku B1." You have to insert a preferred "name" and "resource group" name you created in your Azure account.

7. The terminal will then say that the webapp does not exist, and it will create the resource group and start the zip deployment process. (This process takes a few minutes)

8. You can now login into your Azure account and view your running wbepage URL under "App Services"


## Observations and Benefits of Using a CDN and Cloud Deployment
#### Content Delivery Networks (CDNs) offer several advantages, such as:
1. Improved Load Times: CDNs reduce latency and enhance loading speed by distributing content globally.

2. Global Reach: Content is delivered from the nearest server location, improving content delivery and reducing server load.

3. Enhanced Availability: CDNs provide redundancy and high availability, ensuring consistent access to resources.

4. Cost-Efficiency: CDNs optimize content delivery while reducing infrastructure costs.

5. Enhanced Security: CDNs offer security measures, including encryption and firewalls, to protect data.

#### Cloud deployment provides numerous benefits, such as:
1. Scalability: Cloud environments effortlessly adapt to varying workloads, making them well-suited for growing applications.

2. Cost Optimization: Cloud services follow a pay-as-you-go model, minimizing upfront investments and offering cost predictability.

3. High Reliability: Cloud platforms offer redundancy and high availability, reducing service interruptions and downtime.

4. Comprehensive Security: Cloud providers typically offer advanced security features, ensuring data and applications are well-protected.

5. User-Friendly Management: Cloud platforms provide intuitive interfaces for efficient resource management.

6. Continuous Enhancements: Cloud services regularly update applications and infrastructure to maintain security and functionality.


## Challenges Encountered.

While attempting to upload my healthcare informatics video to Github, I encountered an issue as the file size exceeded the 25 MB limit. Therefore, I had to compress the video. 

