# A simple Angular that can be used for testing in various Cloud Platforms like Azure and Heroku. See the following directions for deploying an Angular application to Azure, AWS, Heroku, and Google Cloud.
This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 7.3.6.

## Development server
Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding
Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build and Testing
1. Run `ng build --base-href [APP_NAME]` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.
    * Use . if you want to deploy to the root directory of the web site
    * Use APP_NAME if you want to deploy to a URI of APP_NAME of the web site
2. Test the Angular App locally by using MAMP: Copy all the files under the dist directory to the MAMP htdocs directory

## Deployment to Cloud Platforms
## Azure
1. Create a new Web App (if new application)
    * Select the + Create a new Resource menu option.
    * Select Web App, select to Publish Code, select Node 10.x Runtime stack either Windows (required for Zip deploy) or Linux, and select a desired Region. Click Review + Create. Click Create.
    * After your new application deployment is finished click the application link to test out. Click go to Resource.
2. Open the Web App from the Dashboard
3. Deploy from a Build:
    1. Select Advanced Tools and click the Go link
    2. Select the Debug console->CMD menu options.
    3. Navigate to the site/wwwroot directory.
    4. Delete the default content.
    5. Zip up all the files under your files within the dist\APP_NAME directory. 
    6. Drag and drop the zip file onto the right side of the CMD window.		 
4. Deploy from a GIT CI/CD Build Pipeline:
    1. Select the Deployment Center menu option.
    2. Select the GitHub CI/CD type (authorize access if necessary) and click the Continue button.
    3. Select the GitHub Actions type and click the Continue button.
      * Fill in the GitHub Repository
      * Select the master branch
      * Select the Node.JS Runtime stack
      * Select the Node Version
      * Click the Finish button.
      * In the GitHub repo modify the GitHub build workflow file in the .guthub/workflows directory
        * Change the package: . entry to package: ./dist/[APP_NAME]
