## Alex Xu - System Design

### Basic Design Concpet
- 




### Design A rate limiter
#### Rate limiter: to control the rate of traffic sent by client/service. 
#### Example: 
- One user can write no more than 2 posts per second.
- One user can create 10 accounts at maxiumem per day from the same IP Address

  
#### Benefits:
- Prevent DOS attack.
- Reduce cost.
- Prevent servers from being overloaded.

#### Design Option
1. API Gateway - Middleware
   - Convenient if API Gateway is already built. It's also beneficial for IP whitelisting, authentication etc.
3. Implement in Server Side
   - Have full control
   - Takes time
3. Implement in Client Side
   - Not frequently used

#### Algorithm for rate limiting 
1. Token bucket algorithm: Create bucket with defined bucket size and token refill rate. Once a request is coming in, if the bucket has enough token, the request can pass through,vice versa.
   - How many buckets are needed? It depends on which unit we want to do throttling. For IP Address, could be 1 bucket for each API type. 
   - Pros:
   - - Easy to impelement
     - Memory effeicient.
     - Token buckets are allowed for a burst of traffic for short period.
   - Cons:
   - - hard to rune bucket size and token refill rate. 





