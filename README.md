# Shared-SIMS-DB

This repository serves as the metadata registry for simulations and experimental datasets produced within our research group. Its purpose is to ensure:

1. Scientific reproducibility/restartability
2. Long-term preservation of simulation knowledge
3. Transparent sharing of data and setup details
4. Structured linkage between simulations and experiments
5. Avoidance of duplicated work

This repository stores metadata only. Large data files (plasma outputs, restart files, meshes, etc.) must be stored in shared project storage (ISAAC work directory)and must not be committed to GitHub. The structure of the shared storage on ISAAC, will follow the example structure:

/lustre/isaac24/proj/UTK0325/Casali_Shared_SIMS_DB/
    SIM_ID/
        mesh/
        restart_files/plasma_final.h5
        results_files/large_postprocessed_data
        
The metadata file must contain the absolute path to this directory.The structure of the following archive is given as: 

Shared-SIMS-DB/
│
├── README.md
├── TEMPLATE_simulation.yml (instructions to fulfill the metadata for simulations)
├── TEMPLATE_experiment.yml (instructions to fulfil the metadata for experiments)
│
├── simulations/
│     ├── SIMID_name/
│     │     ├── metadata.yml
│     │     └── README.md
│     ├── ...
│
├── experiments/
│     ├── EXPID_name/
│     │     └── metadata.yml
│     ├── ...
│
└── scripts/
      └── (postprocessing and any other relevant script produced)
      
A simulation is considered archived only if:
1. Metadata is completed
2. Full input case is stored in shared storage

Experimental datasets used for validation or comparison should also be registered, including diagnostic information and data storage location.
