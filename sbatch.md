# sbatch running


      #!/bin/bash
      #SBATCH --ntasks=2
      #SBATCH --cpus-per-task=2
      #SBATCH --ntasks=2 --cpus-per-task=2
      # module load ANSYS_CFD/19.3
      echo "Date              = $(date)"
      echo "Hostname          = $(hostname -s)"
      echo "Working Directory = $(pwd)"
      echo ""
      echo "Number of Nodes Allocated      = $SLURM_JOB_NUM_NODES"
      echo "Number of Tasks Allocated      = $SLURM_NTASKS"
      echo "Number of Cores/Task Allocated = $SLURM_CPUS_PER_TASK"
      module load Python/3.8.6-GCCcore-10.2.0
      python 'spectrum of circulant graphs.py'
      echo "Date              = $(date)"
