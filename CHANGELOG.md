# Changelog

All notable changes to this project will be documented in this file. The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Unreleased

## 0.3.0

### Breaking changes

- Remove type parameterization of rules [#151](#151). For instance, learning rate is now always of the same type. This should not break straightforward user code, but may break break loading via BSON etc. Negative learning rates now lead to error. In some cases changes the default regulator from `eps(Float32)` to `1e-8`.