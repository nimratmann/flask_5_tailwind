# flask_5_tailwind
Gaining hands-on experience in video hosting, creating a Flask app styled with Tailwind CSS, and deploying it to a cloud platform. I will leverage CDN services in Google Cloud or Azure to optimize video delivery, ensuring a seamless user experience for viewers worldwide.

Flask App Link: https://mannflaskapp.azurewebsites.net/

## Design Rationale and Principles Followed
I used an online healthcare informatics program video for display on both the CDN and the Flask app.


## Azure Cloud CDN and Video Hosting
1. Sign in to Azure Portal: Access the Azure Portal using this link: https://azure.microsoft.com/en-us/get-started/azure-portal 
2. Create a Storage Account:
- Utilize the Search bar to find and select "Storage Accounts."
- Choose to either use an existing resource group or create a new one.
- Define a unique storage account name and proceed with the creation.
3. Configure Storage Account:
- After creating the storage account, navigate to the left-side menu and select or search for "Overview."
- Under the Security section, ensure the following options are enabled: "Allow Blob Anonymous," "Secure Transfer Required," and "Allow Storage Account Key Access." Save your settings.
4. Set Up a Container:
- Access the left-side menu and select or search for "Containers."
- Create a new container, assigning a name and adjusting the anonymous access to "Container (Anonymous read access for containers and blobs)." Complete the creation.
5. Upload Content:
- Within the chosen container, upload a file of your choice.
- Open the uploaded file to retrieve the associated URL, as you will need it for your code.
6. Configure Azure CDN:
- Access the left-side menu and select or search for "Security and Networking."
- Within this section, locate "Front Door and CDN" and select it.
- Choose "Azure CDN" as the service type and proceed to create the profile and endpoint names.
- Adjust the query string setting to "Ignore Query String" and finalize the creation.
7. Copy CDN Endpoint URL:
- Once the CDN endpoint is created, open it.
- Click on the hostname and then the endpoint hostname.
- Copy the URL provided.
8. Combine URLs:
- Merge the hostname and container URLs by copying the part of the URL from the container that comes after ".net."
- Append this to the end of the hostname URL.
By following these steps, you'll be able to seamlessly integrate your Azure storage account and CDN into your application.


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
1. Faster Load Times: CDNs improve website loading speed by distributing content globally, minimizing delays.
2. Wider Audience Reach: Content is delivered from the nearest server location, ensuring efficient content delivery and less strain on servers.
3. Reliable Access: CDNs offer redundancy and high availability, ensuring resources are consistently accessible.
4. Cost-Effective: CDNs optimize content delivery while reducing infrastructure expenses.
5. Enhanced Data Protection: CDNs incorporate security features like encryption and firewalls to safeguard data.

#### Cloud deployment provides numerous benefits, such as:
1. Scalability: Cloud environments easily adjust to varying workloads, making them ideal for expanding applications.
2. Financial Efficiency: Cloud services follow a pay-as-you-go model, reducing initial investments and providing cost predictability.
3. Dependable Service: Cloud platforms provide redundancy and high availability, minimizing service disruptions and downtime.
4. Robust Security: Cloud providers typically offer advanced security measures to protect data and applications.
5. Intuitive Management: Cloud platforms feature user-friendly interfaces for streamlined resource management.
6. Continuous Improvement: Cloud services regularly update applications and infrastructure to maintain security and functionality.


## Challenges Encountered.

While attempting to upload my healthcare informatics video to Github, I encountered an issue as the file size exceeded the 25 MB limit. Therefore, I had to compress the video. 

