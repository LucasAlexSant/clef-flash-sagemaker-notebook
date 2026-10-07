# Clef-Flash on SageMaker

Jupyter notebook for running a sample decision with [Cloudflare/Clef-Flash](https://huggingface.co/Cloudflare/clef-flash) on Amazon SageMaker.

## Setup

- Use a CUDA-enabled Python kernel.
- The notebook supports `ml.g5.12xlarge` (four A10G GPUs, with the backbone sharded across the GPUs) and `ml.g6e.xlarge` (one L40S GPU).
- Set notebook storage to at least 80 GB. The model weights take about 19.1 GB.
- Run the cells in order. The first model download can take a while.

The multi-GPU loader and the L40S configuration have not been validated on SageMaker. The model authors report testing the release on an H200. Stop the notebook instance after the run to stop compute charges; persistent storage may continue to incur charges.

The notebook downloads the model at runtime and does not include model weights. Clef-Flash is published under the Apache-2.0 license.
