# Redis Introduction

Install Redis with `asdf`:

```zsh
asdf plugin add redis
asdf install redis latest
```

Now, run the Redis server with: `redis-server`

And then you can run the CLI with: `redis-cli`

## Redis commands

Set values:

* Set values: `SET <key> <value>`
* Get values: `GET <key>`
* Check if value exists: `EXISTS <key>`
* Delete value: `DEL <key>`
* Expire: `EXPIRE <key> <number_of_seconds>`
* Increment: `INCRBY <key> <increment>`
* Decrement: `DECR <key> <decrement>`
* Multiple set: `MSET <key1> <value1> <key1> <value2> ...`
* Multiple get: `MGET <key1> <key2> ...`

## Redis basic data types

* Strings
* Hashes
* Lists
* Sets
* Sorted sets

## Redis hashes

* To set a hash with multiple fields and values: `HMSET <key> <field1> <value1> <field2> <value2> ...`
* To get a field from a specific hash: `HGET <key> <field>`
* To get all fields and values from a hash: `HGETALL <key>`

## Redis lists

* Left push: `LPUSH <list_name> <value>`
* Right push: `RPUSH <list_name> <value>`
* To get the list: `LRANGE <list_name> <start> <stop>` (index starts at 0)
* To drop an element from the right: `RPOP <list_name>`

## Sets and Sorted sets

* Add members to a set: `SADD <set_name> <member1> <member2> ...`
* Get members of a set: `SMEMBERS <set_name>`
* Check to see if a value is a memeber of a set: `SISMEMBER <set_name> <value>`

* Add members to a sorted set: `ZADD <set_name> <score1> <member1> <score2> <member2> ...`
* To get members: `ZRANGE <set_name> <start> <stop>`
* To get the rank of a member: `ZRANK <set_name> <member>`
