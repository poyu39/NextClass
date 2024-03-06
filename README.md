# NextClass
基於 IOS 捷徑和逢甲大學課程檢索系統 API 的快速查看下一節課腳本。

![image](https://github.com/poyu39/NextClass/assets/42506064/88b461ed-fd6d-49a2-beeb-648ded65c91a)


## 逢甲大學課程檢索系統 API
```
功能：登入

POST:  https://coursesearch02.fcu.edu.tw/Service/Auth.asmx/login
Payload:
{
  "id": <NID>,
  "password": <Password>,
  "baseOptions": {
    "lang": <語言(ex. cht)>,
    "year": <學年度(ex. 112)>,
    "sms": <學期(ex. 2)>
  }
}
```
```
功能：搜尋課程
POST: https://coursesearch03.fcu.edu.tw/Service/Search.asmx/GetType2Result
Payload:
{
  "baseOptions": {
    "lang": "cht",
    "year": 112,
    "sms": 2
  },
  "typeOptions": {
    "code": {
      "enabled": true,
      "value": <選課代碼>
    },
    "weekPeriod": {
      "enabled": false,
      "week": "*",
      "period": "*"
    },
    "course": {
      "enabled": false,
      "value": ""
    },
    "teacher": {
      "enabled": false,
      "value": ""
    },
    "useEnglish": {
      "enabled": false
    },
    "useLanguage": {
      "enabled": false,
      "value": "01"
    },
    "specificSubject": {
      "enabled": false,
      "value": "1"
    },
    "courseDescription": {
      "enabled": false,
      "value": ""
    }
  }
}
```
