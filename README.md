# Gaai - Artificial Intelligence Database Performance Tuning #

Gaai automatically tunes a MySQL database for highest performance as measured by tps (transactions per second) using a genetic algorithm

Setup/Prereq:
  cd ~
  git clone --depth=1 https://github.com/Percona-QA/gaai.git        # GPLv2
  git clone --depth=1 https://github.com/Percona-QA/percona-qa.git  # GPLv2, only script we use from this repo is startup.sh


Download a tarball version of Percona Server, unpack it in some directory, cd (change dir) to the same, and run startup:
  cd /your_unpacked_tarball_dir
  ~/percona-qa/startup.sh  # This will create some handy scripts to use