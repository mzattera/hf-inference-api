# DefaultApi

All URIs are relative to *https://router.huggingface.co*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**chatCompletion**](DefaultApi.md#chatCompletion) | **POST** /v1/chat/completions | Chat completion using messages |
| [**featureExtraction**](DefaultApi.md#featureExtraction) | **POST** /{provider}/v1/embeddings | Get embeddings for input(s) |
| [**textToImage**](DefaultApi.md#textToImage) | **POST** /{provider}/v1/images/generations | Text to Image generation |


<a id="chatCompletion"></a>
# **chatCompletion**
> ChatCompletionResponse chatCompletion(chatCompletionRequest)

Chat completion using messages

### Example
```java
// Import classes:
import io.github.mzattera.hfinferenceapi.ApiClient;
import io.github.mzattera.hfinferenceapi.ApiException;
import io.github.mzattera.hfinferenceapi.Configuration;
import io.github.mzattera.hfinferenceapi.auth.*;
import io.github.mzattera.hfinferenceapi.models.*;
import io.github.mzattera.hfinferenceapi.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://router.huggingface.co");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    ChatCompletionRequest chatCompletionRequest = new ChatCompletionRequest(); // ChatCompletionRequest | 
    try {
      ChatCompletionResponse result = apiInstance.chatCompletion(chatCompletionRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#chatCompletion");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **chatCompletionRequest** | [**ChatCompletionRequest**](ChatCompletionRequest.md)|  | |

### Return type

[**ChatCompletionResponse**](ChatCompletionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Chat completion response |  -  |
| **400** | Bad request — invalid input |  -  |
| **401** | Unauthorized — invalid or missing token |  -  |

<a id="featureExtraction"></a>
# **featureExtraction**
> EmbeddingsResponse featureExtraction(provider, embeddingsRequest)

Get embeddings for input(s)

### Example
```java
// Import classes:
import io.github.mzattera.hfinferenceapi.ApiClient;
import io.github.mzattera.hfinferenceapi.ApiException;
import io.github.mzattera.hfinferenceapi.Configuration;
import io.github.mzattera.hfinferenceapi.auth.*;
import io.github.mzattera.hfinferenceapi.models.*;
import io.github.mzattera.hfinferenceapi.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://router.huggingface.co");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String provider = "provider_example"; // String | The specific inference provider.
    EmbeddingsRequest embeddingsRequest = new EmbeddingsRequest(); // EmbeddingsRequest | 
    try {
      EmbeddingsResponse result = apiInstance.featureExtraction(provider, embeddingsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#featureExtraction");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **provider** | **String**| The specific inference provider. | |
| **embeddingsRequest** | [**EmbeddingsRequest**](EmbeddingsRequest.md)|  | |

### Return type

[**EmbeddingsResponse**](EmbeddingsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Embeddings computed successfully |  -  |
| **400** | Bad request — invalid input |  -  |
| **401** | Unauthorized — invalid or missing token |  -  |

<a id="textToImage"></a>
# **textToImage**
> ImageGenerationResponse textToImage(provider, imageGenerationRequest)

Text to Image generation

### Example
```java
// Import classes:
import io.github.mzattera.hfinferenceapi.ApiClient;
import io.github.mzattera.hfinferenceapi.ApiException;
import io.github.mzattera.hfinferenceapi.Configuration;
import io.github.mzattera.hfinferenceapi.auth.*;
import io.github.mzattera.hfinferenceapi.models.*;
import io.github.mzattera.hfinferenceapi.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://router.huggingface.co");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String provider = "provider_example"; // String | The specific inference provider.
    ImageGenerationRequest imageGenerationRequest = new ImageGenerationRequest(); // ImageGenerationRequest | 
    try {
      ImageGenerationResponse result = apiInstance.textToImage(provider, imageGenerationRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#textToImage");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **provider** | **String**| The specific inference provider. | |
| **imageGenerationRequest** | [**ImageGenerationRequest**](ImageGenerationRequest.md)|  | |

### Return type

[**ImageGenerationResponse**](ImageGenerationResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Generated image(s) returned as Base64 encoding in the response. |  -  |
| **400** | Bad request — invalid input |  -  |
| **401** | Unauthorized — invalid or missing token |  -  |

