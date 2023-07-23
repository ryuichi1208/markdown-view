# markdown-view

```
$ tree
.
├── Dockerfile
├── Makefile
├── PROJECT
├── README.md
├── cmd
│   └── main.go
├── config
│   ├── default
│   │   ├── kustomization.yaml
│   │   ├── manager_auth_proxy_patch.yaml
│   │   └── manager_config_patch.yaml
│   ├── manager
│   │   ├── kustomization.yaml
│   │   └── manager.yaml
│   ├── prometheus
│   │   ├── kustomization.yaml
│   │   └── monitor.yaml
│   └── rbac
│       ├── auth_proxy_client_clusterrole.yaml
│       ├── auth_proxy_role.yaml
│       ├── auth_proxy_role_binding.yaml
│       ├── auth_proxy_service.yaml
│       ├── kustomization.yaml
│       ├── leader_election_role.yaml
│       ├── leader_election_role_binding.yaml
│       ├── role_binding.yaml
│       └── service_account.yaml
├── go.mod
├── go.sum
└── hack
    └── boilerplate.go.txt
```

## help

```
$ make help

Usage:
  make <target>

General
  help             Display this help.

Development
  manifests        Generate WebhookConfiguration, ClusterRole and CustomResourceDefinition objects.
  generate         Generate code containing DeepCopy, DeepCopyInto, and DeepCopyObject method implementations.
  fmt              Run go fmt against code.
  vet              Run go vet against code.
  test             Run tests.

Build
  build            Build manager binary.
  run              Run a controller from your host.
  docker-build     Build docker image with the manager.
  docker-push      Push docker image with the manager.
  docker-buildx    Build and push docker image for the manager for cross-platform support

Deployment
  install          Install CRDs into the K8s cluster specified in ~/.kube/config.
  uninstall        Uninstall CRDs from the K8s cluster specified in ~/.kube/config. Call with ignore-not-found=true to ignore resource not found errors during deletion.
  deploy           Deploy controller to the K8s cluster specified in ~/.kube/config.
  undeploy         Undeploy controller from the K8s cluster specified in ~/.kube/config. Call with ignore-not-found=true to ignore resource not found errors during deletion.

Build Dependencies
  kustomize        Download kustomize locally if necessary. If wrong version is installed, it will be removed before downloading.
  controller-gen   Download controller-gen locally if necessary. If wrong version is installed, it will be overwritten.
  envtest          Download envtest-setup locally if necessary.
```
