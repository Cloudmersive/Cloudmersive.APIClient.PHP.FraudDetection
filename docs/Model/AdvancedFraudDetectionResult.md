# AdvancedFraudDetectionResult

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**successful** | **bool** | True if successful, false otherwise | [optional] 
**clean_result** | **bool** | True if the document is clean, false if fraud threats were found | [optional] 
**fraud_risk_level** | **double** | Overall fraud risk level between 0.0 and 1.0 | [optional] 
**contains_financial_liability** | **bool** | True if the document contains financial liability | [optional] 
**contains_sensitive_information_collection** | **bool** | True if the document contains sensitive data collection from the recipient | [optional] 
**contains_asset_transfer** | **bool** | True if the document contains an asset transfer | [optional] 
**contains_purchase_agreement** | **bool** | True if the document contains a purchase agreement | [optional] 
**contains_employment_agreement** | **bool** | True if the document contains an employment agreement | [optional] 
**analysis_rationale** | **string** | Rationale on why the document was classified as such | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


