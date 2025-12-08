

# ChatCompletionRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**model** | **String** | Model to use. |  |
|**frequencyPenalty** | **BigDecimal** | Number between -2.0 and 2.0. Positive values penalize new tokens based on their existing frequency in the text. |  [optional] |
|**logprobs** | **Boolean** | Whether to return log probabilities of the output tokens. |  [optional] |
|**maxTokens** | **Integer** | The maximum number of tokens that can be generated. |  [optional] |
|**messages** | [**List&lt;Message&gt;**](Message.md) | A list of messages comprising the conversation so far. |  |
|**presencePenalty** | **BigDecimal** | Number between -2.0 and 2.0. Positive values penalize appearance of new tokens. |  [optional] |
|**responseFormat** | [**ChatCompletionRequestResponseFormat**](ChatCompletionRequestResponseFormat.md) |  |  [optional] |
|**seed** | **Integer** | Seed for the random number generator. |  [optional] |
|**stop** | **List&lt;String&gt;** | Up to 4 sequences where the API will stop generating further tokens. |  [optional] |
|**stream** | **Boolean** | Whether to use streaming (SSE) when true. |  [optional] |
|**streamOptions** | [**ChatCompletionRequestStreamOptions**](ChatCompletionRequestStreamOptions.md) |  |  [optional] |
|**temperature** | **BigDecimal** | What sampling temperature to use, between 0 and 2. |  [optional] |
|**toolChoice** | [**ChatCompletionRequestToolChoice**](ChatCompletionRequestToolChoice.md) |  |  [optional] |
|**topLogprobs** | **Integer** | An integer between 0 and 5 specifying the number of most likely tokens to return per position. |  [optional] |
|**topP** | **BigDecimal** | Nucleus sampling parameter. |  [optional] |



