---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)

requestBody := graphmodels.NewEdiscoveryCase()
displayName := "My Case 1 - Renamed"
requestBody.SetDisplayName(&displayName) 
description := "Updated description"
requestBody.SetDescription(&description) 

result, err := graphClient.Security().Cases().EdiscoveryCasesById("ediscoveryCase-id").Patch(context.Background(), requestBody, nil)


```