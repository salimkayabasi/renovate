# Renovate Preset

## Usage

Simply create a file as `.github/renovate.json` and extend the configuration as shown below.

`renovate` will access this repository and use the config sets (`default.json`):
```json
{
  "extends": [
    "github>salimkayabasi/renovate"
  ]
}
```
More than one config preset can be referenced. This configuration will use `default.json` and `other-preset.json`:

```json
{
  "extends": [
    "github>salimkayabasi/renovate",
    "github>salimkayabasi/renovate:other-preset"
  ]
}
```

## Config Preset Validation

After a config preset has been changed, it should be validated.

First install the dependencies:

```console
npm install
```

Then validate all config presets:

```console
.github/scripts/validate.sh
```
