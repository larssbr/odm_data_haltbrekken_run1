# odm_data_haltbrekken_run1

Instructions to use with vagrant and opendrone map to create 3d map

1.) Follow instructions at https://github.com/OpenDroneMap/odm_vagrant to set up odm_vagrant
- vahrant up
- vagrant ssh

2.) Clone the Haltbrekken imagery repository https://github.com/larssbr/odm_data_haltbrekken_run1

- sudo apt-get -y install git
- cd /vagrant_data/
- git clone https://github.com/larssbr/odm_data_haltbrekken_run1

3.) Clone the OpenDroneMap application repository https://github.com/OpenDroneMap/OpenDroneMap.git

- sudo mkdir /odm_app
- sudo chown vagrant:vagrant /odm_app/
- cd /odm_app/
- git clone https://github.com/OpenDroneMap/OpenDroneMap.git

4.) Install the OpenDroneMap software:

- cd /odm_app/OpenDroneMap/
- ./install.sh

5.) Run the OpenDroneMap App on the an odm_data test dataset.

(not done here -- think i will swap pacifica with left or right folder name )
- cd /vagrant_data/odm_data/pacifica/
- /odm_app/OpenDroneMap/run.py

Wait patiently again, this will take about the same amount of time as the install proceedure.
Outputs will be in:
/vagrant_data/odm_data/pacifica/reconstruction-with-image-size-1200
and
/vagrant_data/odm_data/pacifica/reconstruction-with-image-size-1200-results

6.) If you are done processing imagery datasets, you can logout and shutdown the virutal machine.

sudo shutdown now

