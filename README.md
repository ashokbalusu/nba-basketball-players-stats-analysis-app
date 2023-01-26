# Build and deploy

## Command to build the application. PLease remeber to change the project name and application name

gcloud builds submit --tag gcr.io/<ProjectName>/<AppName>  --project=<ProjectName>

### For example:
    <ProjectName> is "tt-project-374905"  -- Note that this is GCP project ID
    <AppName> is "tt" -- Note that this is GCP Cloud Run service name
#### Resulting command will be as below based on above example parameters:
gcloud builds submit --tag gcr.io/tt-project-374905/tt  --project=tt-project-374905


## Command to deploy the application

gcloud run deploy --image gcr.io/<ProjectName>/<AppName> --platform managed  --project=<ProjectName> --allow-unauthenticated

### For example: Resulting command will be as below based on above example parameters:
gcloud run deploy --image gcr.io/tt-project-374905/tt-project-374905 --platform managed  --project=tt-project-374905 --allow-unauthenticated




# GIt commands go add source files
## create a new repository on https://github.com/ashokbalusu
## open terminal/command prompt and run below commands (Assuming git already installed)
git init
git add .
git commit -m "initial commit"
git remote add origin https://github.com/ashokbalusu/nba-basketball-players-stats-analysis-app.git
git push -u origin master
