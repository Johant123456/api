# api



https://my-json-server.typicode.com/Johant123456/api


## GET
```
curl -X GET "https://my-json-server.typicode.com/Johant123456/api/albums/1"
```

```
Invoke-WebRequest -Uri "https://my-json-server.typicode.com/Johant123456/api/albums/1" -Method Get 
```


## POST

$updatedAlbum = @{
    Id = "1"
    Title = "Updated Album Title"
    Artist = "Updated Artist"
    Price = 29.99
} | ConvertTo-Json

Invoke-WebRequest -Uri "https://my-json-server.typicode.com/Johant123456/api/albums/1" -Method Put -Body $updatedAlbum -ContentType "application/json"


## POST
```
curl -X POST "https://my-json-server.typicode.com/Johant123456/api/albums" \
     -H "Content-Type: application/json" \
     -d '{
           "Id": "6",
           "Title": "Gold: Greatest Hits",
           "Artist": "ABBA",
           "Price": 29.99
         }'
```

```
$newAlbum = @{
    Id = "6"
    Title = "Gold: Greatest Hits"
    Artist = "ABBA"
    Price = 29.99
} | ConvertTo-Json

$response = Invoke-WebRequest -Uri "https://my-json-server.typicode.com/Johant123456/api/albums" -Method Post -Body $newAlbum -ContentType "application/json"
$response.Content
```
