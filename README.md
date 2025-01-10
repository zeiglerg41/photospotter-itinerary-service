# photo-spotter-itinerary-service

## Table of Contents
- [Overview](#overview)
- [Planned Features](#planned-features)
- [Environment and Dependencies](#environment-and-dependencies)
- [API Endpoints](#api-endpoints)
- [Deployment and Usage](#deployment-and-usage)
- [Tasks](#tasks)

## Overview
This service focuses on trip planning and route optimization, allowing users to assemble multi-stop itineraries for photography. It can factor in travel time, sunrise/sunset, and other scheduling details.

## Planned Features
- Creation and management of itineraries
- Route optimization using an external routing library (e.g., GraphHopper)
- Integration of sunrise/sunset data
- Time window adjustments for traffic or weather

## Environment and Dependencies
- Go for high concurrency (routing calculations) or .NET 6+ for robust tooling
- A routing library (GraphHopper, OSRM, etc.)
- Docker for container builds

## API Endpoints
- `/itineraries` for create, read, and update operations
- `/itineraries/optimize` to run route optimizations
- `/itineraries/schedule` for adjusting times based on sunrise/sunset

## Deployment and Usage
- Run locally with `go run main.go` or `dotnet run`
- Build container: `docker build -t photo-spotter-itinerary-service .`
- Deploy via Kubernetes manifests or Helm charts

## Tasks
- Implement itinerary CRUD operations
- Integrate a routing library for optimizations
- Implement scheduling logic for best shooting times
- Provide a `/health` endpoint and CI integration
