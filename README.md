# Multi-module Application

## Main Modules:

- store
- data
- rabbitmq
- shared
- service
- worker
- client-api

## Application Module Requirement

_An application module is needed that will show how many messages were sent per session._

### Steps:

1. Sending messages directly (payload emulation)
2. Creating a database with tasks to send a message and scheduled sending from the worker
3. Scheduled dispatch of tasks to workers (parallelization of duties via RabbitMQ + Redis)
4. Task interception synchronization (Redis). To prevent the same task from being executed twice.

### Additional Component:

- mail client