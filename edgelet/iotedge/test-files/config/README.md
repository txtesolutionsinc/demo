This directory contains test files for the `iotedge config apply` and `iotedge config import` tests.

For each test, `old-config.yaml` is the old iotedged config, and when given to `iotedge config import` should produce the super-config in `super-config.toml`. This super-config, when given to `iotedge config import`, should produce the five services' configs in `keyd.toml`, `certd.toml`, `identityd.toml`, `tpmd.toml` and `edged.toml`. In the tests that involve a symmetric key, the `device-id` file stores the contents of the `/var/secrets/aziot/keyd/device-id` file that holds the symmetric key and is preloaded into keyd.