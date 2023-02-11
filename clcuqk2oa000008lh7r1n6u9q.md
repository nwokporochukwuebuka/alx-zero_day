# Introduction to Caching Using Redis

## Introduction to caching and its benefits

Caching is a technique used to store frequently accessed data in a temporary storage area, known as a cache, to speed up the retrieval of that data.

Some of the benefits of caching include:

* It significantly improves the performance of an application by reducing the number of times it needs to fetch data from a slower storage medium, such as a database or a remote API.
    
* It also improves the availability of an application by storing a copy of the data locally and serving it in case the backend resources are unavailable.
    
* Additionally, Caching can also reduce the load on the backend resources and improve the scalability of the application, as the cache can handle a large number of requests without the need to repeatedly fetch the same data from the backend.
    

Hence, in summary, caching can help improve the performance, scalability, and availability of an application by temporarily storing frequently accessed data in a cache.

> ***NB:*** *This article aims to provide an overview and caching strategies for using Redis to cache data in a Node.js application.*

## Factors to consider when caching

When deciding whether or not to cache data, it's important to consider the following factors:

* **Data access patterns:** If the data is frequently accessed, caching it can significantly improve the performance of the application.
    
* **Data retrieval Speed:** If retrieving the data from the backend is slow, caching it can improve the performance of the application.
    
* **Data volatility:** If the data is static and not expected to change frequently, caching can be a good strategy.
    
* **Data generation cost:** If generating the data is resource intensive, caching it can save resources and improve the performance of the application.
    
* **App's availability:** If the data is important for the application to function and should be served even if the backend is down, caching a copy of it can help to support the availability of the application.
    

> It is important to consider the trade-offs of caching, such as increased complexity, the risk of serving stale data, and the need for eviction policies to manage the cache size.

## What is Redis?

Redis is an in-memory data structure store that can be used as a database, cache, and message broker. It supports a wide variety of data structures such as strings, hashes, lists, sets, and more. It is often used for real-time data processing, high-speed data ingest, and caching. Redis is open-source and written in C.

Redis runs inside the working memory (RAM) inside your computer, and this is what makes it fast. The Redis database stores data in key-value pairs, and it stores values as a string.

## How to Install Redis on Windows

To download Redis on a Windows machine, follow the given steps:

* Visit the [GitHub repo](https://github.com/microsoftarchive/redis/releases)
    
* Download the [**Redis-x64-3.0.504.msi**](https://github.com/microsoftarchive/redis/releases/download/win-3.0.504/Redis-x64-3.0.504.msi)
    

After downloading Redis on your machine

* Locate the .msi file and install
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673616919219/56ec5816-5383-491c-965e-f9fe1c0f593c.png align="center")
    
* Click on"Next"
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673617046849/fe3829dc-9bb2-4412-8559-32119e6ea4f9.png align="center")
    
* Ensure that the "Add the Redis installation folder to the PATH environmental variable" is ticked and click "Next"
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673617296484/c4bfd0df-f742-4dcd-b853-f083c092bf26.png align="center")
    
* Click the "Add an exception to the Windows Firewall" box and click "Next"
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673617489399/8914ee56-b4c6-4f3b-b5a1-ca38c5c24651.png align="center")
    
* Set the maximum memory for the Redis storage on your local machine and click "Next".
    

Following the above process will help install Redis on a Windows machine. To check if Redis is installed locally, run the command `redis-cli` on the command prompt.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673620935911/298e3392-b054-4c04-b08a-5f2ceaf417d5.png align="center")

Immediately after the command is entered, the redis-client appears, where caching operations can be carried out. To exit the CLI, use the `quit` command.

## Commands used in Redis

* **SET:** This command is used to set a variable in redis. To do this, a key name and the name of the variable are required. e.g `SET <keyname> <value>`
    
* **GET:** This command is used to get a value using the key name. e.g `GET <keyname>`
    
* **DEL:** This command is used to delete a value. This requires the key name alone. `DEL <keyname>`
    
* **EXIST:** This command helps to check if a key name already exists. `EXISTS <keyname>`
    
* **KEYS:** This command helps to check if a particular key exists. e.g `KEY <keyname>`. It can also call all the keys that exist in the database, e.g `KEYS *`
    
* **FLUSHALL:** This commands flushes or deletes all the keys in the database. e.g `FLUSHALL`
    
* **CLEAR:** To clear out all the output i.e. clear the screen we use the `CLEAR` command.
    
* **TTL:** This command means Time To Leave. It gives us the expiration time for a variable that has been stored in a key. e.g `TTL <keyname>` If the expiration time was not set for a particular variable, it returns `-1`, which means that it can leave forever.
    
* **EXPIRE:** This command sets an expiration time for a key-value pair. e.g `EXPIRE <keyname> <time-in-seconds>` . After the expiration time, the key-value pair is automatically flushed from the database.
    
* **SETEX:** This command helps to set a key to a value with an expiration time. e.g `SETEX <keyname> <time-in-seconds> <value>` .
    
* **LPUSH:** This command creates an array for storing values and storing the values at the left-hand side of the array. e.g `LPUSH <keyname> <value1> <value2> ...... <valueN>` .
    
* **RPUSH:** This command creates an array for storing values and storing the values at the right-hand side of the array. e.g `RPUSH <keyname> <value1> <value2> ...... <valueN>` .
    
* **LRANGE:** This command is used to print out the items in a list. e.g `LRANGE <keyname> <start-index> <stop-index>`
    
* **LPOP:** This command removes the leftmost value in the array and returns it to the user. e.g `LPOP <keyname>` .
    
* **RPOP:** This command removes the rightmost value in the array and returns it to the user. e.g `RPOP <keyname>` .
    
* **SADD:** This command creates a set and adds values to it. e.g `SADD <keyname> <value1> <value2> <value3> .... <valueN>`
    
* **SMEMBERS:** This command displays the values in a set. e.g `SMEMBERS <keyname>`
    
* **HSET:** This sets the value in the field of a key. e.g `HSET <keyname> <fieldname> <value>` . This stores data like hash tables, but it is more like key-value pairs stored in key-value pairs.
    
* **HGET:** This gets the value stored in a field name. e.g `HGET <keyname> <fieldname>`
    
* **HGETALL:** This gets all the value that is stored in a hash table. e.g `HGETALL <keyname>` .
    
* **HEXISTS:** This command checks if a field name exists in the hash table. e.g `HEXISTS <keyname> <fieldname>` .
    

## Conclusion

This article highlights the benefits of caching, as well as the trade-offs of caching, with a brief introduction to how to use Redis and basic commands.

Thank you for reading 🙏🙏.

You can follow me on the following platforms:

Twitter 🐦: [**@nwokporo\_ebuka**](https://twitter.com/@nwokporo_ebuka)

LinkedIn ⚡: [**@chukwuebuka\_nwokporo**](https://www.linkedin.com/in/chukwuebuka-nwokporo-018a98175/)

GitHub 🚀: [**@ebukvick**](https://github.com/Chukwuebuka2)

Hashnode 📗: [**Nwokporo Chukwuebuka**](https://codedaddy.hashnode.dev/@codeDaddy)