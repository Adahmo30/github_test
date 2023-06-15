# ecr-deployment
deploy to aws ecr
I had a few failed deployment to ecr
The first was the credentials, the terraform user doesn't have the authorization to perform the task
After I changed the user, by using the dfault credentials, it couldn't identify my dockerfile to build the image because I had the file within the ,github/workflows folder
I had to remove the Dockerfile and package.json files out of the .github/workflows folders for the runners to identify the files
It was a success at the end. The 'workflows' file can be in the .github/workflows folder and others outside to be identified and execute.
