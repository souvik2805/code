
### 1. Event loop
 Web Api -> 1. Timeout
             2. Network
             3. Event

https://www.youtube.com/watch?v=8aGhZQkoFbQ
  


So In javascript we have two types to code -> one which is handle and  run by javascript itself and another one is handled by web api.

Web api -> setTimeout , Network, event handler

for Web api handler

js code - (1) > Web api (wait for it's time) (2) -> then put the function in Callback Queue  (3) --> eventLoop --> callstach (4)


for normal 

js code (1) --> evvent loop  --> callstack (2)
