# remi

`remi` installs Remi, a personal assistant with a long memory, on your own computer or server with Docker, and looks after it.

```bash
curl -fsSL https://github.com/adithya1123/remi-releases/releases/latest/download/install.sh | sh
remi setup
```

This repository holds remi's releases and nothing else. Each one has remi for macOS and Linux (amd64 and arm64), their
`SHA256SUMS` (install.sh and `remi update` check them), `VERSION`, and `install.sh`. Remi's images are private: whoever gave
you Remi gives you access to them.

Each archive carries `LICENSE`: remi and Remi are for the people they were given to, to use.
