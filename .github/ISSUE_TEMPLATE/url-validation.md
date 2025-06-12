---
name: URL Validation Enhancement
about: Add URL validation to ensure only valid URLs are shortened
title: 'Enhancement: Add URL Validation'
labels: enhancement, good first issue
assignees: ''
---

## Description
Currently, the URL shortener accepts any string as input without validating if it's a proper URL. We should add validation to ensure only valid URLs are processed.

## Tasks
- [ ] Add URL validation using Go's `net/url` package
- [ ] Add validation in the `ShortURLHandler` function
- [ ] Return appropriate error messages for invalid URLs
- [ ] Add tests for URL validation

## Expected Behavior
- Valid URLs (e.g., "https://example.com") should be accepted
- Invalid URLs should return a 400 Bad Request with a clear error message
- URLs without scheme (http/https) should be rejected or automatically add https://

## Additional Context
This will improve the reliability and user experience of the URL shortener service. 