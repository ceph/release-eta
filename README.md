# release-eta

Estimates when the next upstream Ceph releases will land, from where each
release is in the release process and how long each stage has taken
historically. Its output is the release schedule page on ceph.io
(<https://ceph.io/en/users/releases/>), refreshed daily by a workflow in
[ceph/ceph.io](https://github.com/ceph/ceph.io).

The estimates are not official dates and are not reviewed by the release team.
The script was written with the help of an LLM.

## Usage

```
./release-eta.py                 # text summary of all active releases
./release-eta.py squid           # just one release
./release-eta.py --json out.json --html out.html
```

It runs with [uv](https://docs.astral.sh/uv/) (`uv run --script`), which
installs its one dependency, PyYAML. Set `GITHUB_TOKEN` (or be logged in with
`gh`) to avoid GitHub API rate limits.

## History

The script started in ceph/ceph.io#1232 and then ceph/ceph#72648; this
repository keeps its history from the latter.

## License

LGPL-2.1-or-later; see [COPYING-LGPL2.1](COPYING-LGPL2.1).
