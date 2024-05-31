# NeuroHack

Break neural networks in your browser.

An interactive, in-browser demonstration of adversarial attacks on neural networks – entirely in JavaScript.

## Get Started

To run locally, just start up a web server using the example given below:

```
> python3 -m http.server
Serving HTTP on 0.0.0.0 port 8000 (http://0.0.0.0:8000/) ...
```

Click docs

## Implementation

adversarial.js is completely implemented in JavaScript – so it can run entirely within your browser. We rely on TensorFlow.js.

The library supports the following attacks:

- [Fast Gradient Sign Method](https://arxiv.org/pdf/1412.6572.pdf) (L_inf attack)
- [Basic Iterative Method](https://arxiv.org/pdf/1607.02533.pdf) (L_inf attack)
- [Jacobian-based Saliency Map Attack](https://arxiv.org/pdf/1511.07528.pdf) (L0 attack)
- [Jacobian-based Saliency Map Attack, One-Pixel](https://arxiv.org/pdf/1511.07528.pdf) (L0 attack)
- [Carlini & Wagner](https://arxiv.org/pdf/1608.04644.pdf) (L2 attack)

The demo can break the following pre-loaded systems:

- MNIST (digit recognition)
- GTSRB (street sign recognition)
- CIFAR-10 (object recognition, small images)
- ImageNet (object recognition, large images)

## Repo Structure

1. [`src/adversarial.js`](src/adversarial.js): The core adversarial.js library that implements all attacks.
2. [`docs/`](docs/): The interactive demo directory.
3. [`docs/js/`](docs/js/): Contains a ton of scripts that process data and power the demo, and a copy of `adversarial.js`.
4. [`docs/data/`](docs/data/): Contains (subsets) of datasets used in the demo.
