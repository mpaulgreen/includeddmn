
- Request Method
    - POST
- Request URI
```
http://localhost:8080/kie-server/services/rest/server/containers/first_1.0.0-SNAPSHOT/dmn
```
- Request Body
```
{
   "model-namespace":"https://kiegroup.org/dmn/_74683546-B1D7-4A6C-86C6-4A2268546C77",
   "model-name":"ConsolidatedDMN",
   "decision-name":[
      
   ],
   "decision-id":[
      
   ],
   "dmn-context":{
       "by":{
        "BankingYears":3,
        "BankingYearsThreshold 1":5,
        "BankingYearsThreshold 2":10,
        "BankingYearsThreshold 3":15
       },
       "cs" :{
        "Credit Score":3,
        "Credit Score Threshold 1":5,
        "Credit Score Threshold 2":10,
        "Credit Score Threshold 3":15
       },
       "op" : {
        "OperationYears":3,
        "OperationYearsThreshold 1":5,
        "OperationYearsThreshold 2":10,
        "OperationYearsThreshold 3":15
       }
   }
}
  
```

- Result
```
{
  "type" : "SUCCESS",
  "msg" : "OK from container 'first_1.0.0-SNAPSHOT'",
  "result" : {
    "dmn-evaluation-result" : {
      "messages" : [ ],
      "model-namespace" : "https://kiegroup.org/dmn/_74683546-B1D7-4A6C-86C6-4A2268546C77",
      "model-name" : "ConsolidatedDMN",
      "decision-name" : [ ],
      "dmn-context" : {
        "cs" : {
          "Credit Score Threshold 3" : 15,
          "Credit Score Threshold 2" : 10,
          "Credit Score Threshold 1" : 5,
          "Credit Score" : 3,
          "Credit Score Grade" : 5
        },
        "op" : {
          "OperationYearsThreshold 2" : 10,
          "OperationYearsThreshold 3" : 15,
          "OperationYearsThreshold 1" : 5,
          "OperationYears" : 3,
          "OperationYearsGrade" : 0
        },
        "Final Grade" : 4,
        "by" : {
          "BankingYearsThreshold 3" : 15,
          "BankingYearsThreshold 2" : 10,
          "BankingYearsGrade" : 5,
          "BankingYearsThreshold 1" : 5,
          "BankingYears" : 3
        }
      },
      "decision-results" : {
        "_FCB4376F-9242-4D22-8F07-551DA7930E06" : {
          "messages" : [ ],
          "decision-id" : "_FCB4376F-9242-4D22-8F07-551DA7930E06",
          "decision-name" : "Final Grade",
          "result" : 4,
          "status" : "SUCCEEDED"
        },
        "https://kiegroup.org/dmn/_9D9A3A95-438A-4B2B-9EB1-ED0797B35BCD#_131C30C8-5AC1-411A-B3D0-3F6A884F5691" : {
          "messages" : [ ],
          "decision-id" : "https://kiegroup.org/dmn/_9D9A3A95-438A-4B2B-9EB1-ED0797B35BCD#_131C30C8-5AC1-411A-B3D0-3F6A884F5691",
          "decision-name" : "by.BankingYearsGrade",
          "result" : 5,
          "status" : "SUCCEEDED"
        },
        "https://kiegroup.org/dmn/_EF8F583F-F7E9-4260-9081-C974B36C91AC#_126977A0-1171-403B-A1E4-3FA515EB5385" : {
          "messages" : [ ],
          "decision-id" : "https://kiegroup.org/dmn/_EF8F583F-F7E9-4260-9081-C974B36C91AC#_126977A0-1171-403B-A1E4-3FA515EB5385",
          "decision-name" : "cs.Credit Score Grade",
          "result" : 5,
          "status" : "SUCCEEDED"
        },
        "https://kiegroup.org/dmn/_FCC9F0EA-2E6E-4E63-A97C-B6C1A1359A94#_6DDCF119-4629-4F2E-BCF3-160B4876E8BD" : {
          "messages" : [ ],
          "decision-id" : "https://kiegroup.org/dmn/_FCC9F0EA-2E6E-4E63-A97C-B6C1A1359A94#_6DDCF119-4629-4F2E-BCF3-160B4876E8BD",
          "decision-name" : "op.OperationYearsGrade",
          "result" : 0,
          "status" : "SUCCEEDED"
        }
      }
    }
  }
}
```
