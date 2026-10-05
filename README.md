# BestReduce: Optimized Parallel Reduction for Regular and Irregular Segments on GPU (DATA AND RESULTS)

---
> **This repository contains the experimental data, results, and materials used in the BestReduce paper.**
>
>  **The BestReduce source code is maintained in a separate repository:**\
>  **[BestReduce — Source Code](https://github.com/MichelBC/bestReduce.git)**

This repository is **not the implementation of BestReduce**. Instead, it provides the **results and experimental data** supporting the research presented in the paper, including the data used to generate its tables and plots.

## BestReduce Source Code

The BestReduce implementation is available in the [BestReduce source code repository](https://github.com/MichelBC/bestReduce.git), which contains the CUDA implementation and all the code required to reproduce the performance experiments and results presented in this work.

👉 **[Go to the BestReduce source-code repository](https://github.com/MichelBC/bestReduce.git)**

> **This repository focuses specifically on the experimental data and results.**

# Citation

If you find the BestReduce results, data, or analysis useful in your research or projects, we'd really appreciate it if you could cite our paper:

```bibtex
@article{cordeiro2025bestreduce,
  title={Optimized Parallel Reduction for Regular and Irregular Segments on GPU},
  author={Cordeiro, Michel B. and Zola, Wagner M. N.},
  journal={Concurrency and Computation: Practice and Experience},
  year={2025}
}
```

---

# Overview

**BestReduce** is a high-performance CUDA implementation of:

* Non-segmented parallel reduction
* Segmented parallel reduction (regular and irregular segments)

The core contribution is a **runtime-adaptive segmented reduction algorithm** that dynamically selects the most efficient kernel based on the segment size.

Unlike existing GPU libraries that rely on a fixed granularity model, BestReduce implements multiple specialized kernels and selects among them automatically. Additionally, it includes a tuning algorithm that identifies the best kernel for different segment size ranges.

---

## Paper Results

The implementation includes comparisons with:

* **NVIDIA CUB library**
* **NVIDIA Thrust library**

All experiments in the paper were performed with:

* 32 million elements
* Maximum reduction operator
* Average throughput reported in **Giga-elements/s**

All result data is available in the LibreOffice sheet located in the **'results'** folder. This file contains detailed instructions on how to generate each table and plot from the paper.

LibreOffice Version: 25.8.4.2

---

## License

This project is licensed under the BSD 3-Clause License.
See the `LICENSE` file for details.

---

## Contact

Michel B. Cordeiro
Federal University of Paraná (UFPR)
Email: [michel.brasil.c@gmail.com](mailto:michel.brasil.c@gmail.com)
