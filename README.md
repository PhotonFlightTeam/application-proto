### application-proto
A gRPC proto3 spec for communication between PhotonCore and
the PhotonFlight Electron application.

The API is split into:
- `application.proto`: gRPC services and their request/response messages
- `common.proto`: dataset, operation, plugin, and coordinate types
- `commands.proto`: typed commands sent from Electron to PhotonCore
- `events.proto`: events streamed from PhotonCore to Electron

`PointBatch` uses binary buffers so Electron
can turn the data into typed arrays without creating JavaScript
objects for every point.
In the future, `PointBatch` may be entirely replaced by
shared memory if we deem it as necessary for performance.

Use 
`git submodule add
https://github.com/PhotonFlightTeam/application-proto.git
proto`
to initialize this as a submodule into a project.

Use:
```text
git pull
git submodule update --init --recursive
```
To update the submodule.