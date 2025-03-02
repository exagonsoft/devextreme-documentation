---
id: dxFileUploader.abortUpload()
---
---
##### shortDescription
Cancels the file upload.

---

    <!-- tab: JavaScript -->
    var uploadControl = $("#uploaderContainer").dxFileUploader("instance");
    uploadControl.abortUpload()

[note]

The **abortUpload** method works differently in the following [upload modes](/api-reference/10%20UI%20Components/dxFileUploader/1%20Configuration/uploadMode.md '/Documentation/ApiReference/UI_Components/dxFileUploader/Configuration/#uploadMode'):

- **useForm**: The method is not supported in this mode.

- **useButtons**: Cancels the file upload and makes the file available for upload.  

- **instantly**: Cancels the file upload.

[/note]
