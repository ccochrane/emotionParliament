# emotionParliament
The Automated Detection of Emotion in Transcripts of Parliamentary Speech: Comparing Human and Machine Classification of the Video and Written Records of Debates in the Canadian House of Commons

Abstract: The volume of machine-readable text communication about politics has increased exponentially over the past three decades, spawning the pursuit of new tools for automated analyses of sentiment in large political corpora.  Unlike written communication, however, the expression of emotion in speech is not confined to word-choice and syntax, and instead relies heavily on intonation, facial expressions, and body language, which go undetected in analyses of political text.  This raises the question of whether tools developed for analyses of writing can detect sentiment in transcripts of political speech.  In this paper, we survey a variety of strategies for the automated analysis of emotion in text, and test their outputs against human-coded sentiment analysis of the written and video record of debates in the Canadian House of Commons. We find that transcripts capture the valence, but not the emotional intensity, of political speeches. We also find that while leading dictionary and supervised approaches to sentiment detection performed reasonably well, using domain specific word embeddings induced from state-of-the-art Neural Networks surpassed these other approaches, and achieved near-human level performance. 

(1) selectionScript.R - A script for selecting video clips to extract from CPAC Question Periods.

(2) extractedSentencesYouTubeLinks.csv -The list of videos extracted from Step 1, along with date, speaker, party, language of speech, Hansard record (English), timeStamp (MM:SS), sentence length (SS:MS), and video link (youTube). 

(3) videoCodingInstrument.pdf - An image of the Qualtrics coding instrument for the video clips.

(4) emotionInHansard_December+20%2C+2018_14.52.csv - The raw output from the Qualtrics survey instrument that the Video Coders used to code the videos.

(5) qualtricsDataExtract.py - A script for structuring the raw Qualtrics output (from Step 4).  

(6) qualtricsStructured.csv - The structured Qualtrics data (from Step 5).

(7) createVideoCoderRecord.py - A script for extracting (from Step 6) the first two coding decisions of each video coder for each video.

(8) videoCoderAverages.csv - The record of video coding decisions (from Step 7), which captures, for each video coder and video, the first and second score that the coder assigned for activation and sentiment, as well as the averages of their first two scores for both dimensions. Rows are videos.  Columns are: v1Act1, v1Act2, v1ActAvg, v1Sent1, v1Sent2, v1SentAvg, v2Act1 ... v3SentAct. 

(9) The csv files of the text coding, as returned by the text coders for rounds 1 and 2.  These files are:
                a) cm_coding1.csv & cm_coding2.csv for coder CM
                b) sf_coding1.csv & sf_coding2.csv for coder SF
                c) jv_coding1.csv & jv_coding2.csv for coder JV

(10) createTextCoderRecord.py - A script for rearranging and merging the coding data (from Step 9) of the text coders.

(11) textCoderAverages.csv - The record of text coding decisions (from Step 10), which captures, for each text coder and video, the first and second score that the coder assigned for activation and sentiment, as well as the averages of their first two scores for both dimensions. Rows are videos.  Columns are: t1Act1, t1Act2, t1ActAvg, t1Sent1, t1Sent2, t1SentAvg, t2Act1 ... t3SentAct. 

(12) mergeTextVideoCoding.py - A script for mergint the video coding data (from Step 8) and the text coding data (from Step 11).

(13) fullCodingData.cscv - The merged record of video and text coding decisions (from Step 12).


