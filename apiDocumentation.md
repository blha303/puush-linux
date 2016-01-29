puush API documentation
-----------------------

###Authentication
 - URL: `/api/auth`
 - Request (two methods, key authentication takes priority):
    - With login credentials:
        - e = email address
        - p = password
    - With API key:
        - k = apikey
 - Response (authenticated, success): `{premium},{apikey},[expire],{size-sum}`
 - Response (failure): `-1`

###Deletion
 - URL: `/api/del`
 - Request:
    - k = apikey
    - i = file identifier - on puush.me, is SEQUENTIAL
 - Response (success): `0`
 - Response (failure): `-1`

###History
 - URL: `/api/hist`
 - Request:
    - k = apikey
 - Response (history, success): up to 10 lines of `{id},{YYYY-MM-DD HH:MM:SS},{url},{filename},{views},{unknown}`
 - Response (failure): `-1`

###Thumbnail
 - URL: `/api/thumb`
 - Request:
    - k = apikey
    - i = file identifier - on puush.me, is SEQUENTIAL
 - Response (success): image, 100x100 png
 - Response (failure): nothing

###Upload
 - URL: `/api/up`
 - `Content-Disposition` header needs filename
 - Request:
    - k = apikey
    - z = anything at all
    - f = file
 - Response (upload, success): `0,{url},{id},{size}`
 - Response (failure, upload): `-1`
 - Response (failure, no filename header): `-2`
