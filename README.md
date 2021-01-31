# asr_labs

# Info

This repo contains the labs for the spring 2021 Automatic Speech Recognition course of the University of Edinburgh. The labs make use of Python, Jupyter notebooks and OpenFST. The labs will be uploaded periodically; if you are not familiar with git, just manually download the files you're missing or you might lose your work.


# Setup for UoE students
There's 4 main ways to have the environment for the labs and assigment set-up for remote work:
<ol>
<li>Use the <a href="http://computing.help.inf.ed.ac.uk/remote-desktop" target="_blank" rel="noopener noreferrer">remote desktop service</a></li>
<li>Use the <a href="http://computing.help.inf.ed.ac.uk/openvpn" target="_blank" rel="noopener noreferrer">informatics VPN</a></li>
<li>Use SSH tunneling</li>
<li>Run locally</li>
</ol>
<span style="text-decoration: underline;">1: Remote desktop</span>
<ol>
<li>Set up the <a href="http://computing.help.inf.ed.ac.uk/remote-desktop" target="_blank" rel="noopener noreferrer">remote desktop service</a></li>
<li>Connect to remote desktop</li>
<li>Open terminal on remote desktop</li>
<li>Run 'ssh s123456.lab.inf.ed.ac.uk'</li>
<li>Run these commands:</li>
</ol>
<pre>
git clone https://github.com/Ore-an/asr_labs.git
cd asr_labs
source /opt/conda/etc/profile.d/conda.sh
conda create -n asr_env python=3.7
conda activate asr_env
pip install openfst-python jupyter
jupyter notebook --ip=*</pre>
<span style="text-decoration: underline;"></span>
After the first setup do the first four step and then:

<pre>
source /opt/conda/etc/profile.d/conda.sh
conda activate asr_env
jupyter notebook --ip=*</pre>
If the token is not working, 'jupyter notebook password' lets you set a password.
<span style="text-decoration: underline;"></span>
<span style="text-decoration: underline;">2: VPN</span>
<ol>
<li>Set up the <a href="http://computing.help.inf.ed.ac.uk/openvpn" target="_blank" rel="noopener noreferrer">informatics VPN</a></li>
<li>Connect to the VPN</li>
<li>Open terminal</li>
<li>Run 'ssh s123456@s123456.lab.inf.ed.ac.uk'</li>
<li>Insert your DICE password</li>
<li>Run shared commands (add --ip=* after --no-browser)</li>
<li>Copy the link in the terminal to your browser</li>
</ol>
After the first setup, substitute the shared commands with
<pre>
source /opt/conda/etc/profile.d/conda.sh
conda activate asr_env
jupyter notebook --no-browser --ip=*</pre>
<span style="text-decoration: underline;"></span>
<span style="text-decoration: underline;">3: SSH tunneling</span>
<ol>
<li>Open terminal</li>
<li>Run 'ssh -J s123456@student.ssh.inf.ed.ac.uk -L 8888:localhost:8888 s123456@s123456.lab.inf.ed.ac.uk'</li>
<li>Insert your DICE password</li>
<li>Insert your DICE password again</li>
<li>Run shared commands</li>
<li>Copy the link that appears in the terminal and put it in your browser</li>
</ol>
After the first setup, substitute the shared commands with
<pre>
source /opt/conda/etc/profile.d/conda.sh
conda activate asr_env
jupyter notebook --no-browser</pre>

<span style="text-decoration: underline;">4:Run jupyter locally (<strong>NOT RECOMMENDED</strong>)</span>
<ol>
<li>Install python 3.7, virtualenv and graphviz</li>
<li>Run shared commands</li>
<li>Copy the link that appears on the terminal, open the browser and paste it in</li>
</ol>
After the first setup, substitute the shared commands with
<pre>
source /opt/conda/etc/profile.d/conda.sh
conda activate asr_env
jupyter notebook --no-browser</pre>

Shared commands:


<pre>
git clone <a href="https://github.com/Ore-an/asr_lab1.git" target="_blank" rel="noopener noreferrer">https://github.com/Ore-an/asr_labs.git</a>
cd asr_labs
source /opt/conda/etc/profile.d/conda.sh
conda create -n asr_env python=3.7
conda activate asr_env
pip install openfst-python jupyter
jupyter notebook --no-browser</pre>


After the first setup, connecting to the machine, activating the conda environment and starting the jupyter notebook will suffice.

We think the easiest option is to use the remote desktop, while the VPN and the SSH tunnel will give you the most responsive experience.
Running jupyter on your personal machine is not recommended, but you can do it, in a pinch, for the first few labs. The files we will use for the assignment are on the school's AFS filesystem and can't be copied locally for data protection. While it is possible to have <a href="http://computing.help.inf.ed.ac.uk/informatics-filesystem" target="_blank" rel="noopener noreferrer">AFS on your personal machine</a>, it's more complicated than just running the code on a lab machine and we don't have experience with the set-up, so we won't be able to provide tech support.

# For everybody else

Just make sure you have a version of Python between 3.5 and 3.7, then use pip to install openfst_python.
