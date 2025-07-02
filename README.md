# MarketPeak_Ecommerce

Steps taken to deploy the entire flow of the project:

1. Created MarketPeak_Ecommerce directory and initialized Git Repository
![](./img/1.Initialize_Git_Repository.PNG)

2. Obtained and prepared the E-commerce website template. Extracted the downloaded template into the MarketPeak_Ecommerce directory.
![](./img/2.E-commerce_website_template.PNG)

3. Staged and commit the template to Git
![](./img/3.Stage_and_commit_the_template.PNG)

4. Pushed the code to my GitHub repository.
Created a remote repository on GitHub
![](./img/4.Created_Remote_Repository.PNG)

Linked the local repository to GitHub using git remote add command
![](./img/5.Linked_local_repository_to_GitHub.PNG)

Uploaded the local repository to GitHub using git push -u command.
![](./img/6.Upload_local_repository_to_GitHub.PNG)

5. Set up AWS EC2 instance.
Logged in to AWS management console and launched an EC2 instance using Amazon Linux AMI.
![](./img/7.Created_EC2_Instance.PNG)

Connected to the instance using ssh
![](./img/8.Connected_to_Instance.PNG)

6. Clone the GitHub repository to the AWS instance.
Generated ssh keypair using ssh-keygen
![](./img/9.ssh-keygen.PNG)

Added ssh public keypair using ssh-keygen
![](./img/10.ssh_key_linked_to_GitHub.PNG)

Error Encountered: (-bash: git:command not found). I encountered this error so I had to install Git in my EC2 instance using yum command.
![](./img/11.Install_git.PNG)

7. Installes Apache web server
![](./img/12.Installed_Apache_server.PNG)

Then I started and enabled Apache
![](./img/13.Start_Apache.PNG)

8. Configured httpd for the website, and cleared the default httpd web directory /var/www/html/
![](./img/14.Configured_httpd.PNG)

Then I copied MarketPeak_Ecommerce to the httpd web directory.

Finally I reloaded httpd and tested the website using the EC2 public ip address.