# DataCrafter Releases

This repository hosts public release downloads for **DataCrafter**, a self-hosted data engineering platform (Java 25 / Spring Boot 4).

The source code is maintained in a private repository. This repo exists solely to make built artifacts available for download.

## Downloads

Browse the [Releases](https://github.com/DataCrafter-SL/DataCrafter-releases/releases) page. Each release includes:

- `datacrafter-server-X.Y.Z.zip` - Server bundle. Contains the server JAR, the web client and the Excel add-in it serves, launch scripts (`bin/run.bat`, `bin/run.sh`, `bin/stop.bat`, `bin/stop.sh`), schema, password, backup and update tools, and a default `DataCrafter.properties`. Run `bin\run.bat` (Windows) or `bin/run.sh` (Linux/macOS) after extracting, then read `QUICKSTART.md`.

  The zip includes a 30-day trial `DataCrafter.key`, so the server starts straight away. For a full licence key, contact the vendor, and replace the trial `DataCrafter.key` beside `datacrafter-server.jar` with it.

- `datacrafter-client-X.Y.Z.zip` - Desktop client bundle. Contains the desktop client JAR and launch scripts (`run.bat`, `run.sh`). Connects to a running DataCrafter server.

## Container image

The server also comes as a container image, for Linux on amd64 and arm64, with its own Java.
Anyone can pull it, with no account:

```bash
docker pull ghcr.io/datacrafter-sl/datacrafter:latest
docker run -d --name datacrafter -p 127.0.0.1:8080:8080 -v datacrafter-data:/data --memory 2g --stop-timeout 45 ghcr.io/datacrafter-sl/datacrafter:latest
```

Then open http://localhost:8080 and sign in as `trial` / `trial`.

`latest` names the newest release. Each release also has its own tag, `X.Y.Z`; use that in a
command you keep. The registry keeps the three newest releases; for an older one, use its zip.

The image runs the same 30-day trial key as the zip, H2 only, under the terms in
`LICENSE-TRIAL.txt` (in the container at `/data/LICENSE-TRIAL.txt`). Its
`/data/THIRD-PARTY-NOTICES-IMAGE.txt` lists the Java runtime and Linux packages it holds. The
server zip's `README.md`, section "Running it in a container", covers upgrades, backups and
everything else. An image with the Standard key comes with the first free release.

## Requirements

- **Runtime:** JDK 25 (any distribution) (not needed for the container image).
- **Database:** Embedded H2 (default - no setup) or Postgres or Oracle.
- **OS:** Windows, Linux, or macOS.

## Documentation

User-facing documentation lives alongside each release. For the changelog and high-level docs, see the release notes on the [Releases](https://github.com/DataCrafter-SL/DataCrafter-releases/releases) page.

## Reporting Issues

Open an issue on this repository. Please include the version (`X.Y.Z`), OS, JDK version, and a snippet from `logs/datacrafter-server.log` if relevant.
