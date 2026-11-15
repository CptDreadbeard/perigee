# ADR-0002: No backend and no user data

Status: accepted
Date: 2026-11-14

## Context

The cost must be as near to zero as possible. The developer does not want to operate a service that processes personal data, such as IP addresses. German commentary generally treats a software maker that does not process data as not a data controller. A website or an own API changes that. This is not legal advice.

## Decision

Perigee has no server. Each installed app calls the public data sources directly. The app has no accounts, no telemetry, no analytics and no crash reports. Settings and the cache stay on the computer of the user. Only the Rust backend makes network requests. The frontend makes no network requests. It loads no remote fonts and no CDN files.

## Alternatives

- A static website. It needs a privacy policy that names the operator.
- An own cache API. The server receives client IP addresses. The cost can reach about 6.50 EUR each month.

## Consequences

Positive:
- Hosting cost is zero.
- The developer has no usage data to store or protect.

Negative:
- Rate limits apply to each user IP address. Launch Library 2 allows 15 requests each hour. CelesTrak allows one download for each data update, which is about 2 hours.
- The app must cache each response. The app must work offline from the cache.
- Bug reports come only through GitHub issues.
- Fallback: if limits become a problem, a scheduled GitHub Actions workflow builds a static JSON snapshot. GitHub operates the server.

## Review trigger

A data source changes its rate limits or terms. Or users on shared IP addresses report missing data.
