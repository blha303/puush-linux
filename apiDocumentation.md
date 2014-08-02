puush API documentation
-----------------------

###Authentication
 - URL: `/api/auth`
 - Request:
 - - e = email address
 - - p = password
 - Response (authenticated, success): `{premium},{apikey},[expire],{size-sum}`
 - Response (failure): `-1`

###Deletion
 - URL: `/api/del`
 - Request:
 - - k = apikey
 - - i = file identifier - on puush.me, is SEQUENTIAL
 - Response (history, success): `{id},{YYYY-MM-DD HH:MM:SS},{url},{filename},{views},{unknown}`
 - Response (failure): `-1`

###History
 - URL: `/api/hist`
 - Request:
 - - k = apikey
 - Response (history, success): `{id},{YYYY-MM-DD HH:MM:SS},{url},{filename},{views},{unknown}`
 - Response (failure): `-1`

###Thumbnail
 - URL: `/api/thumb`
 - Request:
 - - k = apikey
 - - i = file identifier - on puush.me, is SEQUENTIAL
 - Response (success): image, 100x100 png
 - Response (failure): `-1`

###Upload
 - URL: `/api/up`
 - `Content-Disposition` header needs filename
 - Request:
 - - k = apikey
 - - z = "poop"
 - - f = file
 - Response (upload, success): `0,{url},{id},{size}`
 - Response (failure, upload): `-1`
 - Response (failure, no filename header): `-2`
