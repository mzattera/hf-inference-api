

# ModelSearchRequest

Payload used to filter, sort, and paginate model results.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**search** | **String** | Filter based on substrings for repos and their usernames (e.g., &#39;resnet&#39;). |  [optional] |
|**author** | **String** | Filter models by an author or organization (e.g., &#39;huggingface&#39;). |  [optional] |
|**filter** | **String** | Filter based on tags (e.g., &#39;text-classification&#39;). |  [optional] |
|**sort** | **String** | Property to use when sorting (e.g., &#39;downloads&#39; or &#39;author&#39;). |  [optional] |
|**direction** | **Integer** | Direction in which to sort. Use -1 for descending, and 1 for ascending. |  [optional] |
|**limit** | **Integer** | Limit the number of models fetched. |  [optional] |
|**full** | **Boolean** | Whether to fetch most model data, such as all tags, the files, etc. |  [optional] |
|**config** | **Boolean** | Whether to also fetch the repo config. |  [optional] |



