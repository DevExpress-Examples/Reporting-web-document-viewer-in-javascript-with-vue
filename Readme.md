<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/228656974/23.2.3%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/T848267)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
[![](https://img.shields.io/badge/💬_Leave_Feedback-feecdd?style=flat-square)](#does-this-example-address-your-development-requirementsobjectives)
<!-- default badges end -->
# Reporting for Vue - How to Integrate Web Document Viewer

This example consists of two parts: 

- A server (back-end) ASP.NET Core project that enables [cross-domain requests (CORS)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) (Access-Control-Allow-Origin) and implements a custom web report storage.

- An Vue JavaScript Framework front-end client application.

Perform the following steps to run this example:

1. Open the back-end project solution (*ServerSide/ServerSide.sln*) in Visual Studio and run the project.
2. Navigate to the *vue-report-viewer* folder that is the client part's root folder.
3. Open the console and run the following command:

    ```npm install```
4. Run the command to compile and start the client part:

    ```npm run serve```

5. Point your browser to `http://localhost:8080/` to see the result.

> [!TIP]
> Make sure that the backend application runs on the port specified in the host setting of the Document Viewer component. For more information, refer to the following help topic: [Determine the Host URL](https://docs.devexpress.com/XtraReports/400197/web-reporting/asp-net-core-reporting/server-side-configuration/document-viewer-server-side-configuration-asp-net-core#step-3-determine-the-host-url).

![](Images/screenshot.png)

## Files to Review

- [WebDocumentViewer.vue](vue-report-viewer/src/components/WebDocumentViewer.vue)
- [main.js](vue-report-viewer/src/main.js)
- [HomeController.cs](ServerSideApp/ServerSideApp/Controllers/HomeController.cs)
- [CustomReportStorageWebExtension.cs](ServerSideApp/ServerSideApp/Services/CustomReportStorageWebExtension.cs)
- [Program.cs](ServerSideApp/ServerSideApp/Program.cs)

## Documentation

- [Document Viewer Integration in Vue](https://docs.devexpress.com/XtraReports/401539)
<!-- feedback -->
## Does this example address your development requirements/objectives?

[<img src="https://www.devexpress.com/support/examples/i/yes-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=reporting-vue-integrate-web-document-viewer&~~~was_helpful=yes) [<img src="https://www.devexpress.com/support/examples/i/no-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=reporting-vue-integrate-web-document-viewer&~~~was_helpful=no)

(you will be redirected to DevExpress.com to submit your response)
<!-- feedback end -->
