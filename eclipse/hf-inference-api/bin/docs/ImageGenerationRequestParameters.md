

# ImageGenerationRequestParameters

Optional parameters for image generation

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**guidanceScale** | **BigDecimal** | A higher guidance scale value encourages the model to generate images closely linked to the text prompt, but values too high may cause saturation and other artifacts. |  [optional] |
|**negativePrompt** | **String** | A prompt to guide what NOT to include in image generation. |  [optional] |
|**numInferenceSteps** | **Integer** | The number of denoising steps. More steps → higher quality image at expense of slower inference. |  [optional] |
|**width** | **Integer** | The width in pixels of the output image |  [optional] |
|**height** | **Integer** | The height in pixels of the output image |  [optional] |
|**scheduler** | **String** | Override the scheduler with a compatible one. |  [optional] |
|**seed** | **Integer** | Seed for the random number generator. |  [optional] |



