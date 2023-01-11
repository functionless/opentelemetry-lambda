# OpenTelemetry Lambda
A fork of OpenTelemetry-lambda, with AWS XRAY and EMF exporters packaged in, for use in eventual lambda.
It is intended to be used as an extension on oltp-proxy-lambda, receiving traces and metrics and exporting them to xray and emf.

# To build for eventual
`GOARCH=arm64 make`

This will output `collector/build/collector-extension.zip`. This will need to be copied to `packages/@eventual/aws-runtime/otlp-proxy-lambda/collector-extension.zip` in the eventual codebase to be deployed as a lambda extension.
