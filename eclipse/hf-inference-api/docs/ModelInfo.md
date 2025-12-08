

# ModelInfo

Detailed information about a single model from the Hub.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique identifier of the model repository (format - author/name). |  |
|**likes** | **Integer** | Number of likes received by the model. |  [optional] |
|**trendingScore** | **Integer** | Score indicating the current popularity or trending status. |  [optional] |
|**_private** | **Boolean** | Whether the model repository is private (true) or public (false). |  [optional] |
|**downloads** | **Integer** | Total number of downloads for the model. |  [optional] |
|**tags** | **List&lt;String&gt;** | List of tags associated with the model (e.g., library, task, license). |  [optional] |
|**pipelineTag** | **String** | Primary task supported by the model. |  [optional] |
|**libraryName** | **String** | Main machine learning library used by the model. |  [optional] |
|**createdAt** | **OffsetDateTime** | Timestamp when the model was created. |  [optional] |
|**modelId** | **String** | Alternative or redundant field for the unique model identifier. |  [optional] |



