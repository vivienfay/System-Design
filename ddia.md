# Part II Distributed Data

## Replication

### What is replication

1. Replication: making copy of the same data on multiple machine that are connected via a network.
Some advantages:
   - keep data geographically close to users
   - allow systems to work even if one machine is down(availability)
   - scale out the number of machines that can serve read queries
2. The difficulty in replication: how to handle the difficulty.

    Three algorithms for handling difficulty
   - single-leader
   - multi-leader
   - leaderless
  
3. Replica: each node that stores a copy of the database is called a replica.
4. The way we ensure that all the data ends up on the all the replicas.
    leader-based replication
    client send data to master(leader) replication -> leader sends to follower using replication log/change stream
5. synchronous versus asynchronous: 
   [截图]
   - sync: 
     - have to wait for followers confirmation
     - guarentee to have an up-to-date copy of the data that is consistent of the leader
     - if follower doesn't respond, the writer cannot be processed
     - normally use one sync and other async -- semi-sync
   - async: doesnt' have to
     - does not guarent to be durable
     - can process the writes
6. setting up new followers: need to ensure that the new follower has an accurate copy of the leader's data





## Partitioning

## Transactions

## The trouble with Distributed Systems

## Consistency and consensus
