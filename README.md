# DevcloudSandbox
Because FPGA cards are pricey. 
# Commands
git clone --recursive https://github.com/codeplaysoftware/syclacademy.git 
<br>
module load cmake<br> 
cd syclacademy <br>
mkdir build <br>
cd build <br>
cmake ../ "-GUnix Makefiles" -D SYCL_ACADEMY_USE_DPCPP=ON -D SYCL_ACADEMY_ENABLE_SOLUTIONS=ON -D CMAKE_C_COMPILER=icx -D CMAKE_CXX_COMPILER=icpx<br>
<br>
// If I don't request an interactive mode in a node, I won't be able to see my output. <br>
<br>
qsub -I -l nodes=1:gpu:ppn=2 -d . // This is the command that requests for an interactive mode.<br>
<br>
// To execute my source <br>
<br>
bash my_shell_script_that_wraps_my_binary.sh
<br>
// Then, I should be able to see my output. 
<br>
// Don't forget to exit. 

exit
