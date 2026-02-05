# Rate-Limited-Task-Execution

This project implements a simple, single-node rate-limited task execution system in Java.  
The goal is to study and demonstrate how tasks can be safely executed under concurrency and throughput constraints, with clear control over execution rate, retries, and system behavior under load.

The project is intentionally scoped for academic evaluation and system design clarity rather than production completeness.

## What the system does

At a high level, the system:
- Accepts tasks through a small HTTP API
- Queues tasks in memory with optional priority
- Executes tasks using a worker pool
- Enforces a configurable rate limit on task execution
- Retries failed tasks with backoff
- Exposes basic metrics and task status
- Provides a minimal UI to demonstrate behavior

The system is designed to run as a standalone service on a local machine or a private network node (e.g., an Arch Linux host or VPN peer).

## Core features

- Token-bucket–based rate limiting
- Thread-safe in-memory task queue
- Worker pool using Java concurrency primitives
- Retry with exponential backoff
- Basic task lifecycle tracking (queued, running, completed, failed)
- Minimal web UI for task submission and monitoring
- Simple configuration via application properties
- Graceful shutdown support

## Running locally

Requirements:
- Java 17 or newer
- Maven or Gradle (depending on build setup)

Typical run flow:
1. Build the project:




TL;DR I am open fro offering dual-license for a paid version 
