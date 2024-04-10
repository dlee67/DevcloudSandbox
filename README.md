# DevcloudSandbox
Because FPGA cards are pricey. 
# Commands
git clone --recursive https://github.com/codeplaysoftware/syclacademy.git 
<\b>
module load cmake<\b> 
cd syclacademy <\b>
mkdir build <\b>
cd build <\b>
cmake ../ "-GUnix Makefiles" -D SYCL_ACADEMY_USE_DPCPP=ON -D SYCL_ACADEMY_ENABLE_SOLUTIONS=ON -D CMAKE_C_COMPILER=icx -D CMAKE_CXX_COMPILER=icpx<\b>
<\b>
// If I don't request an interactive mode in a node, I won't be able to see my output. <\b>
<\b>
qsub -I -l nodes=1:gpu:ppn=2 -d . // This is the command that requests for an interactive mode.<\b>
<\b>
// To execute my source <\b>
<\b>
bash my_shell_script_that_wraps_my_binary.sh
<\b>
// Then, I should be able to see my output. 
<\b>
// Don't forget to exit. 

exit
