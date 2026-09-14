# EdGraph.Platform.Client.Model.EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactEmailOverrideRequestDto
The body of an override write.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Value** | **string** | The corrected detail. The DELETE route removes an override instead; this is never blank. | [optional] 
**StudentId** | **string** | The student whose screen the edit was made from. Recorded on the history entry so it can be  filtered per student. It does NOT scope the override — every student linked to the contact shares  one corrected value. | [optional] 
**ExpectedVersion** | **string** | The &#x60;lastUpdatedDateTime&#x60; the client read, round-tripped back. When it no longer matches the  write is refused with 412 rather than winning because it arrived second. Omit to skip the check. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

