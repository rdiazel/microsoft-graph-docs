---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := msgraphsdk.New()
clientContext := "clientContext-value"
requestBody.SetClientContext(&clientContext)
options := &msgraphsdk.CancelMediaProcessingRequestBuilderPostOptions{
	Body: requestBody,
}
callId := "call-id"
result, err := graphClient.Communications().CallsById(&callId).CancelMediaProcessing().Post(options)


```