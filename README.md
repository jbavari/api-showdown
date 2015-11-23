# api-showdown
A comparison of API's accessing postgres - Go, Phoenix, Sinatra, and Node.js.

# The idea

Many coffeeshops have art on the walls. This art is drawn by local artists, and available at many coffeeshops.

We'll have a simple coffee shop art selection. Coffee shops will be stored, the art, and the artists.

# DB Structure

First we'll store shops. Then we'll store art, that has shops it is associated with. Finally, we'll store artists, and associate them with art work.

Shops - name, location, hours  
Artists - name, list of artwork  
Artwork - artwork name, shop listed  

## API

We'll have the following API's available, all returning JSON from Postgres.

All results will follow this JSON structure:

```
{
  "result": "ok",
  "payload": {}
}
```

GET  
/api/v1/shops  
/api/v1/shops/zip/:zipcode  
/api/v1/shops/nearme (POST lat/lon)  
```
{
  "shops": [
    { "name": "Logans Cafe", "location": "25, 55", "hours": "8-7", "artwork": []}
  ]
}
```

GET
/api/v1/artist/:id
```
{
  "name": "Jeffrey",
  "artwork": [
    "name": "Dragon",
    "shop": {/* Shop JSON Data */}
  ]
}
```

# File structure

```
/db
  setup.sql
  # Database stuff, set up, creation, migration, etc
/server
  /go
  /node
  /phoenix
  /rails
```


We'll need something that will execute all this seamlessly, that will have to be decided.
