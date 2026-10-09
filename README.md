### application-proto
A gRPC proto3 spec for PhotonFlight interop

Use 
`git submodule add
https://github.com/PhotonFlightTeam/application-proto.git
proto`
to initialize this as a submodule into a project.
The only projects which will initially depend on this will
be PhotonCore and PhotonFlight-React.

Use:
```text
git pull
git submodule update --init --recursive
```
To update the submodule.