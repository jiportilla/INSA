# INSA Chatbot API Service

For details about using this service, see [Getting started with Watson Assistance](https://cloud.ibm.com/docs/assistant-data?topic=assistant-data-getting-started).

## Python API

**Note:** if you build your own Watson chatbot, update the `apikey` variable with your own Watson Assistant API information.
Set environment variables as recommended in [Authentication information](https://cloud.ibm.com/apidocs/assistant/assistant-v2?code=python#authentication) and then:

```
authenticator = IAMAuthenticator('{apikey}')
assistant = AssistantV2(
    version='{version}',
    authenticator=authenticator
)
```

## Testing with CURL

Replace `{apikey}` and `{url}` with your service credentials.

curl -X {request_method} -u "apikey:{apikey}" "{url}/v2/{method}"

For example:

```
curl -X POST -u "apikey:{apikey}" --header "Content-Type:application/json" --data "{\"input\": {\"text\": \"Hello\"}}" "{url}/v2/assistants/{assistant_id}/message?version=2021-06-14"
```