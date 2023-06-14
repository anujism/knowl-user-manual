---
title: Backend API
description: 
---



# api

## POST /napi/:pk/branch/create





Takes a primary key of document and a branch name and returns an the id of the new branched document.

 

**Parameters**







**Responses**

```javascript
{id: new_doc_id}
```

### Example:

```javascript
curl -XPOST 'https://staging-api.knowl.io/napi/4b5021dc-2c44-42b1-b6a8-cedcc1168a89/branch/create' --data '{"name":"BranchName"}' -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwiZXhwIjoxNjc1ODMxNzcyLCJpYXQiOjE2NzUyOTQwNTYsImp0aSI6ImZiMDhlMDFkMzBjODRlYjlhY2E4YjI1M2YyZTg0MjRkIiwidXNlcl9pZCI6IjJmY2JhYjViLTA3MmYtNGFmMC04Y2MxLTVmNTJjYzE1Zjk5MyIsImVtYWlsIjoia3Jpc2hhbnVAa25vd2wuaW8ifQ.SPfuu2UlHEVY1IHfsX443R7wSEO4t9yrDdxf-SAn3iM'
```



## POST /napi/:pk/branch/merge





Merge a branch with the main branch

Note that Merge always compares latest state of main branch. if main branch has a new node but side branch doesn't it will be deleted.



### Parameters

1. branch: In body, required



### Response:



```javascript
"status":"success"
```



Example

```javascript
 curl -X POST 'https://staging-api.knowl.io/napi/63921fc9-c9df-49d6-b9ff-43e64e7e5538/branch/merge'  -H "Content-Type: application/json"  -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwiZXhwIjoxNjc1OTM3ODM2LCJpYXQiOjE2NzU5MzQyMzYsImp0aSI6ImM3NTE1OGE2YzQwNTRhMGY5OWJkZTU1MmNmODg2ZDEzIiwidXNlcl9pZCI6IjJmY2JhYjViLTA3MmYtNGFmMC04Y2MxLTVmNTJjYzE1Zjk5MyIsImVtYWlsIjoia3Jpc2hhbnVAa25vd2wuaW8ifQ.93VSNd0mbTz_vjqURW4tKpAUc-DHO80G_P164wR6L3U' --data '{"branch":"c543e416-2ad3-45e7-97fa-1e4212dc152a"}' 

```





