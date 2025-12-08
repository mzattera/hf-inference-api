

# EmbeddingsRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**model** | **String** | Model to use. |  |
|**input** | **List&lt;String&gt;** | Array of strings with inputs. |  |
|**normalize** | **Boolean** | If true, normalize embeddings. |  [optional] |
|**promptName** | **String** | The name of the prompt that should be used for encoding. |  [optional] |
|**truncate** | **Boolean** | Whether to truncate inputs |  [optional] |
|**truncationDirection** | [**TruncationDirectionEnum**](#TruncationDirectionEnum) |  |  [optional] |



## Enum: TruncationDirectionEnum

| Name | Value |
|---- | -----|
| LEFT | &quot;left&quot; |
| RIGHT | &quot;right&quot; |



