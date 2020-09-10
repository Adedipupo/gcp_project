## Overview

In this lab, you become familiar with the Google Cloud web-based interface. There are two integrated environments: a GUI (graphical user interface) environment called the Cloud Console, and a CLI (command-line interface) called Cloud Shell. In this class you use both environment

## Objectives

In this lab, you learn how to perform the following tasks:

- Get access to Google Cloud.

- Create a Cloud Storage bucket using the Cloud Console.

- Create a Cloud Storage bucket using Cloud Shell.

- Become familiar with Cloud Shell features.

  

## Task 1: Create a bucket using the Cloud Console

gsutil mb gs://<BUCKET_NAME>

## Task 4: Explore more Cloud Shell features
## To Upload File

gsutil cp [MY_FILE] gs://[BUCKET_NAME]

## Task 5: Create a persistent state in Cloud Shell

## Identify available regions

gcloud compute regions list

## Create and verify an environment variable
INFRACLASS_REGION=[YOUR_REGION]

## Append the environment variable to a file

## 1. Create a subdirectory for materials used in this class:

mkdir infraclass

## 2. Create a file called config in the infraclass directory:

touch infraclass/config

## 3. Append the value of your Region environment variable to the config file:

echo INFRACLASS_REGION=$INFRACLASS_REGION >> ~/infraclass/config

## 4. Create a second environment variable for your Project ID, replacing [YOUR_PROJECT_ID] with your Project ID. You can find the project ID on the Cloud Console Home page.

INFRACLASS_PROJECT_ID=[YOUR_PROJECT_ID]

## 5. Append the value of your Project ID environment variable to the config file:

echo INFRACLASS_PROJECT_ID=$INFRACLASS_PROJECT_ID >> ~/infraclass/config

## 6. Use the source command to set the environment variables, and use the echo command to verify that the project variable was set:

source infraclass/config
echo $INFRACLASS_PROJECT_ID

## 7. Close and re-open Cloud Shell. Then issue the echo command again:

echo $INFRACLASS_PROJECT_ID

## Modify the bash profile and create persistence

## 1. Edit the shell profile with the following command:

nano .profile

## 2. Add the following line to the end of the file:

source infraclass/config

## 3. Press Ctrl+O, ENTER to save the file, and then press Ctrl+X to exit nano.

## 4. Use the echo command to verify that the variable is still set:

echo $INFRACLASS_PROJECT_ID

You should now see the expected value that you set in the config file.