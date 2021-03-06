# bdat

Wraps https://github.com/maxogden/dat with new commands.
Used by https://github.com/pfraze/beaker.

Currently adds: `version`.

```
bdat <directory>

  share directory and create a dat-link

  --snapshot            create a snapshot of directory
  --port, -p            set a specific inbound tcp port

bdat version 

  get the current version

bdat version major|minor|patch|prerelease|<semver>

  write a new version to the dat

bdat <dat-link> <directory>

  download a dat-link into directory

  --list                print file list for dat-link
  --exit                exit process after download finishes
  --port, -p            set a specific inbound tcp port

general options

  --version, -v         get installed dat version
  --doctor              run dat doctor
  --quiet, -q           output only dat-link, no progress information
  --debug               show debugging output
```

## About the additions

### version

The `version` command writes a semver to `.bdat-version`.
Beaker scans the hyperdrive feed for changes to that file, to detect version updates.