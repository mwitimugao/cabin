# cabin

Managing Kubernetes resources from a phone can be difficult when you need a quick view of cluster state or a small operational change. cabin provides a mobile interface for viewing and modifying Kubernetes resources from iOS and Android devices.

## Features

- Add existing Kubernetes clusters and create clusters on GKE.
- View pods and other resources by namespace, with label-based search.
- Delete pods with a swipe, edit labels, and scale deployments with touch controls.
- Read pod logs and run simple exec commands in containers.
- Change deployment images to trigger rolling updates and view resource YAML.
- Browse Helm chart repositories and launch charts. Helm support is still under development.

## Installation

cabin is a React Native JavaScript application. Install the React Native CLI and follow the platform prerequisites in the [React Native getting started guide](https://facebook.github.io/react-native/docs/0.48/getting-started.html).

```sh
npm install -g react-native-cli
yarn install
yarn start
```

For iOS, install CocoaPods and the native dependencies:

```sh
gem install cocoapods
cd iOS/ && pod install
```

Keep the packager running, then launch the app from another terminal. For Android:

```sh
npx react-native run-android
```

For iOS:

```sh
npx react-native run-ios
```

## Usage

Start the packager and launch cabin on a simulator:

```sh
yarn start
npx react-native run-ios --simulator="iPhone 15"
```

After the app starts, add a Kubernetes cluster, select a namespace, and open a resource list. From the resource views, you can inspect workloads, read pod logs, edit labels, scale deployments, or change a deployment image.

## License

cabin is licensed under the Apache License 2.0. This project is based on [vmware-archive/cabin](https://github.com/vmware-archive/cabin), and retains attribution to that project and its contributors. See [LICENSE](LICENSE) for the full license text.
