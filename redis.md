
# My Redis Notebook

Run redis-server on a terminal.

![image](https://github.com/Hariharan98m/jupyter-notebooks/blob/master/redis/1.JPG)

Run client instance on another terminal

![image.png](![image](https://github.com/Hariharan98m/jupyter-notebooks/blob/master/redis/2.JPG))

## Redis Strings



## Redis hashes

A redis hash is a collection of field-value pairs under a single key, such that every field maps onto to a value. 

Example: 

`
student: {
       name: hari, 
       age: 15, 
       class: 10
    }
`

Note that the key should be a string, and the value can be of any datatype.


```python
save  #saves the DB to disk
```


```python
flushall  # flushes all the keys in the DB
```

### Creating a hash


```python
hmset stu-1 name hari age 15 class 10
```

![image.png](![image](https://github.com/Hariharan98m/jupyter-notebooks/blob/master/redis/3.JPG))

### Accessing fields in a hash


```python
hget stu-1 name

hget stu-1 age

hget stu-1 class
```

![image.png](![image](https://github.com/Hariharan98m/jupyter-notebooks/blob/master/redis/4.JPG))


```python
hgetall stu-1
```

![image.png](![image](https://github.com/Hariharan98m/jupyter-notebooks/blob/master/redis/5.JPG))

### Check if a field exists in a key


```python
hexists stu-1 name
hexists stu-1 surname
```

![image.png](![image](https://github.com/Hariharan98m/jupyter-notebooks/blob/master/redis/6.JPG))

### Delete a field in a key


```python
hdel stu-1 class
```

![image.png](![image](https://github.com/Hariharan98m/jupyter-notebooks/blob/master/redis/7.JPG))

### Set a field only if it doesn't exists


```python
hsetnx stu-1 name tom
hsetnx stu-1 nameT tom
```

![image.png](![image](https://github.com/Hariharan98m/jupyter-notebooks/blob/master/redis/8.JPG))
