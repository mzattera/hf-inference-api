# hf-inference-api

A OpenAPI-generated client for Hugging Face inference API.

As the online API documentation is in contrast with actual implementation, this is a best effort to have something up and running.

For the time being, this covers only Chat Completion, Feature Extraction (embeddings), and Text to Image APIs.


## How to Install

The library is available as a Maven dependency:

```
<dependency>
  <groupId>io.github.mzattera</groupId>
  <artifactId>hf-inference-api</artifactId>
  <version>2.0.0</version>
</dependency>	
```


## How to Use

Simple test code in [DeafaultApiTest.java](https://github.com/mzattera/hf-inference-api/tree/master/eclipse/hf-inference-api/src/test/java/io/github/mzattera/hfinferenceapi/client/api) shows basic usage of the API, which is detailed in the `openapi.yaml` file.


## How to Build

The `eclipse` folder contains an Eclipse workbench for the project; it consists of two Maven projects:

### hf-client-api-generator

This contains a `pom.xml` to configure and run the OpenAPI generator. 

  * Right click and use `Run As > Maven generate-sources` to (re)generate API code accordingly to the provided `openapi.yaml`.
  
  * Right click onto newly (re)generated `hf-inference-api` project and `Refresh` then `Maven > Update Project...` to have generated API client built.
  
  * Replace `pom.xml` in (re)generated `hf-inference-api` with the one available in the repo; this because the `pom.xml` has been changed to support publishing to Maven repository. Be mindful to update the version for the generated artifact.

Upon major changes to the API, it is advised to delete content of `hf-inference-api` before generation, as the generator normally overwrites only some of the existing files and it never deletes files.

Note for Eclipse users: in some cases, after a `Maven > Update Project...` it might be necessary to close and reopen the project to fix compilation errors.

### hf-inference-api

This is a Maven project that is automatically created by the OpenAPI generator, as explained above.

Please notice the generator is not deleting any existing file upon re-generation and that JUnit test provided will not be overwritten.

 	


