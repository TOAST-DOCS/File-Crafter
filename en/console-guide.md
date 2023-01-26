## Application Service > File Crafter > Console User Guide

You can request File Crafter service’s features via API ([API Guide](./api-guide.md)). You can only retrieve the features and process some of them in the console.

### 콘솔 아이콘
콘솔에서는 다양한 형태의 아이콘을 통해 정보와 기능을 제공합니다.

![](../image/icons.png)

1. 상세 항목
2. 재업로드
3. 내비게이션
4. 유효성 검사
5. 다운로드
6. Import 처리

### Export Request List

- You can make a query by applying query conditions.
    - Search key: You can make a query by using the search key sent when requesting to export.
    - Processing status
        - ALL: All
        - READY: Waiting for process
        - WORKING: Processing
        - COMPLETED: Completed
        - FAILED: Failed
- 상세 항목 아이콘을 클릭하여 요청 상세를 확인할 수 있습니다.
- 스토리지 업로드에 실패할 경우 재업로드 아이콘을 클릭하여 업로드를 다시 요청할 수 있습니다.

#### Details

- Details of the request can be found through scrolls.
    - Number of processed exports: You can check the number of processed exports requested. Large files over 10 KB are marked separately.
    - Expiration date: When uploading to a specified storage fails, the exported file is kept for 7 days and then deleted. You must request reupload before expiration date. (When uploading succeeds, it is immediately deleted.)
    - Password: A password specified upon request. You can release the exported fil with the specified password.
    - 스토리지 정보: 요청 시 지정한 스토리지 정보입니다. 여러 개의 스토리지를 지정한 경우 내비게이션 아이콘을 클릭해 확인할 수 있습니다.
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
- 유효성 검사가 포함된 요청은 해당 아이콘이 표시됩니다.
- 상세 항목 아이콘을 클릭하여 요청 상세를 확인할 수 있습니다.
- VALIDATED(유효성 검사 완료) 상태인 요청 건에 한해 검사 성공/실패 결과 파일을 내려받을 수 있는 다운로드 아이콘이 나타납니다.
- VALIDATED(유효성 검사 완료) 상태인 요청 건에 한해 Import 처리 아이콘이 나타납니다.

#### Details

- You can find the request details.
    - Expiration date: Imported files and validity check success and failure files are kept in 7 days and then deleted.
    - Password: When the file to be imported is encrypted and uploaded, File Crafter processes it using a password.
    - Validity check callback URL: A callback URL for validity check.
    - Data start row: The row number where the actual data of the imported file starts. It is used in files with multi-line headers.
    - Auto Import process: After validity check, the import operation continues without remaining in the VALIDATED status.
    - Processing result: You can find the processing result of the requested Import. Large files over 10 KB are marked separately.