# MaquiGest Platform Mock

Mock REST API developed for the MaquiGest academic project.

## Overview

MaquiGest Platform Mock is a simulated REST API created to support the development and demonstration of the MaquiGest Angular Web Application.

This repository is not the real backend.

The real backend is developed separately in maquigest-platform using Java, Spring Boot, MySQL, Domain-Driven Design, Hexagonal Architecture and CQRS.

## Technologies

- Node.js
- JavaScript
- JSON Server
- JSON-based mock data

## Project Structure

The repository contains the following files:

- server.js: Mock API server and endpoints.
- seed.json: Initial demonstration data.
- package.json: Dependencies and execution scripts.
- .gitignore: Excluded dependencies and generated files.

## Installation

Requirements:

- Node.js and npm installed.

Install dependencies:

    npm install

Start the API:

    npm start

The server uses the PORT environment variable when available.

## Health Check

Endpoint:

    GET /health

## Authentication

Available endpoints:

    POST /api/v1/authentication/sign-in
    POST /api/v1/authentication/sign-up

Authentication is simulated and intended only for academic demonstrations.

## REST Resources

The mock provides REST resources under /api/v1:

- profiles
- equipment-categories
- equipment
- rental-requests
- rentals
- deliveries
- equipment-returns
- subscription-plans
- user-subscriptions
- maintenances
- incidents

## Data Storage

Initial records are loaded from seed.json.

The API uses temporary storage, so changes may disappear after restarting or redeploying the service.

Newly registered demonstration accounts are also temporary.

## Limitations

- No real database persistence.
- No production-grade authentication.
- No real JWT authorization.
- No complete backend domain implementation.
- Not intended for production.
- Only fictitious demonstration data should be used.

## GitFlow

The project follows GitFlow:

- main: Stable version.
- develop: Integration branch.
- feature/*: Feature development.
- release/*: Release preparation.

## Related Repositories

- maquigest-webapp: Angular Web Application.
- maquigest-platform: Real Spring Boot backend.
- maquigest-website: Landing Page.
- maquigest-report: Academic report.

## Academic Purpose

This repository preserves the initial API simulation and its Git history as evidence of the MaquiGest development process.
