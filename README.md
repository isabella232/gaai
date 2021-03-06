# gaai - Artificial Intelligence Database Performance Tuning #

gaai automatically tunes a MySQL or Percona database server for highest performance as measured by qps (queries per second) using an Artificial Intelligence Genetic Algorithm. 

The tool could easily be expanded to become a full fledged tuner. My hope instead is that code similar to this will be added to the MySQL or Percona server and in time grow to cover many (towards 'all') variables with surrounding smart bits (memory calculations, variable tuning interactions etc.) for automatic tuning. The Genetic Algorithm engine itself can likely also be further improved by using more advanced Gentic Algorithms.

Setup/Prereq:
```
cd ~
git clone --depth=1 https://github.com/Percona-QA/gaai.git        # GPLv2
git clone --depth=1 https://github.com/Percona-QA/percona-qa.git  # GPLv2
sudo yum install util-linux   # or yum equivalent
```

Download a tarball version of Percona Server, unpack it in some directory, cd (change dir) to the same, and run startup:
```
cd /your_unpacked_tarball_dir
~/percona-qa/startup.sh   # This will create some handy scripts to use. This is optional as gaai.sh already does this too
```

Configure sysbench 
```
# Setup the Percona repo from https://www.percona.com/doc/percona-repo-config/apt-repo.html
sudo apt-get install sysbench   # or yum equivalent
```

Start gaai
```
cd ~/gaai
vi gaai.sh   # Edit variables like BASEDIR (point it to the extracted tarball directory above) and PERCONAQADIR (likely percona-qa in your home directory if you followed the instructions)
./gaai.sh
```

Stopping gaai
```
CTRL+C the running process, then execute
./gaai-stop.sh   # Or simply execute this from another shell session
```

Thank you credits
* Percona, the great company I work for
* My colleagues, who are always helpful
* My family, for always allowing me time
* https://github.com/Mimyka for the GA lua algo
* My Heavenly Father, for all I have and am
