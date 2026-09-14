# EdGraph.Platform.Client.Model.EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**TenantId** | **string** |  | [optional] 
**ApplicationPathway** | [**EnrollmentApiEnrollmentApplicationResponsesV1ApplicationPathwayMessage**](EnrollmentApiEnrollmentApplicationResponsesV1ApplicationPathwayMessage.md) |  | [optional] 
**CurrentScreenCode** | **string** |  | [optional] 
**Progress** | **string** | Decimal progress (0-100, 2dp) carried as an invariant-culture string,  mirroring the legacy enrollmentresults.proto completedProgress convention. | [optional] 
**StudentId** | **string** |  | [optional] 
**LanguageCode** | **string** |  | [optional] 
**Contacts** | [**List&lt;EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseContactMessage&gt;**](EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseContactMessage.md) |  | [optional] [readonly] 
**Screens** | [**List&lt;EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseScreenMessage&gt;**](EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseScreenMessage.md) |  | [optional] [readonly] 
**CreatedBy** | **string** |  | [optional] 
**CreatedDateTime** | **string** |  | [optional] 
**LastModifiedBy** | **string** |  | [optional] 
**LastModifiedDateTime** | **string** |  | [optional] 
**DeletedBy** | **string** |  | [optional] 
**DeletedDateTime** | **string** |  | [optional] 
**IsDeleted** | **bool** |  | [optional] 
**Status** | **string** |  | [optional] 
**StudentFirstName** | **string** |  | [optional] 
**StudentLastName** | **string** |  | [optional] 
**StudentLocalId** | **string** |  | [optional] 
**NextSchoolCode** | **string** |  | [optional] 
**NextSchoolName** | **string** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

