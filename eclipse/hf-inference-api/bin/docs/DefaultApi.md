# DefaultApi

All URIs are relative to *https://router.huggingface.co/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createChatCompletion**](DefaultApi.md#createChatCompletion) | **POST** /chat/completions | Chat completion using messages |
| [**createEmbeddings**](DefaultApi.md#createEmbeddings) | **POST** /{provider}/v1/embeddings | Get embeddings for input(s) |
| [**createImage**](DefaultApi.md#createImage) | **POST** /images/completions | Text to Image generation |


<a id="createChatCompletion"></a>
# **createChatCompletion**
> ChatCompletionResponse createChatCompletion(chatCompletionRequest)

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
    defaultClient.setBasePath("https://router.huggingface.co/v1");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    ChatCompletionRequest chatCompletionRequest = new ChatCompletionRequest(); // ChatCompletionRequest | 
    try {
      ChatCompletionResponse result = apiInstance.createChatCompletion(chatCompletionRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createChatCompletion");
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

<a id="createEmbeddings"></a>
# **createEmbeddings**
> List&lt;List&lt;BigDecimal&gt;&gt; createEmbeddings(provider, embeddingsRequest)

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
    defaultClient.setBasePath("https://router.huggingface.co/v1");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    String provider = "provider_example"; // String | The specific inference provider.
    EmbeddingsRequest embeddingsRequest = new EmbeddingsRequest(); // EmbeddingsRequest | 
    try {
      List<List<BigDecimal>> result = apiInstance.createEmbeddings(provider, embeddingsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createEmbeddings");
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

[**List&lt;List&lt;BigDecimal&gt;&gt;**](List.md)

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

<a id="createImage"></a>
# **createImage**
> File createImage(imageGenerationRequest)

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
    defaultClient.setBasePath("https://router.huggingface.co/v1");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    ImageGenerationRequest imageGenerationRequest = new ImageGenerationRequest(); // ImageGenerationRequest | 
    try {
      File result = apiInstance.createImage(imageGenerationRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#createImage");
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
| **imageGenerationRequest** | [**ImageGenerationRequest**](ImageGenerationRequest.md)|  | |

### Return type

[**File**](File.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/octet-stream

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Generated image returned as raw bytes |  -  |
| **400** | Bad request — invalid input |  -  |
| **401** | Unauthorized — invalid or missing token |  -  |

