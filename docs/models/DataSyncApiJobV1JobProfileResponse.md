# EdGraph.Platform.Client.Model.DataSyncApiJobV1JobProfileResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TenantId** | **string** |  | [optional] 
**JobId** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**JobTypeId** | **string** |  | [optional] 
**JobTypeName** | **string** |  | [optional] 
**SourceConnectionId** | **string** |  | [optional] 
**DestinationConnectionId** | **string** |  | [optional] 
**ProfileId** | **string** |  | [optional] 
**ProfileName** | **string** |  | [optional] 
**ApplicationId** | **string** |  | [optional] 
**JobPoints** | **int** |  | [optional] 
**DataRefreshType** | **DataSyncApiJobV1DataRefreshType** |  | [optional] 
**DataRefreshSpecificDate** | **string** |  | [optional] 
**MaxApiFailure** | **int** |  | [optional] 
**MaxApiRetry** | **int** |  | [optional] 
**JobCompleteCallbackUrl** | **string** |  | [optional] 
**JobMetadata** | [**List&lt;DataSyncApiJobV1JobMetadata&gt;**](DataSyncApiJobV1JobMetadata.md) |  | [optional] [readonly] 
**Schedule** | [**DataSyncApiJobV1Schedule**](DataSyncApiJobV1Schedule.md) |  | [optional] 
**NotificationEmails** | **List&lt;string&gt;** |  | [optional] [readonly] 
**JobStatus** | **DataSyncApiJobV1JobStatus** |  | [optional] 
**JobExecutionId** | **string** |  | [optional] 
**JobExecutionStatus** | **DataSyncApiJobV1JobExecutionStatus** |  | [optional] 
**JobExecutionStartDateTime** | **string** |  | [optional] 
**JobExecutionEndDateTime** | **string** |  | [optional] 
**Metrics** | [**List&lt;DataSyncApiJobV1Metric&gt;**](DataSyncApiJobV1Metric.md) |  | [optional] [readonly] 
**ChildJobs** | [**List&lt;DataSyncApiJobV1ChildJob&gt;**](DataSyncApiJobV1ChildJob.md) |  | [optional] [readonly] 
**CreatedBy** | **string** |  | [optional] 
**CreatedDateTime** | **string** |  | [optional] 
**LastModifiedBy** | **string** |  | [optional] 
**LastModifiedDateTime** | **string** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

