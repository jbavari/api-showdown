# api-showdown
A comparison of API's accessing postgres - Go, Phoenix, Rails, and Node.js

# The idea

Many coffeeshops have art on the walls. This art is drawn by local artists, and available at many coffeeshops.

We'll have a simple coffee shop art selection. Coffee shops will be stored, the art, and the artists.

# DB Structure

First we'll store shops. Then we'll store art, that has shops it is associated with. Finally, we'll store artists, and associate them with art work.

Shops
Artists
Artwork

# File structure

```
/db
  # Database stuff, set up, creation, migration, etc
/server
  /go
  /node
  /phoenix
  /rails
```
