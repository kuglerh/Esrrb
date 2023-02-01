# Esrrb

This site provides access to computational code and models for the paper:

Carbognin et al. 
Esrrb conveys naïve pluripotent cells through the formative transcriptional program

The Reasoning Engine Framework is open source and available at:
https://github.com/fsprojects/ReasoningEngine

The model was developed and tested on a Linux Ubuntu machine. We recommend the following VM instalation for 
initial evaluations of the framework and models:

https://zenodo.org/record/4041464#.Y9o9NnBBw2w

Dowmlaod the TACAS 21.ova file which can be run using Oracle VM VirtualBox or other standard Virtualization tools.

Follow the following instructions after running the VM:

# Submission mount point
export SD=/mnt/submission/artifact

# Give user access to VirtualBox shared folder
sudo usermod -aG vboxsf tacas21
su -p tacas21

# Install system packages and IFsharp
sudo dpkg -i $SD/packages/*.deb
mono $SD/ifsharp/ifsharp.exe --install

# Start jupyter with F# kernel
cd $SD/Examples
BROWSER=firefox jupyter notebook

# In the browser

 - Open ReasoningEngineBasics.ipynb
 - If asked, chose the F# kernel in Jupyter
 - Use the "Run" button to execute the cells in the notebook

The REIN files for model in Fig 8 is:



Additional examples from case studies published in other papers are made available in the following notebooks:
   - REIN.ipynb: Examples of using the RE:IN language to study stem cell decision making
   - YordanovDunnNSB2016.ipynb: Additional examples of using the RE:IN language to analyze various biological systems
   - RESIN.ipynb: Illustrates an extension of the RE:IN methodology that supports reasoning about switching interaction networks
   - Motifs.ipynb: Illustrates an extension of the RE:IN methodology that enables reasoning about function (dynamical behaviour) and structure (network motifs) of biological interaction networks





