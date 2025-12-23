# `/pkg`

外部应用程序可以使用的库代码（例如 `/pkg/mypubliclib`）。其他项目会导入这些库，并期望它们能正常工作，所以在把东西放在这里之前请三思 :-) 请注意，`internal` 目录是确保您的私有包不被导入的更好方法，因为它是由 Go 强制执行的。`/pkg` 目录仍然是明确传达该目录中的代码可供他人安全使用的好方法。Travis Jeffery 的博客文章 [“我更喜欢 pkg 而不是 internal”](https://travisjeffery.com/ill-take-pkg-over-internal/) 很好地概述了 `pkg` 和 `internal` 目录，以及何时使用它们是有意义的。

当您的根目录包含许多非 Go 组件和目录时，这也是一种将 Go 代码分组到一个地方的方法，从而可以更轻松地运行各种 Go 工具（如这些演讲中所述：[“工业编程的最佳实践”](https://www.youtube.com/watch?v=PTE4VJIdHPg) 来自 GopherCon EU 2018，[GopherCon 2018: Kat Zien - 如何组织您的 Go 应用](https://www.youtube.com/watch?v=oL6JBUk6tj0) 以及 [GoLab 2018 - Massimiliano Pippi - Go 中的项目布局模式](https://www.youtube.com/watch?v=3gQa1LWwuzk)）。

请注意，这并不是一个被普遍接受的模式，对于每一个使用它的流行仓库，您都可以找到 10 个不使用它的仓库。是否使用此模式取决于您。无论它是否是一个好的模式，大多数人都会明白您的意思。对于一些新的 Go 开发人员来说，这可能会有点困惑，但这是一个非常容易解决的困惑，这也是本项目布局仓库的目标之一。

如果您的应用项目非常小，且额外的嵌套层级没有增加太多价值，那么不使用它也是可以的（除非您真的想用）。当项目变得足够大且根目录变得相当繁忙时（特别是如果您有许多非 Go 应用组件），请考虑使用它。

`pkg` 目录的起源：旧的 Go 源代码曾使用 `pkg` 作为其包目录，随后社区中的各种 Go 项目开始效仿这一模式（有关更多背景信息，请参阅 [Brad Fitzpatrick 的这条推文](https://twitter.com/bradfitz/status/1039512487538970624)）。


示例：

* https://github.com/containerd/containerd/tree/main/pkg
* https://github.com/slimtoolkit/slim/tree/master/pkg
* https://github.com/telepresenceio/telepresence/tree/release/v2/pkg
* https://github.com/jaegertracing/jaeger/tree/master/pkg
* https://github.com/istio/istio/tree/master/pkg
* https://github.com/GoogleContainerTools/kaniko/tree/master/pkg
* https://github.com/google/gvisor/tree/master/pkg
* https://github.com/google/syzkaller/tree/master/pkg
* https://github.com/perkeep/perkeep/tree/master/pkg
* https://github.com/heptio/ark/tree/master/pkg
* https://github.com/argoproj/argo-workflows/tree/master/pkg
* https://github.com/argoproj/argo-cd/tree/master/pkg
* https://github.com/heptio/sonobuoy/tree/master/pkg
* https://github.com/helm/helm/tree/master/pkg
* https://github.com/k3s-io/k3s/tree/master/pkg
* https://github.com/kubernetes/kubernetes/tree/master/pkg
* https://github.com/kubernetes/kops/tree/master/pkg
* https://github.com/moby/moby/tree/master/pkg
* https://github.com/grafana/grafana/tree/master/pkg
* https://github.com/influxdata/influxdb/tree/master/pkg
* https://github.com/cockroachdb/cockroach/tree/master/pkg
* https://github.com/derekparker/delve/tree/master/pkg
* https://github.com/etcd-io/etcd/tree/master/pkg
* https://github.com/oklog/oklog/tree/master/pkg
* https://github.com/flynn/flynn/tree/master/pkg
* https://github.com/jesseduffield/lazygit/tree/master/pkg
* https://github.com/gopasspw/gopass/tree/master/pkg
* https://github.com/sosedoff/pgweb/tree/master/pkg
* https://github.com/GoogleContainerTools/skaffold/tree/master/pkg
* https://github.com/knative/serving/tree/master/pkg
* https://github.com/grafana/loki/tree/master/pkg
* https://github.com/bloomberg/goldpinger/tree/master/pkg
* https://github.com/Ne0nd0g/merlin/tree/master/pkg
* https://github.com/jenkins-x/jx/tree/master/pkg
* https://github.com/DataDog/datadog-agent/tree/master/pkg
* https://github.com/dapr/dapr/tree/master/pkg
* https://github.com/cortexproject/cortex/tree/master/pkg
* https://github.com/dexidp/dex/tree/master/pkg
* https://github.com/pusher/oauth2_proxy/tree/master/pkg
* https://github.com/pdfcpu/pdfcpu/tree/master/pkg
* https://github.com/weaveworks/kured/tree/master/pkg
* https://github.com/weaveworks/footloose/tree/master/pkg
* https://github.com/weaveworks/ignite/tree/master/pkg
* https://github.com/tmrts/boilr/tree/master/pkg
* https://github.com/kata-containers/runtime/tree/master/pkg
* https://github.com/okteto/okteto/tree/master/pkg
* https://github.com/solo-io/squash/tree/master/pkg
* https://github.com/google/exposure-notifications-server/tree/main/pkg
* https://github.com/spiffe/spire/tree/main/pkg
* https://github.com/rook/rook/tree/master/pkg
* https://github.com/buildpacks/pack/tree/main/pkg
* https://github.com/cilium/cilium/tree/main/pkg
* https://github.com/containernetworking/cni/tree/main/pkg
* https://github.com/crossplane/crossplane/tree/master/pkg
* https://github.com/dragonflyoss/Dragonfly2/tree/main/pkg
* https://github.com/kubeedge/kubeedge/tree/master/pkg
* https://github.com/kubevela/kubevela/tree/master/pkg
* https://github.com/kubevirt/kubevirt/tree/main/pkg
* https://github.com/kyverno/kyverno/tree/main/pkg
* https://github.com/thanos-io/thanos/tree/main/pkg
* https://github.com/cri-o/cri-o/tree/main/pkg
* https://github.com/fluxcd/flux2/tree/main/pkg
* https://github.com/kedacore/keda/tree/main/pkg
* https://github.com/linkerd/linkerd2/tree/main/pkg
* https://github.com/opencost/opencost/tree/develop/pkg
* https://github.com/antrea-io/antrea/tree/main/pkg
* https://github.com/karmada-io/karmada/tree/master/pkg
* https://github.com/kuberhealthy/kuberhealthy/tree/master/pkg
* https://github.com/submariner-io/submariner/tree/devel/pkg
* https://github.com/trickstercache/trickster/tree/main/pkg
* https://github.com/tellerops/teller/tree/master/pkg
* https://github.com/OpenFunction/OpenFunction/tree/main/pkg
* https://github.com/external-secrets/external-secrets/tree/main/pkg
* https://github.com/ko-build/ko/tree/main/pkg
* https://github.com/lima-vm/lima/tree/master/pkg
* https://github.com/clastix/capsule/tree/master/pkg
* https://github.com/carvel-dev/ytt/tree/develop/pkg
* https://github.com/clusternet/clusternet/tree/main/pkg
* https://github.com/fluid-cloudnative/fluid/tree/master/pkg
* https://github.com/inspektor-gadget/inspektor-gadget/tree/main/pkg
* https://github.com/sustainable-computing-io/kepler/tree/main/pkg
* https://github.com/GoogleContainerTools/kpt/tree/main/pkg
* https://github.com/guacsec/guac/tree/main/pkg
* https://github.com/kubeovn/kube-ovn/tree/master/pkg
* https://github.com/kube-vip/kube-vip/tree/main/pkg
* https://github.com/kubescape/kubescape/tree/master/pkg
* https://github.com/kudobuilder/kudo/tree/main/pkg
* https://github.com/kumahq/kuma/tree/master/pkg
* https://github.com/kubereboot/kured/tree/main/pkg
* https://github.com/nocalhost/nocalhost/tree/main/pkg
* https://github.com/openelb/openelb/tree/master/pkg
* https://github.com/openfga/openfga/tree/main/pkg
* https://github.com/openyurtio/openyurt/tree/master/pkg
* https://github.com/getporter/porter/tree/main/pkg
* https://github.com/sealerio/sealer/tree/main/pkg
* https://github.com/werf/werf/tree/main/pkg
  
