# System Architecture

## Overview

The server is designed as a single-node backend system that hosts multiple independent services. Each service runs in its own Docker container to ensure isolation, fault tolerance, and ease of maintenance.

## High-Level Components

- Linux host (Ubuntu Server)
- Docker Engine
- Docker Compose
- Reverse proxy
- VPN gateway
- Persistent storage volumes

## Architecture Flow

1. External requests resolve through DuckDNS
2. Traffic enters the server via the reverse proxy
3. Requests are routed to internal services
4. Sensitive services require VPN access
5. Data is persisted using Docker volumes

## Design Principles

- **Isolation**: Services do not interfere with each other
- **Recoverability**: Containers restart automatically on failure
- **Minimal exposure**: Only required services are public
- **Documentation-first**: System behavior is clearly described
