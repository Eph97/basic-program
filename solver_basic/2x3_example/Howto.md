To implement this example, please do as follows:
1) Download the following data files into a directory of your choice: cap_data.csv, shock_data.csv, util_data.csv. Observe the path for this directory, using "pwd" on linux/mac if desired. Create a sub-directory in this directory called "assignment_data"
2) Download the following Julia file from the "solver_basic" folder of this Github repository into the directory you just created: pkgs2add.jl. Once you have done this, open the file in an editor and exchange the directory path from step 1 for "/Users/joshuapurtell/Desktop/Strack_Project/" in lines 18-20. 
3) Download the following Julia files from the "solver_basic" folder of this Github repository into the directory you created in step 1: problem_generator.jl, problem_solver.jl. Choose a file name for the destination of the optimal assignment data. Once you have done this, open "problem_solver.jl" in an editor, and substitute  "directory path from step 1/assignment_data/file name for the destination of the optimal assignment data" for "/Users/joshuapurtell/Desktop/Strack_Project/assignment_data/a_data@$num_objects,$num_types.csv" at line 77. 
4) Open the Julia IDE (code should be updated for Julia v 1.2). Enter the following commands: 
      include("directory path from step 1/pkgs2add.jl")
      include("directory path from step 1/problem_generator.jl")
      include("directory path from step 1/problem_solver.jl")
      compos("directory path from step 1/util_data.csv","directory path from step 1/shock_data.csv","logistic","directory path       from step 1/cap_data.csv")
By inputing "logistic", you are choosing a logistic distribution. "compos" is a function which composes the problem            solver and generator functions.
5) The assignment array should appear as output, but feel free to check "directory path from step 1/assignment_data/file name for the destination of the optimal assignment data" to make sure that the array was written, as intended.