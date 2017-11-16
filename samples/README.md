# Dialogflow API Java examples

These samples demonstrate the use of the [Dialogflow API][dialogflow].

These samples show how to detect intents with text, audio, and streaming audio.

These samples show how to manage contexts, entities, entity types, and intents

[dialogflow]: https://dialogflow.com/docs/getting-started/basics
[google-cloud-java]: https://github.com/GoogleCloudPlatform/google-cloud-java

## Java Version

This sample requires you to have
[Java8](https://docs.oracle.com/javase/8/docs/technotes/guides/install/install_overview.html).

### Download Maven

To get started, [download][maven-download] and [install][maven-install] it.

[maven]: https://maven.apache.org
[maven-download]: https://maven.apache.org/download.cgi
[maven-install]: https://maven.apache.org/install.html

### Setup

* Create a project with the [Google Cloud Console][cloud-console], and enable
  the [Dialogflow API][dialogflow-api].
* [Set up][auth] authentication. For
    example, from the Cloud Console, create a service account,
    download its json credentials file, then set the appropriate environment
    variable:

    ```bash
    export GOOGLE_APPLICATION_CREDENTIALS=/path/to/your-project-credentials.json
    ```
* To run tests, set GOOGLE_CLOUD_PROJECT to your PROJECT_ID:
  ```
  export GOOGLE_CLOUD_PROJECT=PROJECT_ID
  ```
  ```
  mvn clean verify
  ```
* Set PROJECT_ID in pom.xml to your Google Cloud Project Id.
* Set SESSION_ID in pom.xml to a session name of your choice. (Defaults to SESSION_ID)
* Set CONTEXT_ID in pom.xml to a context name of your choice. (Defaults to CONTEXT_ID)

[cloud-console]: https://console.cloud.google.com
[dialogflow-api]: https://pantheon.corp.google.com/apis/library/dialogflow.googleapis.com
[auth]: https://cloud.google.com/docs/authentication/getting-started

## Run the sample

To build the sample, we use Maven.

```bash
mvn clean package
```

### Set up the Agent
Import the sample agent (RoomReservation.zip) from the resources directory to your
[Dialogflow Project][dialogflow-import] using the following guide: 
[Versioning with Import/Export][import-export-versioning]

[dialogflow-import]: https://console.dialogflow.com/api-client/#/editAgent/
[import-export-versioning]: https://dialogflow.com/docs/best-practices/import-export-for-versions

## Samples

### Detect Intent Texts
DialogFlow API Detect Intent sample with text inputs.

```
mvn exec:java -DDetectIntentTexts
```

### Detect Intent Audio
DialogFlow API Detect Intent sample with audio files. Returns the result of detect intent with an
audio file as input.

Note: Execute the following commands in order to yield reasonable outputs.
```
mvn exec:java -DDetectIntentAudioBookARoom
```
```
mvn exec:java -DDetectIntentAudioMountainView
```
```
mvn exec:java -DDetectIntentAudioToday
```
```
mvn exec:java -DDetectIntentAudio230PM
```
```
mvn exec:java -DDetectIntentAudioHalfAnHour
```
```
mvn exec:java -DDetectIntentAudioTwoPeople
```

### Detect Intent Stream
DialogFlow API Detect Intent sample with audio files processes as an audio stream.

```
mvn exec:java -DDetectIntentStreamBookARoom
```
```
mvn exec:java -DDetectIntentStreamMountainView
```

### Context Management
DialogFlow API Context sample.

Lists contexts
```
mvn exec:java -DContextManagementList
```
Create an entity type
```
mvn exec:java -DContextManagementCreate
```
Delete entity type
```
mvn exec:java -DContextManagementDelete
```

### Entity Management
DialogFlow API Entity sample.

List entities
```
mvn exec:java -DEntityManagementList
```
Create an entity
```
mvn exec:java -DEntityManagementCreate
```
Delete entity
```
mvn exec:java -DEntityManagementDelete
```

### Entity Type Management
DialogFlow API EntityType sample.

List entity types
```
mvn exec:java -DEntityTypeManagementList
```
Create an entity type
```
mvn exec:java -DEntityTypeManagementCreate
```
Delete entity type
```
mvn exec:java -DEntityTypeManagementDelete
```

### Intent Management
DialogFlow API Intent sample.

List intents
```
mvn exec:java -DIntentManagementList
```
Create an intent
```
mvn exec:java -DIntentManagementCreate
```
Delete intent
```
mvn exec:java -DIntentManagementDelete
```

### Session Entity Type Management
DialogFlow API SessionEntityType sample.

List session entity types
```
mvn exec:java -DSessionEntityTypeManagementList
```
Create session entity type
```
mvn exec:java -DSessionEntityTypeManagementCreate
```
Delete session entity type
```
mvn exec:java -DSessionEntityTypeManagementDelete
```
