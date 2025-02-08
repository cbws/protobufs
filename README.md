# CBWS API definitions

This repository contains the Protocol Buffers definitions of the public CBWS APIs. Use these files to make a client for a CBWS API in a language that does not have a CBWS SDK.

Each directory under `cbws/` contains one API version, for example `cbws/compute/v1alpha1`. The APIs follow the [Google API Improvement Proposals](https://google.aip.dev).

## Use the definitions

The definitions import files from [googleapis](https://github.com/googleapis/googleapis). The `buf.yaml` file in this repository gets these files from the Buf Schema Registry.

To generate code with [Buf](https://buf.build):

1. Install the Buf CLI.
2. Write a `buf.gen.yaml` file that names the plugins for your language.
3. Run `buf generate` in the root of this repository.

The services accept gRPC on port 443, for example on `compute.cbws.cloud:443`. The API reference at https://docs.cbws.cloud gives the endpoint of each API.

## Versions

The tags of this repository have the same version numbers as the CBWS API releases. An API with `alpha` or `beta` in its version can change in a way that is not compatible with earlier releases.

## Changes

CBWS makes changes to these APIs in an internal repository. A process copies the public part of each change to this repository. Each commit message describes the change to the public API.

This repository does not accept pull requests. To report a problem with an API, contact CBWS support.

## License

The definitions are available under the Apache License, Version 2.0. Refer to the `LICENSE` file.
