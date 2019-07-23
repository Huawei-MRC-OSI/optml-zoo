Optimization frameworks for machine learning
--------------------------------------------

### Frameworks with low-level features (e.g. optimized for something special)

* <https://www.tensorflow.org/lite>
  - Small version of TF, targets mobile devices on Android and IoT

* <https://www.tensorflow.org/performance/xla/>
  - XLA (Accelerated Linear Algebra) is a domain-specific compiler for linear
    algebra that optimizes TensorFlow computations.
  - <https://haosdent.gitbooks.io/tensorflow-document/content/resources/xla_prerelease.html>
  - Has two modes: JIT and AOT. JIT is more like TFlite. AOT resembles TVM.

* <http://ngraph.nervanasys.com/docs/latest/>
  - nGraph (Intel, make business with PlaidML)

* <https://software.intel.com/en-us/openvino-toolkit>
  - OpenVINO (Intel).

* <https://github.com/xiaomi/mace>
  - 2018, MACE is a deep learning inference framework optimized for mobile heterogeneous computing platforms

* <https://github.com/Tencent/PocketFlow>
  - PocketFlow, a kind of Autotuner for TF?

* <https://github.com/Tiramisu-Compiler/tiramisu>
  - Tiramisu, Polyhedral compiler
  - Paper <https://arxiv.org/pdf/1804.10694.pdf>
    + 2018, Tiramisu: A Code Optimization Framework for High Performance Systems
  - Not mentioned:
    + Autodiff
    + Quantization
    + Python API

 * <http://eyeriss.mit.edu/>
   - CNN enegry-efficient optimizations, by MIT

* <https://github.com/Tencent/ncnn>
  - Something for fast inference on ARMs. Often used as a baseline for internal
    Huawei projects.

* <https://github.com/snipsco/tract>
  - NLP-optimized (?) inference framework for IoT
  - Well, SNIPS is about NLP, but Track targets MobileNet. Strange.
  - Claims that is optimized for streaming.

### Frameworks with higher-level features (e.g. auto-tuning)

* <https://github.com/google/jax>
  - Another project of Google
  - Has Autodiff through `numpy`, AFAIK, PyTorch-style.
  - Backed by XLA.

* <https://tvm.ai>
  - TVM itself. main feature is the Tensor-Expression language (with both auto-
    and manual-schedulings). Supports many frontends and backends, from
    Web(sic!) to GPUs to FPGAs and IoT. Level of support varies.
  - Has `Relay` for static typing and high-level frontend.
  - Has `muTvm` for IoT backends and bare-metal systems.
  - Autodiff is in PRs.

* <http://halide-lang.org/>
  - Halide is a source of inspiration for TVM. AFAIK, invented Tensor-Expression
    language for image processing.
  - Has autodiff since recently (merged or not?)
  - Initially was not intended for machine learning, but who knows..

* <https://github.com/plaidml/plaidml>
  - PlaidML - "PlaidML is the easiest, fastest way to learn and deploy deep
    learning on any device, especially those running macOS or Windows"
  - Main feature is AutoTuning (Search of optimizations)
  - (RIP?) Obtained by Intel

* <http://dlvm.org/>
  - Paper <https://arxiv.org/pdf/1711.03016>
    DLVM: A modern compiler infrastructure for deep learning systems (autodiff)
  - RIP in favor of TF-Swift

* <https://github.com/vgvassilev/clad>
  - Posters <https://llvm.org/devmtg/2013-11/slides/Vassilev-Poster.pdf>
    clad - Automatic Differentiation using Clang
  - RIP?

* <https://github.com/facebookresearch/TensorComprehensions>
  - A domain specific language to express machine learning workloads.
  - <https://arxiv.org/abs/1802.04730>
    Tensor Comprehensions: Framework-Agnostic High-Performance Machine Learning Abstractions
  - RIP?
  - Integrated into PyTorch
  - Like TVM, has Tensor-Expression language (with auto-schedulers)

