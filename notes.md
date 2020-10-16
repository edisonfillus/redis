# Redis Commands

## General
Get all key names
```
KEYS *
```

Delete a key
```
DEL "key"
```

Set expires in a key
```
EXPIRE "key" seconds
```

Get time left to expire
```
TTL "key"
```




## Strings

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

## Hashes
Define a key with many fields
```
HSET "key" field value [field value ...]
```

Get a field from key
```
HGET "key" field
```

Get all fields form a key
```
HGETALL "key"
```

Delete a field from key
```
HDEL key field [field ...]
```

## Counters
Create an increment counter
```
INCR "key"
```

Create a decrement counter
```
DECR "key"
```

Create a hash field as an increment counter
```
HINCRBY "key" field increment
```
