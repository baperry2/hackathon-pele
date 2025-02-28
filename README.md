# Hackathon Profiling Scripts
Scripts for profiling NREL applications with HPCToolkit or Nsight Systems

====================================================

Not in the scripts, but handy is a command for using NSight Compute (ncu)
to profile Pele:

    srun -n 1 ncu --import-source true --set full -f -o pele-ncu-profile --nvtx --nvtx-include "Pele::ReactorCvode::cF_RHS()/" -c 3 ./PeleLMeX3d.gnu.TPROF.MPI.CUDA.ex inputs.3d_DodecaneQSS

====================================================

Instructions from Marc HdF on installing Nsight Systems UI (nsys-ui) on Kestrel:

    $ wget https://developer.nvidia.com/downloads/assets/tools/secure/nsight-systems/2025_1/NsightSystems-linux-public-2025.1.1.103-3542797.run
    $ bash NsightSystems-linux-public-2025.1.1.103-3542797.run # nothing like executing a random script from the internet ;) 
    # then boot a terminal in fastx
    $ ./install-location/bin/nsys-ui