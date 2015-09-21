# Resource management
Conquest is designed to exhibit particularly good weak scaling, where the number
of atoms per core is fixed and number of cores varied to increase system size.
We show detailed strong and weak scaling in Figs. 1 & 2.

Figure 1: (a) Timing spent for parallel matrix multiplications in the
calculations of bulk Si system having 32,768 atoms. Timing of two subroutines
mainly for computation part and that of a subroutine for communication part are
plotted for two cases with or without calling MPI test. (b) Timing spent for
optimizing density matrix for bulk Si systems having various number of atoms,
using different number of CPUs.

Figure 2: (left) Strong scaling for Ge hut cluster on Si(001) with 11,620 atoms
in unit cell, using between 16 and 512 cores (middle). Strong scaling for Ge hut
cluster on Si(001) with 22,346 atoms, using between 64 and 288 cores. Efficiency
is defined as actual speed up divided by increase in number of cores. (right)
Weak scaling for bulk silicon cells with 512 atoms per core, increasing number
of cores. Note that the time plotted is total time–i.e. summed over all cores.
The system demonstrates perfect linear scaling, while time per core is
invariant, indicating excellent parallelization.

The grant is split into two parts: 40,702 kAUs in the first six months (not
47,702 as in the Technical Assessment where a 7 was substituted for a 0 in
error); 100,000 kAUs in the second six months.  These will be divided roughly
as:
   * First part: 50 small jobs (500 cores, 12 hours, 24GB memory per node); 40 medium
jobs (2000 cores, 12 hours, 24GB memory per node);2 large jobs (16,000 cores, up
to 48 hours, 24GB memory per node).
   * Second part: 10 medium jobs and 8 large jobs (specifications as before).

The storage required for each run will not exceed 200GB (allowing 10MB output
per process for large jobs) and we request 5TB of RDF storage to allow long-term
storage and analysis of trajectories.

The project will build on existing work investigating the nanowires, and will
start will small, characterisation runs (see workplan).  As these progress, our
medium jobs will allow the initial production runs to be performed (up to 40,000
atom simulations over timescales up to 1ps).  We will run two of the largest
jobs in the first period of the project to ensure that we understand the
challenges and results likely to come from these.

The second period will involve the main production runs, with the specific
simulations to be decided based on the results from the first period, and
consultation with our experimental colleagues in Japan.
