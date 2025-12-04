# hf-inference-api

A OpenAPI-generated client for Hugging Face inference API.

As the API documentation is in contrast with actual implementation, this is a best effort to have something up and running.

For the time being, this covers only Chat Completion, Feature Extraction (embeddings), and Text to Image APIs.

## How to Build

The `eclipse` folder contains an Eclipse workbench for the project; it consists of two Maven projects:

### hf-client-api-generator

This contains a `pom.xml` to configure and run the OpenAPI generator. Right click and use `Run As > Maven generate-sources` to (re)generate API code accordingly to the provided `openapi.yaml`.

### hf-inference-api

This is a Maven project that is automatically created by the OpenAPI generator.

Please notice the generator is not deleting any existing file upon re-generation and that JUnit test provided will not be overwritten.

## How to Use

Simple test code in [DeafaultApiTest.java](https://github.com/mzattera/hf-inference-api/tree/master/eclipse/hf-inference-api/src/test/java/io/github/mzattera/hfinferenceapi/client/api) shows basic usage of the API, which is detailed in the `openapi.yaml` file.

 	


