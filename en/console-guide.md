## Application Service > File Crafter > Console User Guide

You can request File Crafter service’s features via API ([API Guide](./api-guide.md)). You can only retrieve the features and process some of them in the console.

### Export Request List

- You can make a query by applying query conditions.
    - Search key: You can make a query by using the search key sent when requesting to export.
    - Processing status
        - ALL: All
        - READY: Waiting for process
        - WORKING: Processing
        - COMPLETED: Completed
        - FAILED: Failed
- You can see the details of request by clicking the icon of details ![](../image/new_window.png).
- When storage upload has failed, you can request reupload by clicking the reupload icon ![](../image/move.png).

#### Details

- Details of the request can be found through scrolls.
    - Number of processed exports: You can check the number of processed exports requested. Large files over 10 KB are marked separately.
    - Expiration date: When uploading to a specified storage fails, the exported file is kept for 7 days and then deleted. You must request reupload before expiration date. (When uploading succeeds, it is immediately deleted.)
    - Password: A password specified upon request. You can release the exported fil with the specified password.
    - Storage information: The information on storage specified upon request. When you specify multiple storage, you can find the information through the navigation icon![](../image/nav_arrow_left.png) ![.
    - Query parameter, extraction field, sheet: Additional information transmitted to the specified callback API URL upon request.

### Import Request List

- You can make a query by applying query conditions.
    - Search key: You can make a query by using the search key sent when requesting to import.
    - Processing status
        - ALL: All
        - FAILED: Failed
        - IMPORTED: Completed
        - IMPORTING: Processing
        - VALIDATED: Validity check completed
        - VALIDATING: Validating
        - READY: Waiting for process
- Requests that contain validity check are displayed with a separate icon![](../image/green_check.png).
- You can see the details of request by clicking the icon of details ![](../image/new_window.png).
- For requests in a VALIDATED status (validity check completed), an icon ![](../image/download.png) is displayed to download a file of check results indicating success and failure.
- For requests in a VALIDATED status (validity check completed), an icon to process Import ![](../image/play.png) is displayed.

#### Details

- You can find the request details.
    - Expiration date: Imported files and validity check success and failure files are kept in 7 days and then deleted.
    - Password: When the file to be imported is encrypted and uploaded, File Crafter processes it using a password.
    - Validity check callback URL: A callback URL for validity check.
    - Data start row: The row number where the actual data of the imported file starts. It is used in files with multi-line headers.
    - Auto Import process: After validity check, the import operation continues without remaining in the VALIDATED status.
    - Processing result: You can find the processing result of the requested Import. Large files over 10 KB are marked separately.