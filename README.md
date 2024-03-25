# DevcloudSandbox
Because FPGA cards are pricey. 
# Commands
git clone --recursive https://github.com/codeplaysoftware/syclacademy.git
module load cmake
cd syclacademy
mkdir build
cd build
cmake ../ "-GUnix Makefiles" -DSYCL_ACADEMY_USE_DPCPP=ON -DSYCL_ACADEMY_ENABLE_SOLUTIONS=ON -DCMAKE_C_COMPILER=icx -DCMAKE_CXX_COMPILER=icpx

// If I don't request an interactive mode in a node, I won't be able to see my output.
qsub -I -l nodes=1:gpu:ppn=2 -d . // This is the command that requests for an interactive mode.

// To execute my source
bash my_shell_script_that_wraps_my_binary.sh

// Then, I should be able to see my output.
// Don't forget to exit.
exit
