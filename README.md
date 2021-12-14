
# Experiment for running Onenote add-in locally

## Install requirements:
- node version >=8.0+
- run
```npm install -g yo generator-office```
- run ```npm install``` at project root

## Running App

1. Go to [office on the web](https://office.live.com/). Using the Create option, make a document in OneNote. In this new document, select `Share` in the ribbon, select Copy Link.

2. Open the package.json file. Within the config section of this file, find "document" property. Paste the URL you copied as the value for the "document" property. For example, yours will look something like this:

```json 
"config": {
    "document": "<YOUR URL>",
    ...
  }
```
3. In the command line starting at the root directory of your project, run the following command as admin: 
```npm run start:desktop```
if it asks for loopback, press "yes". You may need to verify certificate, press "yes". 

4. Open your oneNote document you created earlier. There should be a button on the ribbon that says `Show Taskpane`. Press this button. This will open the side panel. You should see an iframe from windy.com as well as a run button. Press the `run` button will populate sample contents for the document. You can modify this in [taskpane.js](src\taskpane\taskpane.js) via the run() function

These steps are adapted from https://docs.microsoft.com/en-us/office/dev/add-ins/quickstarts/onenote-quickstart

additional instructions from: https://docs.microsoft.com/en-us/office/dev/add-ins/testing/sideload-office-add-ins-for-testing
