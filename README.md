<!-- It seems that github simply ignores the "style" tags within div tags... so try something different -->
<p align=center>
<a href="http://icarus.lngs.infn.it"><img src="http://icarus.lngs.infn.it/img/n3.jpg" alt="ICARUS Experiment" style="border:0"></a>
</p>

<h1 align=center><font color="blue"><font size="7">ICARUS Signal Processing</font></font></h1><br>
<p align=center>
<font color="gray"><font size="3">A repository aimed at collecting tools and notebooks useful for studying waveforms/ROI/hit finding <br>with the ICARUS LAr TPC</font></font><br>
</p>


<h2><font color="blue"><font size="5">General Directory Structure</font></font></h2>
<ul>
    <li><b>sigproc_tools</b> - This folder is broken into two parts:</li>
        <ul>
            <li><b>sigproc_functions</b> - A collection of python modules defining functions useful for stuying noise and developing filtering techniques </li>
            <li><b>sigproc_objects</b> - A collection of python classes for accessing the data to be analyzed</li>
        </ul>
    <li><b>plotting</b> - A collection of useful function definitions for making specific types of plots</li>
    <li><b>notebooks</b> - A collection of example Jupyter notebooks for performing specific analyes</li>
</ul>

<h2><font color="blue"><font size="5">Prerequisites for running</font></font></h2>
<ul>
    <li>The interface are python modules which are designed to be run in jupyter notebooks. Example jupyter notebooks are provided, to be able to execute them you will need:</li>
    <ul>
        <li>The modules are designed to run in python 3.6 or above (tested in 3.7)</li>
        <li>One will need access to the standard python include packages numpy, scipy and matplotlib</li>
        <li>Access to the input root data files is with the <a href="https://uproot.readthedocs.io/en/latest/">uproot package</a> where you can find instructions on installaion (e.g. through pip or conda)</li>
        <li>Graphics output is performed with the <a href="https://plotly/python/">plot-ly</a> package which provides for a nice interactive user experience (though, warning, can be memory intensive), installation instructions can be found on the linked page (e.g. using pip or conda)</li>
        <li>Also useful for the 3D event views is the <a href="https://ipywidgets.readthedocs.io/en/latest/">ipywidgets</a> package those this is not required for the basic analysis. Again installation instructions are on the linked page</li>
        <li>Finally, you will need to be able to run a <a href="https://jupyter-notebook.readthedocs.io/en/stable/">jupyter notebook</a>
    </ul>
    <li>The main idea is to have this installation running on your laptop (e.g. the above works nicely on a macbook pro) with input data files copied to your local machine. However, provided the above libraries are available, no reason to not run the cro-magnon form (i.e. over network to an icarus gpvm machine)</li>
</ul>

<h2><font color="blue"><font size="5">Installing</font></font></h2>
<ul>
    <li>Create a working area on your machine where you will copy the input files and set up this repository</li>
    <li>Navigate to that folder
    <li>git clone https://github.com/SFBayLaser/icarus-sigproc-tools </li>
    <li>Copy one of the example notebooks fromt the repository folder to your working folder (it is not recommended to open them directly since this will create a cache folder and, more important, when you execute the notebook it will create arrays and images which are quite large - it would not be good to upload those back to the root repository!)</li>
    <li>Open the notebook and in the first code block that is highlighted with "TODO" be sure to replace the path you see there with the full path to folder which contains the signal processing tools repository</li>
    <li>In the second "TODO" block set the fully qualified path to the location of your data files and the name of the file you want to read</li>
</ul>

<h2><font color="blue"><font size="5">Running</font></font></h2>
<ul>
    <li>Generally, in my terminal window I navigate to the working directory which contains the data files and a copy of the notebook I want to run. I tend to run jupyter notebook which, if run on my mac, will automatically open a windown in my default browser window display a directory of the folder I'm starting in. From here I can should see the notebook I want to run listed and can simply click on that to get it started. From there it is standard jupyter stuff</li>
    <li><b>It is important to note that all of this code is designed to work on "swizzled" data!</b><br>This means the raw test data files must first be converted so the files contain "RawDigit" format TPC data.</li>
</ul>

<h2><font color="blue"><font size="5">TODO</font></font></h2>
<ul>
    <li>Implementation of the full set of TPC responses functions (currently only electronics response available)</li>
    <li>What is the correct number of channels to group for coherent noise subtraction? 32 or 64?</li>
    <li>Develop algorithm for signal protection with the coherent noise subtraction</li>
    <li>After coherent noise subtraction, what is the source of the remnant noise observed?</li>
    <li>Develop a more sophisticated approach to overlaying a fake particle on existing waveforms</li>
    <ul>
        <li>Need protection for cases when input variables result in out of range parameters</li>
        <li>Need to change input parameters to #electrons with internal converstions</li>
        <li>etc.</li>
    </ul>
    <li>Implement the current deconvolution and ROI algorithms here for faster turnaround studies</li>
    <li>And this is just to start!</li>
</ul>

<h2><font color="blue"><font size="5">Problems/Complaints/Hate mail</font></font></h2>
<ul>
    <li>Currently, all questions and/or complaints should be sent to <a href="mailto:usher@slac.stanford.edu">Tracy Usher</a></li>
</ul>

