# on-the-emerging-potential-of-quantum-annealing-hardware 

The software and data in this repository comprise a snapshot of artifacts used in the production of the article [_On the Emerging Potential of Quantum Annealing Hardware for Combinatorial Optimization_](https://arxiv.org/pdf/2210.04291.pdf) by B. Tasseff, T. Albash, Z. Morrell, M. Vuffray, A. Y. Lokhov, S. Misra, and C. Coffrin.
This snapshot is based on the specific Ising model instances found in the `data` directory.
Snapshots of unprocessed experimental output are provided in the subdirectories of `results`.
Finally, various postprocessing utilities are provided in the `scripts` directory.

## Instances

First, to uncompress all Ising model instance data, execute
```bash
find data/instances/ -name "*.zip" -exec sh -c 'unzip -o "{}" -d "$(dirname "{}")"' \;
```

## Results

To uncompress all solver benchmarking results, execute
```bash
find data/results/ -name "*.zip" -exec sh -c 'unzip -o "{}" -d "$(dirname "{}")"' \;
```

### Subdirectory Naming

- `grd_dwave_*`
- `grd_scd_*`
- `ilp_gurobi_*`
- `iqp_cplex_*`
- `iqp_gurobi_*`
- `iqp_gurobipar_*`
- `mcmc_gd_*`
- `mp_ms_*`
- `pt_par_*`
- `pt_par_betamax_8_*`
- `qa0625_dwave_*`
- `sa_dwave_*`
- `svmc_par_*`
- `tabu_dwave_*`

## Citing

If you have found this repository useful in your work, please cite [the corresponding article](https://arxiv.org/pdf/2210.04291.pdf):
Below is a BibTeX entry that may be used:
```
@misc{tasseff+:arxiv22,
  title         = {On the Emerging Potential of Quantum Annealing Hardware for Combinatorial Optimization},
  author        = {Byron Tasseff and Tameem Albash and Zachary Morrell and Marc Vuffray and Andrey Y. Lokhov and Sidhant Misra and Carleton Coffrin},
  year          = {2022},
  eprint        = {2210.04291},
  archivePrefix = {arXiv},
  primaryClass  = {math.OC}
}
```

## License

This software is provided under a BSD-ish license with a "modifications must be indicated" clause.
See the `LICENSE.md` file for the full text.
This package is part of the Hybrid Quantum-Classical Computing suite, known internally as LA-CC-16-032.