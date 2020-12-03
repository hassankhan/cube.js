---
title: Cube.js Introduction
permalink: /cubejs-introduction
category: Cube.js Introduction
---

__Cube.js is an open source modular framework to build analytical web applications__. It is primarily used to build internal business intelligence tools or to add customer-facing analytics to an existing application.

1. __Performance.__ Most of effort time in modern analytics software development is spent to provide adequate time to insight. In the world where every company data is a big data writing just SQL query to get insight isn't enough anymore.
2. __SQL code organization.__ Modelling even a dozen of metrics with a dozen of dimensions using pure SQL queries sooner or later becomes a maintenance nightmare which ends up in building modelling framework.
3. __Infrastructure.__ Key components every production-ready analytics solution requires: analytic SQL generation, query results caching and execution orchestration, data pre-aggregation, security, API for query results fetch, and visualization.

Cube.js has necessary infrastructure for every analytic application that heavily relies on its caching and pre-aggregation layer to provide several minutes raw data to insight delay and sub second API response times on a trillion of data points scale.

<img src="https://raw.githubusercontent.com/statsbotco/cube.js/master/docs/old-was-vs-cubejs-way.png" style="border: none" />

## Architecture
__Cube.js acts as an analytics backend__, translating business logic (metrics and dimensions) into SQL and handling database connection.

The Cube.js javascript Client performs queries, expressed via dimensions, measures, and filters. The Server uses Cube.js Schema to generate a SQL code, which is executed by your database. The Server handles all the database connection, as well as pre-aggregations and caching layers. The result then sent back to the Client. The Client itself is visualization agnostic and works well with any chart library.

<p align="center"><img src="https://i.imgur.com/FluGFqo.png" alt="Cube.js" width="100%"></p>
