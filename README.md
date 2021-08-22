# MADHAWC
Development of MadDM for HAWC

* tested in CentOS 7 with miniconda 4.9.2 -> success
* tested in MAC OS Big Sur -> failed

## MADDM installation

bash

* Install presquities
```bash
conda create --name maddm -y -c conda-forge/label/cf201901 boost=1.63 cmake zeromq cppzmq matplotlib scipy python=2.7 
conda activate maddm
wget https://launchpad.net/mg5amcnlo/2.0/2.9.x/+download/MG5_aMC_v2.9.4.tar.gz
tar -zxvf MG5_aMC_v2.9.4.tar.gz
cd MG5_aMC_v2_9_4
sed -i 's/python3/python2/' ./bin/mg5_aMC
./bin/mg5_aMC
```

* Install MADDM
madgraph
```
install maddm
exit
```

* Run MADDM
bash
```bash
python2 ./bin/maddm.py
```

* Initialize MADDM
maddm 
```
import model DMsimp_s_spin0
define darkmatter xd
generate relic_density
add direct_detection
add indirect_detection
output PROC_myprocess
launch PROC_myprocess
```


