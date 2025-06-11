---
name: Add Database Persistence
about: Replace in-memory storage with a persistent database
title: 'Feature: Add Database Persistence'
labels: enhancement, database
assignees: ''
---

## Description
Currently, the URL shortener uses an in-memory map (`urlDB`) to store URLs, which means all data is lost when the server restarts. We should implement a persistent storage solution.

## Tasks
- [ ] Choose and integrate a database (e.g., SQLite, PostgreSQL)
- [ ] Create database schema for URLs
- [ ] Implement database operations (CRUD)
- [ ] Add database connection configuration
- [ ] Update existing functions to use database instead of map
- [ ] Add database migration scripts
- [ ] Add tests for database operations

## Expected Behavior
- URLs should persist across server restarts
- Database operations should be efficient
- Proper error handling for database operations
- Configuration should be environment-based

## Additional Context
This will make the URL shortener production-ready by ensuring data persistence. 

## Project Structure
/url-shortener
  /client         # React app
  main.go         # Go backend
  ... 