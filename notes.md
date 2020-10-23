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

## Bits

Define a key
```
SETBIT "key" offset value
```

Get a key
```
GETBIT "key" offset
```

Count of true
```
BITCOUNT "key"
```

Bitwise operations
```
BITOP AND destkey srckey1 srckey2 srckey3 ... srckeyN
BITOP OR destkey srckey1 srckey2 srckey3 ... srckeyN
BITOP XOR destkey srckey1 srckey2 srckey3 ... srckeyN
BITOP NOT destkey srckey
```

## Lists

Include item on left
```
LPUSH "key" value
```

Include item on right
```
RPUSH "key" value
```

Get by index
```
LINDEX "key" index
```

Get by range
```
LRANGE "key" start stop
```

List length
```
LLEN "key"
```

Trim a list
```
LTRIM "key" start stop
```

Take element from the left
```
LPOP "key"
```

Take element from the left, waiting
```
BLPOP "key" seconds
```

Take element from the right
```
RPOP "key"
```

Take element from the right, waiting
```
BRPOP "key" seconds
```

Remove element from the list
```
LREM "key" count element
```
