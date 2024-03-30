# setup-sigrelease-binary GitHub Action

This action is a generic installer for binaries released by the Kubernetes
Release Engineering team. This action is intended to be reused by other
actions to factor out some functionality such as downloading and 
signature verification.

## Usage

```yaml
  - uses: kubernetes-sigs/release-actions/setup-sigrelease-binary
    with:
      binary: release-notes

```

## Parameters

The action takes three parameters, only the binary name is required:

| Parameter | Required | Description |
| --- | --- | --- |
| `binary` | true | Name of the binary to download. |
| `version` | false | Version of the binary to download and verify. |
| `install-dir` | false | Directory to install the binary. It will be appended to the `$GITHUB_PATH` |

