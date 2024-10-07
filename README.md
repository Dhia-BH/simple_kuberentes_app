# simple_kuberentes_app
Description:

This repository contains a simple Kubernetes application demonstrating a microservices-based architecture. It includes a voting app, result app, Postgres database, Redis cache, and a worker component, all deployed using Kubernetes Deployments and Services.

Voting App: Allows users to submit their votes.

Result App: Displays the results of the voting process, retrieving data from the Postgres database.

Postgres Database: Manages persistent storage for the voting results.

Redis Cache: Provides in-memory caching to enhance performance and reduce latency for frequent data retrieval.

Worker Component: Processes background tasks to ensure smooth operation of the application.

This app showcases the use of multiple containerized services working together within a Kubernetes cluster, highlighting the benefits of using Redis for caching and Postgres for reliable data storage.
