---
title: Cloud Computing Software Architecture Patterns
keywords:
summary: "It's the note during learning the cource on Udemy"
sidebar: work_sidebar
permalink: mydoc_Cloud_Computing_Software_Architecture_Patterns.html
folder: work
---

## Introduction to Cloud Computing Software Architecture Patterns

* Software Architecture Patterns
  * Universal Solutions to Common Design Problems
  * Implementation independent
* Cloud Computing Benefits
    * Access to "infinite" Infrastructure (IaaS)
  * Convenient Pricing Model
  * Tools and Features:
    * FaaS
    * Multi-zone, Multi-Region Deployment

## Scalability Patterns

### Load Balancing Pattern

* Goal: 
  * Helps us take advantage of "infinite" accesses to cloud computers
* Components:
  * Source
  * Dispatcher
  * Workers
* Techniques:
  * Load Balancing Service
  * Message Broker

### Pipes and Filters Pattern

* Definitions:
  * Data Source
    * The origin of the incoming data
  * Data Sink
    * The final destination of the data
* Benefits:
  * Use of a different programming language for each operation
  * Optimal Performance/Cost
  * High Scalability
  * Parallel Execution of tasks

### Scatter Gether Pattern

* Components:
  * User
  * Dispatcher
  * Workers (different from each other)
* Core Principle:
  * Each request to a worker is independent of the other
  * Parallel execution of many requests
  * Providing information in constant time

### Execution Orchestrator Pattern
* Problem:
  * Running a complex flow of operations across multiple service/microservices
* Solution:
  * A centralized service acting as the "brain".
  * The only service aware of the
    * Context
    * Execution Steps
  * Responsible for handling issues and retries

### Choreography Pattern
* Problems:
  * Run a flow of business operation that involve multiple services.
  * Tight coupling between microservices using Orchestration Pattern.
* Solution:
  * Event-Driven Architecture using Choreography.

### Map Reduce Pattern
* Problem:
  * The complexity involved in running computations on very large inputs
* Solution:
  * Follow the same programming model: Map-Reduce
  * Reuse the execution framework/architecture

### The Saga Pattern
* Problem:
  * Lose of ACID Transaction properties in a distributed transaction across multiple microservices.
* Solution:
  * Series of local transactions on success
  * Compensating operations to abort upon failure

### Transactional Outbox Pattern
* Problem:
  * Database operations and event publishing cannot be part of a single transaction
* Solution:
  * Transactional Outbox Table
  * Message Relay Service

### Materialize View Pattern
* Problem:
  * Low Efficiency and Performance of key database queries
* Soution:
  * Read-only Materialized View Table, containing a long query result

### CQRS Pattern
* Definitions:
  * CQRS - Command and Query Responsibility Segregation
  * Command - Data mutation
  * Query - Data read operation
* Problem:
  * Tight Coupling of Command and Query in one microservice and database
* Solution:
  * Separation of Command and Query into separate services and database

## Performance Patterns for Data-Intensive Systems

## Software Extensibility Architecture Patterns

## Reliability, Error Handling and Recovery Software Architecture Patterns

## Deployment and Production Testing Patterns
