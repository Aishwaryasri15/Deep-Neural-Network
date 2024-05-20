
# Deep Neural Network Compression

## Abstract
This project addresses the computational and storage challenges associated with Convolutional Neural Networks (CNNs) by proposing a novel pruning criterion inspired by neural network interpretability. Relevance scores for essential components, such as weights or filters, are automatically determined using explainable AI concepts. Demonstrated on the VGG16 model with the CIFAR-100 dataset, the compressed model outperforms previous criteria.

## Background
Traditional pruning methods yield sparse weight matrices, posing optimization challenges on general-purpose hardware. Structured pruning methods, removing complete channels, are devised to leverage pruning benefits on general-purpose devices.

## Methodology
- Unstructured pruning removes redundant or unimportant connections.
- Structured pruning removes entire channels or filters.
- Fine-tuning transfers strong learned representations to other domains.

## Implementation
- Input includes a pre-trained model, sparsity ratios, dataset batches, weight prune ratios, and criteria for unstructured global pruning and structured pruning.
- Output is a pruned model.
- Implementation is on the VGG-16 architecture.

## Results
- Pre-trained VGG-16 achieved 74.44% test accuracy and 1.055 test loss.
- After pruning and fine-tuning, the model achieved 74.15% test accuracy and 1.1855 test loss.

## Conclusion & Future Work
The report presents a method to derive a lightweight network from a fine-tuned network, reducing the model size from 527.802 MB to 46.334 MB (91.2% compression) with minimal accuracy drop. Future work involves iterative pruning implementation and exploring dynamic or post-training quantization on the obtained model.

