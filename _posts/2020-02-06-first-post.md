---
title: "Code Review"
date: 2020-02-06 12:07:28 -0400
categories: network
---

## AlgoSocket

- input (protocol.Protocol, TimeoutMixin)

--------------------------------------------------

- declare part

  ```python
  def __init__(self):
  
  """
    array :
    device :
    f : 
    num :
    i_time = 클라이언트가 요청한 시간 (initial time)
    former = input shape (4,4)
  """

  ```
  
  
- receive data (called whenever data is received)

  num, current_time, length of data, data value 를 출력하고, num+1, resetTimeout()을 호출하는 함수
  
   ```python
   
   def dataReceived(self, data)
  ```


- make connection  (called when a connection is made)

   ```python
   
   @inlineCallbacks
   def connectionMade(self):
   
    self.factory.clients.append(self)
    print("Made : clients are ", self.factory.clients)
    yield self.sleep(10)
    self.setTimeout(30)
    self.resetTimeout()
    self.f_time = time.time()
    self.num += 1
    print('start')
    self.send_request(res=b'INIT\r\n')
  ```
  
- make connection  (called when a connection is made)

   ```python
   
   @inlineCallbacks
   def connectionMade(self):
   
    self.factory.clients.append(self)
    print("Made : clients are ", self.factory.clients)
    yield self.sleep(10)
    self.setTimeout(30)
    self.resetTimeout()
    self.f_time = time.time()
    self.num += 1
    print('start')
    self.send_request(res=b'INIT\r\n')
  ```
  
- make connection  (called when a connection is made)

   ```python
   
   @inlineCallbacks
   def connectionMade(self):
   
    self.factory.clients.append(self)
    print("Made : clients are ", self.factory.clients)
    yield self.sleep(10)
    self.setTimeout(30)
    self.resetTimeout()
    self.f_time = time.time()
    self.num += 1
    print('start')
    self.send_request(res=b'INIT\r\n')
  ```
  
- make connection  (called when a connection is made)

   ```python
   
   @inlineCallbacks
   def connectionMade(self):
   
    self.factory.clients.append(self)
    print("Made : clients are ", self.factory.clients)
    yield self.sleep(10)
    self.setTimeout(30)
    self.resetTimeout()
    self.f_time = time.time()
    self.num += 1
    print('start')
    self.send_request(res=b'INIT\r\n')
  ```

You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

​```python
def print_hi(name):
  print("hello", name)
print_hi('Tom')
​```
