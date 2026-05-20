# DataCrafter Releases

This repository hosts public release downloads for **DataCrafter**, a self-hosted data engineering platform (Java 21 / Spring Boot / Vaadin).

The source code is maintained in a private repository. This repo exists solely to make built artifacts available for download.

## Downloads

Browse the [Releases](https://github.com/nick2468/DataCrafter-releases/releases) page. Each release includes:

- `datacrafter-server-X.Y.Z.zip` - Server bundle. Contains the fat JAR (with bundled Vaadin frontend), launch scripts (`start.bat`, `start.sh`, `stop.bat`, `stop.sh`), schema and license tools, and a default `datacrafter.properties`. Run `start.bat` (Windows) or `start.sh` (Linux/macOS) after extracting.
- `datacrafter-client-X.Y.Z.zip` - Desktop client bundle. Contains the desktop client fat JAR and launch scripts. Connects to a running DataCrafter server.

## Requirements

- **Runtime:** JDK 21 (any distribution).
- **Database:** Embedded H2 (default - no setup) or Oracle (optional).
- **OS:** Windows, Linux, or macOS.

## Documentation

User-facing documentation lives alongside each release. For the changelog and high-level docs, see the release notes on the [Releases](https://github.com/nick2468/DataCrafter-releases/releases) page.

## Reporting Issues

Open an issue on this repository. Please include the version (`X.Y.Z`), OS, JDK version, and a snippet from `logs/datacrafter_server.log` if relevant.
