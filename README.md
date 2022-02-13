# NTHU-Distributed-System

The repository includes modules for the NTHU Distributed System course lab with mono-repo architecture.

Before going through the following parts, make sure your Docker is running since we are generating/testing/building code inside a Docker container to prevent dependencies from conflicting/missing on your host machine.

## Code Generation

Some modules use gRPC for communication or use the `mockgen` library for unit testing.

So there is a need to generate code manually when the code changed.

For generating code for all modules, run `make dc.generate`.

For generating code for a single module, run `make dc.{module}.generate`. For example: `make dc.video.generate`.

## Unit testing

We implements unit testing through DAO and service layers.

To run unit testing for all modules, run `make dc.test`.

To run unit testing for a single module, run `make dc.{module}.test`. For example: `make dc.video.test`.
