# Topology-Action Decoupling for Robust Multi-Agent Coordination

Code for the paper **"Topology-Action Decoupling for Robust Multi-Agent Coordination."**

This repository implements the TAD algorithm on both Multi-Agent Particle Environments (MPE) and StarCraft Multi-Agent Challenge (SMAC), together with the necessary baselines for comparison.

## Requirements

Environment assumptions:

- Python 3.9
- PyTorch 2.8.0
- GPU: NVIDIA RTX 4090

Install dependencies via:

```bash
pip install -r requirements.txt
```

## Training

Run the following commands to reproduce the results:

```bash
python src/main.py --config=hpostcn --env-config=mpe with env_args.map_name=pp_9v3_classical t_max=2050000
python src/main.py --config=hpostcn --env-config=sc2 with env_args.map_name=2s3z t_max=2050000
```

You can switch between MPE and SMAC through `--env-config`, and adapt the algorithm via `--config`.

## Hyper-parameters

Modify algorithm and environment configurations through:

```
src/config/algs/
src/config/default.yaml
src/config/envs/
```

## Note

This repository is developed on top of PyMARL, and we cite SMAC accordingly in our work.
