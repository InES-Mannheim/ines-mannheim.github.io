---
section-id: core
layout: default
img: core.png
category: Services
title: Core
short-title: Core
description: |
---
The `core` module implements the domain and provides means for alteration. The package structure is depicted below.

Package `domain.model` is the bounded context and contains the codified domain model. `SPA` as the sole application service is contained in the `application` package. Further, a `SpaBuilder` is available which implements a DSL for configuring `SPA` instances. For example, `SpaBuilder.local().memory().shared()` creates an instance of the `SPA` which stores its data in a runtime shared memory location. `SPA` itself provides CRUD functionalities for the domain.

Package `io` contains the `Importer` and `Exporter` interfaces for importing data from and to Jena's `Model` inteface and, thus, RDF. Further, classes `ImporterSupport` and `ExporterSupport` are containers responsible for managing groups of `Importer`s and `Exporter`s. All file-based implementations are stored in subpackage `file`.

Package `persistence` contains all implementations responsible for mapping Java instances to RDF and vice-versa. All `Repository` implementations rely on the `Transformation` class which implements a DSL for RDF <-> Java transformations.

A leaky abstraction over `Jena` is the content of the `storage` package. When a `Store` supports transactions, each connection is automatically run in a transaction conext.