# azure-website-deployment

## Steps:
1. az webapp deployment user set --user-name new312User051 --password new312User051
2. az group create --name nw312ResourceGroup --location westeurope
3. az appservice plan create --name nw312AppServicePlan --resource-group nw312ResourceGroup --sku FREE
4. az webapp create --name nw312app --resource-group nw312ResourceGroup --plan nw312AppServicePlan
5. az webapp config set --python-version 3.8  --name nw312app --resource-group nw312ResourceGroup
#local git 
6. az webapp deployment source config-local-git --name nw312app --resource-group nw312ResourceGroup --query url --output tsv

## git bash

1. git remote add azure https://nwUser123@philoapp.scm.azurewebsites.net/nw312app.git
2. git push azure master
