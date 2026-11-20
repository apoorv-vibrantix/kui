# kui

Cloud-native command output is useful, but ASCII tables make it harder to scan resources and follow links between commands. kui adds a graphical interface to `kubectl` workflows so you can inspect results and open resources with less manual copying.

## Features

- Run `kubectl` commands through a graphical command-line experience.
- Render command results as sortable tables instead of plain ASCII output.
- Open Kubernetes resources by clicking names and links in the interface.
- Launch a built-in REPL for interactive command use.
- Build custom graphical CLI extensions with the Kui framework.
- Package the interface as a desktop application with Electron.

## Installation

Install dependencies from a source checkout:

```sh
npm ci
```

Build the Electron application for macOS on Intel:

```sh
npm run build:electron:mac:amd64
```

The packaged application is written to `./dist/electron`. Build targets for other platforms can be selected using the corresponding project script.

## Usage

With `kubectl` configured for a Kubernetes cluster, run:

```sh
kubectl kui get pods
```

You can also launch the installed macOS application directly:

```sh
open /Applications/Kui.app
```

## License

Apache-2.0. This project is based on [kubernetes-retired/kui](https://github.com/kubernetes-retired/kui) and retains attribution to that project under the Apache License 2.0.
