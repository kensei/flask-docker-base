# flask app docker base

## start

`docker-compose up -d`

## running confirmation

```
curl http://localhost:5000/
curl http://localhost:5000/ -X POST -H "Content-Type: application/json" -d '{"keyword": "Keffia"}'
```

