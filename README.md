BBC (Boninsegna-Banisch-Clementi) domains:

Space Time Diffusion Map tools for identifying coherent domains in macromolecules

#---------------------------
Running Space Time Diffusion Map on a list of trajectory frames
#---------------------------

#---------------------------
INPUT:

*  path    (string):            path pointing to molecular files
*  topfile (string):            name of topology file (default .pdb format)
*  trajfile (string):           name of trajectory file (default .dcd format)

*  eps_list (list of floats):    list of epsilon values to be explored in successive runs of the algorihtm
*  my_idx   (list of integers):  list of indices identifying those frames in the trajectory to be considered in the calculation
                                (can be output from PCCA, HMM as in the main manuscript or even built from intuition)

*  out_file (string):           name of file where output is saved (default format is compressed .npz)

NB: Sample data is provided from DE Shaw fip35 microsecond trajectory so that a test calculation can be successfully completed
    Here, my_idx is generated randomly in the notebook.

#---------------------------
OUTPUT

for each value in eps_list, following quantities are saved
        *  Space Time Diffusion Matrix
        *  eigenvalues and eigenvectors
        *  number of frames used to build the matrix

#-----------------------------
NB If multiple trajectories are available, we suggest that the code is run on each of them separately
(sometimes memory and computing time may just not be large or long enough).

Then results can easily be combined by averaging the Space Time Diffusion matrices, each of them properly weighted by the number
of configurations used to compute it (equilibrated trajectories are of course assumed).
#-----------------------------

TODO: ASSOCIATE EACH CELL OF NOTEBOOK WITH EQUATIONS FROM SUPPORTING INFORMATION TO THE MAIN PAPER!!
