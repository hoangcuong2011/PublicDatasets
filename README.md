# PublicDatasets


1. Reuters-21578

https://drive.google.com/file/d/1KT9p0Hj-_12-Cv433MdpXjoi0lv2v7vH/view?usp=sharing

Test Collections
Reuters-21578
Currently the most widely used test collection for text categorization research, though likely to be superceded over the next few years by RCV1.  The data was originally collected and labeled by Carnegie Group, Inc. and Reuters, Ltd. in the course of developing the CONSTRUE text categorization system.  Further details, including discussion of previous versions of the collection (e.g. Reuters-22173), are available in the README file.

The collection is available here as a gzipped tar archive (8.2 MB; 28.0 MB uncompressed).  The UCI KDD archive also has an entry for the collection, including a copy.  The version at UCI is identical, and I encourage you to get the UCI copy if available to save bandwidth at this site.  Previous locations of the collection (now no longer active) were http://www.research.att.com/~lewis/reuters21578.html and ftp:://canberra.cs.umass.edu/pub/reuters.

Various researchers have prepared data files useful for work with Reuters-21578.  Contact me if you would like me to host such resources here; I am happy to if their disk space requirements are modest.  Currently the only such resource available here is a PROLOG fact base about countries contributed by Ronen Feldman.

Return to home page for David D. Lewis

2. 20 Newsgroups
https://drive.google.com/file/d/1R774metrC1Qhxy3e84kBROlkPubV42L0/view?usp=sharing

The 20 Newsgroups data set
The 20 Newsgroups data set is a collection of approximately 20,000 newsgroup documents, partitioned (nearly) evenly across 20 different newsgroups. To the best of my knowledge, it was originally collected by Ken Lang, probably for his Newsweeder: Learning to filter netnews paper, though he does not explicitly mention this collection. The 20 newsgroups collection has become a popular data set for experiments in text applications of machine learning techniques, such as text classification and text clustering.

Organization
The data is organized into 20 different newsgroups, each corresponding to a different topic. Some of the newsgroups are very closely related to each other (e.g. comp.sys.ibm.pc.hardware / comp.sys.mac.hardware), while others are highly unrelated (e.g misc.forsale / soc.religion.christian). Here is a list of the 20 newsgroups, partitioned (more or less) according to subject matter:

comp.graphics
comp.os.ms-windows.misc
comp.sys.ibm.pc.hardware
comp.sys.mac.hardware
comp.windows.x	rec.autos
rec.motorcycles
rec.sport.baseball
rec.sport.hockey	sci.crypt
sci.electronics
sci.med
sci.space
misc.forsale	talk.politics.misc
talk.politics.guns
talk.politics.mideast	talk.religion.misc
alt.atheism
soc.religion.christian
Data
The data available here are in .tar.gz bundles. You will need tar and gunzip to open them. Each subdirectory in the bundle represents a newsgroup; each file in a subdirectory is the text of some newsgroup document that was posted to that newsgroup.

Below are three versions of the data set. The first ("19997") is the original, unmodified version. The second ("bydate") is sorted by date into training(60%) and test(40%) sets, does not include cross-posts (duplicates) and does not include newsgroup-identifying headers (Xref, Newsgroups, Path, Followup-To, Date). The third ("18828") does not include cross-posts and includes only the "From" and "Subject" headers.

20news-19997.tar.gz - Original 20 Newsgroups data set
20news-bydate.tar.gz - 20 Newsgroups sorted by date; duplicates and some headers removed (18846 documents)
20news-18828.tar.gz - 20 Newsgroups; duplicates removed, only "From" and "Subject" headers (18828 documents)
I recommend the "bydate" version since cross-experiment comparison is easier (no randomness in train/test set selection), newsgroup-identifying information has been removed and it's more realistic because the train and test sets are separated in time.
[7/3/07] I had originally listed the bydate version as containing 18941 documents. I've discovered that the correct count is 18846, of which rainbow skips 22. So the matlab version (below) represents 18824 documents. However, my rainbow2matlab.py script drops empty and single-word documents, of which there are 50 post-rainbow-processing, so you will find only 18774 total entries in the matlab/octave version.

