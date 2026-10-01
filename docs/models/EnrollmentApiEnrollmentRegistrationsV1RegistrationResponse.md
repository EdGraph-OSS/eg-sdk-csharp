# EdGraph.Platform.Client.Model.EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**TenantId** | **string** |  | [optional] 
**Pathway** | [**EnrollmentApiEnrollmentRegistrationsV1PathwayMessage**](EnrollmentApiEnrollmentRegistrationsV1PathwayMessage.md) |  | [optional] 
**CurrentScreenCode** | **string** |  | [optional] 
**Progress** | **string** | Decimal progress (0-100, 2dp) carried as an invariant-culture string,  mirroring the legacy enrollmentresults.proto completedProgress convention. | [optional] 
**LanguageCode** | **string** |  | [optional] 
**Contacts** | [**List&lt;EnrollmentApiEnrollmentRegistrationsV1RegistrationContactMessage&gt;**](EnrollmentApiEnrollmentRegistrationsV1RegistrationContactMessage.md) |  | [optional] [readonly] 
**Screens** | [**List&lt;EnrollmentApiEnrollmentRegistrationsV1RegistrationScreenMessage&gt;**](EnrollmentApiEnrollmentRegistrationsV1RegistrationScreenMessage.md) |  | [optional] [readonly] 
**CreatedBy** | **string** |  | [optional] 
**CreatedDateTime** | **string** |  | [optional] 
**LastModifiedBy** | **string** |  | [optional] 
**LastModifiedDateTime** | **string** |  | [optional] 
**DeletedBy** | **string** |  | [optional] 
**DeletedDateTime** | **string** |  | [optional] 
**IsDeleted** | **bool** |  | [optional] 
**Status** | **string** |  | [optional] 
**NextSchoolStateShortCode** | **string** |  | [optional] 
**NextSchoolName** | **string** |  | [optional] 
**Student** | [**EnrollmentApiEnrollmentRegistrationsV1RegistrationStudentMessage**](EnrollmentApiEnrollmentRegistrationsV1RegistrationStudentMessage.md) |  | [optional] 
**Applications** | [**List&lt;EnrollmentApiEnrollmentRegistrationsV1RegistrationApplicationMessage&gt;**](EnrollmentApiEnrollmentRegistrationsV1RegistrationApplicationMessage.md) |  | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

