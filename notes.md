# Redis Commands

Define a key
```
SET "key" value
```

Define a key with expiration
```
SET "key" value EX seconds
```

Define keys in batch
```
MSET key value [key value ...]
```


Get a key
```
GET "key"
```

Get all key names
```
KEYS *
```
