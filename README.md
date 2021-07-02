# DataScience-Course
AWARI Job Guarantee class

# Faz o build as imagens do app e frontend

If you don’t have a Microsoft Azure account or haven’t used it before, you can sign up for free. When you sign up for the first time you get a free credit for the first 30 days. You can utilize that credit to build and deploy a web app on Azure. Once you sign up, follow these steps:

- Login on https://portal.azure.com.
- Click on Create a Resource.
- Search for Container Registry and click on Create.
- Select Subscription, Resource group and Registry name (in our case: awarimask.azurecr.io is our registry name)
    
    ```
    # Faz o build as imagens do app e frontend
    $ sudo docker-compose -f api/docker-compose.yml build
    $ docker login pycaret.azurecr.io
    ```

You will be prompted for a Username and password. The username is the name of your registry (in this example username is “awarimask”). You can find your password under the Access keys of the Azure Container Registry resource you created.

``` # Configura a tag dentro do container registry
    $ docker tag api_app awarimask.azurecr.io/api_app
    # Faz o push da imagem no GCR
    $ docker push awarimask.azurecr.io/api_app

```   

