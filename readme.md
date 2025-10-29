Create a static HTML web app in Azure

mkdir ICTbatch3 
cd $HOME/ICTbatch3
git clone https://github.com/Azure-Samples/html-docs-hello-world.git
cd html-docs-hello-world
•	az account list-locations –o table
az webapp up --location eastasia --name firstwebapp - -html
•	az provider register --namespace Microsoft.Web
•	az webapp up --location eastasia --name firstwebapp - -html
•	go to the app URL:http://.azurewebsites.net
•	nano index.html
•	Ctrl+O to save then Enter and Ctrl+X to exi
•	az webapp up --location eastasia --name firstwebapp - -html
•	Clean up resources
•	az group delete – name group_name


Create a PHP web app in Azure App Service

•	Open Command Prompt (CMD) or PowerShell on your computer.
cd C:\xampp\htdocs
git clone https://github.com/Azure-Samples/php-docs-hello-world
cd php-docs-hello-world
Start Apache in XAMPP (via XAMPP Control Panel).
navigate to the sample app at http://localhost/php-docs-hello-world
•	in cloud shell
az webapp deployment user set --user-name  arena3000 --password arena@123
az group create --name myResourceGroup --location eastasia
az appservice plan create --name myAppServicePlan --resource-group myResourceGroup --is-linux

az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name arenawebapp --runtime "PHP|8.2" --deployment-local-git
•	The URL of the Git remote is shown in the deploymentLocalGitUrl property
•	http:// arenawebapp.azurewebsites.net
•	in the local terminal window

git commit -a -m "My first commit"
git checkout -b my-feature 
git push -u origin my-feature 
git remote add azure deploymentLocalGitUrl
git push azure master
•	open the index.php file within the PHP app, and make a small change
•	In the local terminal window,
git commit -am "updated output" 
git push azure master

git config --global user.name "Your Name" 
git config --global user.email "your_email@example.com" 
