# Basics

## Cluster

A collection of one or more nodes.

Holds all your data and provides indexing and search capabilities across the cluster's nodes.

Identified by a unique name.

A node can only be part of the cluster it is setup to run in.

## Node

A single server which is part of your cluster.

Stores data and participates in indexing and searching.

Identified by a name which is typically a uuid assigned at startup.

A node is setup to join a specific cluster.

## Index

A collection of documents with similar traits. e.g. an index og user data

Identified by a name. This name is refered to when performing operations such as indexing, searching etc.

With a cluster you may have many indexes.

## Document

A document is a JSON file which can be indexed.

One document for each entity e.g. one for a user, one for a book.

Within an index you can store multiple documents.

## Shard

An index can potentially store large ammounts of data that could exceed the storage limits of the node or make the search too slow to be useful.

Shards are used to divide your index into mutiple pieces.

When creating an index you can define the number of shards that you want. Each shard is an independent index which can be hosted on any node in the cluster.

Allow you to horizontally scale your volume.

Allow you to paralellise and distribute operations across shards.

## Replica

A failover mechanism incase a node or shard is unavailable for whatever reason.

A copy of a shard.

Can make more than one replica of a shard.

Provides high availability.

A replica shard is never allocated on the same node as the original.

Allows you to scale your search volume as searches can be executed on replicas in parallel.
