# DataCrafter Releases

This repository hosts public release downloads for **DataCrafter**, a self-hosted data engineering platform (Java 25 / Spring Boot 4).

The source code is maintained in a private repository. This repo exists solely to make built artifacts available for download.

## Downloads

Browse the [Releases](https://github.com/DataCrafter-SL/DataCrafter-releases/releases) page. Each release includes:

- `datacrafter-server-X.Y.Z.zip` - Server bundle. Contains the server JAR, the web client and the Excel add-in it serves, launch scripts (`bin/run.bat`, `bin/run.sh`, `bin/stop.bat`, `bin/stop.sh`), schema, password, backup and update tools, and a default `DataCrafter.properties`. Run `bin\run.bat` (Windows) or `bin/run.sh` (Linux/macOS) after extracting, then read `QUICKSTART.md`.

  The zip includes a 30-day trial `DataCrafter.key`, so the server starts straight away. For a full licence key, contact the vendor, and replace the trial `DataCrafter.key` beside `datacrafter-server.jar` with it.

- `datacrafter-client-X.Y.Z.zip` - Desktop client bundle. Contains the desktop client JAR and launch scripts (`run.bat`, `run.sh`). Connects to a running DataCrafter server.

## Requirements

- **Runtime:** JDK 25 (any distribution).
- **Database:** Embedded H2 (default - no setup) or Postgres or Oracle.
- **OS:** Windows, Linux, or macOS.

## Documentation

User-facing documentation lives alongside each release. For the changelog and high-level docs, see the release notes on the [Releases](https://github.com/DataCrafter-SL/DataCrafter-releases/releases) page.

## Reporting Issues

Open an issue on this repository. Please include the version (`X.Y.Z`), OS, JDK version, and a snippet from `logs/datacrafter-server.log` if relevant.
