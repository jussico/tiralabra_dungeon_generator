# Testausdokumentti

Note: Tämän dokumentin sisältö tulee vielä lisääntymään huomattavasti kun varsinaisen koodin ja sitä myötä testien määrä lisääntyy. Myös ulkoasussa on vielä tekemistä.

## Testauksessa on käytetty kahta yleiskäyttöistä työkalua:
* /usr/bin/time
* python memory profiler

https://man7.org/linux/man-pages/man1/time.1.html

https://pypi.org/project/memory-profiler/

### Testausscriptit ovat hakemistossa testing/

``` bash
install_dependencies.sh
run_tests.sh
```

### Testien ajaminen

Testien ajaminen tapahtuu komennolla ```bash testing/run_tests.sh```

Tämä ajaa scriptissä määritellyt python-tiedostot sekä python 
memory profilerilla että ```/usr/bin/time``` -komennolla.

Tulokset kopioidaan doc/resources/ -hakemistoon josta
ne sisällytetään tähän dokumenttiin alla.

## Testien tulokset

### cave_generator.py

### /usr/bin/time

	Command being timed: "python src/cave_generator.py"
	User time (seconds): 0.04
	System time (seconds): 0.01
	Percent of CPU this job got: 34%
	Elapsed (wall clock) time (h:mm:ss or m:ss): 0:00.17
	Average shared text size (kbytes): 0
	Average unshared data size (kbytes): 0
	Average stack size (kbytes): 0
	Average total size (kbytes): 0
	Maximum resident set size (kbytes): 9940
	Average resident set size (kbytes): 0
	Major (requiring I/O) page faults: 0
	Minor (reclaiming a frame) page faults: 2830
	Voluntary context switches: 0
	Involuntary context switches: 0
	Swaps: 0
	File system inputs: 0
	File system outputs: 0
	Socket messages sent: 0
	Socket messages received: 0
	Signals delivered: 0
	Page size (bytes): 4096
	Exit status: 0

#### Python Memory Profiler

![alt text](resource/mp_report_cave_generator_default.png)
![alt text](resource/mp_report_cave_generator_flame.png)
![alt text](resource/mp_report_cave_generator_slope.png)

