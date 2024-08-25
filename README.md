# Keystroke Dynamics Dataset IKDD
This repository contains a dataset that proposed in the paper  "IKDD: A Keystroke Dynamics Dataset for User Classification". The keystroke dynamics dataset presented in this paper, named IKDD, was created from the daily computer typing of a large number of volunteers. Its use can help researchers to design systems for classifying users according to some of their inherent or acquired characteristics, in order to develop applications related to digital forensics, targeted advertising, ease of use of computing systems, the protection of unsuspecting users in cases of Internet fraud, etc.

IKDD contains a large amount of data, with each logfile having data from approximately 3500 keystrokes, thus adequately capturing the typing behavior of each volunteer. Also it contains data from the recording of 164 volunteers, from five different mother tongues, belonging to various educational levels, while gender, age group, and handedness are represented in the dataset with proportions that are also presented in the world population. For example, there are about as many females as males, while the ratio of left-handers to right-handers is 1 to 9. However, the dataset needs to be extended with the participation of more volunteers.

# Dataset Description
This dataset is named IKDD (IRecU’s Keystroke Dynamics Dataset) [23] and consists of several files, each of which were derived from a raw data dataset logfile. Each IKDD file includes the demographics of the volunteer recorded and a set of records, each of which maps to a keystroke dynamics feature and lists the values of that feature and that volunteer, in that particular logfile. Such a record has the following form:
x–y, value1, value2, value3, …	where x and y are the virtual key codes of the keys participating in the feature, and where value1, value2, value3, etc., are the values recorded for this feature. When y has the value 0, then the feature is keystroke duration, while when it has any other value, then the feature is down–down digram latency.
Some rules were followed for the extraction of the features. For example, regarding keystroke durations, values above 500 ms were rejected, based on the Windows key repeat rate preset. Also, with regard to digram latencies, values above 3000 ms were rejected, based on the fact that a time period greater than 3 s is considered by several studies as a typing pause [24].
An example of some records in an IKDD file is as follows:
```
48–0,62,65,74,64,60,45
49–0,95,91,82,108
50–0,98,88,87,103,104,59,87,65,60,48,83
69–82,272,316,671,391,96,928,550,74
69–83,125,193,170,142,235,168,310
69–84,180,604,362,409,171,147,190,158
```
The first field of each record indicates the feature. For example, the value “50–0” indicates the keystroke duration of the “2” key, while the value “69–84” indicates the digram latency of the “E–T” digram. All other fields are the values of the specific feature in the specific logfile. For example, the key “2” was used 11 times in this particular logfile. The first time this key was used, the keystroke duration recorded was 98 ms, the second time it was 88 ms, the third time it was 87 ms, and so on.
From the format of the IKDD files, it is understood that no sensitive or personal information of the volunteers can be revealed, and this is because it is not known in which order the keys and digrams were used, with the consequence that it is not possible to reconstruct the text, passwords, and credit card numbers.

# Citation
If you use our dataset in a scientific publication, please use the following bibtex citation:
```
@article{
  author    = {Tsimperidis, Ioannis and Asvesta, Olga-Dimitra and Vrochidou, Eleni and Papakostas, George A.},
  title     = {{IKDD: A Keystroke Dynamics Dataset for User Classification}},
  journal   = {Information},
  year      = {2024},
  volume    = {15},
  number    = {9},
  pages     = {511},
  doi       = {10.3390/info15090511},
  url       = {https://doi.org/10.3390/info15090511},
}
```
