# BestReduce: Optimized Parallel Reduction for Regular and Irregular Segments on GPU (DATA AND RESULTS)

---

# Citation

Please cite the corresponding papers if it was useful for your research:

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

---

## License

This project is licensed under the BSD 3-Clause License.
See the `LICENSE` file for details.

---

## Contact

Michel B. Cordeiro
Federal University of Paraná (UFPR)
Email: [michel.brasil.c@gmail.com](mailto:michel.brasil.c@gmail.com)
