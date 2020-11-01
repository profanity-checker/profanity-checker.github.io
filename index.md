# AntiProfanity.API
Detect content is profane.

**URL** : `/api/profanity_detection/`

**Method** : `POST`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

**Content examples**

For positive profanity detection

```json
{
"status": "success",
"isProfanity": true
}
```

For negative profanity detection

```json
{
   "status": "success",
   "isProfanity": false
}
```

For bad Request

```json
{
"status": "error",
"code": 400,
"message": "Bad Request: Missing required parameters/Request content type is not allowed."
}
```

For Maximum content length exceeded

```json
{
"status": "error",
"code": 1001,
"message": "Maximum allowed length of the input text is 100."
}
```
For minimum allowed length
```json
{
"status": "error",
"code": 1002,
"message": "Minimum allowed length of the input text is 2."
}
```
For empty content
```json
{
"status": "error",
"code": 1002,
"message": "Minimum allowed length of the input text is 2."
}
```
For Unexpected error
```json
{
"status": "error",
"code": 1004,
"message": "Unexpected error occurred."
}
```


