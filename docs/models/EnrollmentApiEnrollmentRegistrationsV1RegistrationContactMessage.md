# EdGraph.Platform.Client.Model.EnrollmentApiEnrollmentRegistrationsV1RegistrationContactMessage
One contact on a registration. id is the entry's own identity (minted once, never overwritten);  contactId is the EnrollmentContact record id the entry resolved to (the key every join goes  through; unset until resolved); externalDataSourceContactId is the SIS-side code, when known.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**ContactId** | **string** |  | [optional] 
**ContactName** | **string** |  | [optional] 
**ContactPhone** | **string** |  | [optional] 
**ContactEmail** | **string** |  | [optional] 
**ExternalDataSourceContactId** | **string** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

