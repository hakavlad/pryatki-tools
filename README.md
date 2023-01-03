# pryatki-tools

Hide files in other files and devices.

Just run the hider and answer the questions.

Hide the file:
```
$ ./hider
Select mode:
1 - insertion (insert file in other file)
2 - extraction (extract file from other file)
: 1
I: mode: insertion
Input file (file to hide): 1.mp4
I: input file real path: ['/home/user/PROJ/bin2/hider/1.mp4']
I: input file size: 6735011
Output file (container): 2.mp4
I: output file real path: ['/home/user/PROJ/bin2/hider/2.mp4']
I: output file size: 17622509
Initial position
(valid values are [0; 10887498], default=0): 1000000
I: initial position: 1000000
Output file will be partially overwritten.
Do you want to continue? (y|n): y
I: reading, writing, fsyncing...
I: written: 6735011, 6.4 MiB, 100.0% in 0.1s, avg 113.3 MiB/s
Remember this to extract the data from the container:
Initial position 1000000, Data size 6735011, Final position 7735011
SHA256: c3d8ad94410501dd0de8cd53097f53905016a712e186b4791d7e1e9ae287f766
OK
```

Extract the file:
```
$ ./hider
Select mode:
1 - insertion (insert file in other file)
2 - extraction (extract file from other file)
: 2
I: mode: extraction
Input file (container): 2.mp4
I: input file real path: ['/home/user/PROJ/bin2/hider/2.mp4']
I: input file size: 17622509
Output file: 3.mp4
I: output file real path: ['/home/user/PROJ/bin2/hider/3.mp4']
Initial position
(valid values are [0; 17622508], default=0): 1000000
I: initial position: 1000000
Data size to extract
(valid values are [1; 16622509], default=16622509): 6735011
I: data size to extract: 6735011
I: reading, writing, fsyncing...
I: written: 6735011, 6.4 MiB, 100.0% in 0.1s, avg 106.2 MiB/s
I: final position: 7735011
I: file extracted successfully
SHA256: c3d8ad94410501dd0de8cd53097f53905016a712e186b4791d7e1e9ae287f766
OK
```

### Requirements

Python 3.6+


