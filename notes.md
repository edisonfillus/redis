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

## Sets

Add item to set
```
SADD "key" element
```

Item count
```
SCARD "key"
```

List elements
```
SMEMBERS "key"
```

Check if element exists
```
SISMEMBER "key" element
```

Remove element
```
SREM "key" element
```

Intersection between sets
```
SINTER "key1" ["key2" ...]
```

Union between sets
```
SUNION "key1" ["key2" ...]
```

Difference between sets
```
SDIFF "key1" ["key2" ...]
```
## Sorted Sets (Ranking)

Add item to set
```
ZADD "key" score member
```

Item count
```
ZCARD "key"
```

List itens ascending
```
ZRANGE "key" start end
```
OBS: to get all, set end as -1

List itens descending
```
ZREVRANGE "key" start end WITHSCORES
```

Get score of an member
```
ZSCORE "key" "member"
```

Get position of an member
```
ZRANK "key" "member"
ZREVRANK "key" "member"
```

Increment member score
```
ZINCRBY "key" "increment" "member"
````
