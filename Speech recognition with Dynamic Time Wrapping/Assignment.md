# Introduction

In this homework assignment, you will work on a simple speech recognition task: digit recognition using dynamic time warping.

# Task description

- Modify the wer function to evaluate the speaker error rate (SER), i.e., the performance of the DTW algorithm for text-dependent speaker identification. The wer function calculates the Word Error Rate (WER), the probability of error in the word classification task. By default, it compares the ’text’ of the correct answer with the ’text’ of the labeled recording that is close to each of the test wav files (using DTW distance). Identify the line that counts errors and change ‘text’ with ‘speaker’ to increment the number of errors if the speaker of the closest recording is not equal to the speaker of the test signal.

For the rest of the tasks of this assignment keep the original wer function to evaluate the Word Error Rate of the different variants of the DTW-based speech recognition system.

- Compare the WER with respect to the number of cepstral coefficients Change the default number of cepstral coefficients computed for each speech frame, and check how this number affects the WER of the speech recognizer. Use the obtained best value for the rest of the tasks.
- Analyze the influence on the recognition accuracy of each of the cepstral normalization steps (mean and variance) with and without littering. Use the default littering parameter (sinus window size) of 22.
- Extend the MFCC parameters with the first-order derivatives, and check that the WER is reduced.
- Complete the DTW algorithm to compute the alignment (backtracking). Plot one example of the alignment with the closest reference when the test signal is different from the reference signal (different digit) or equal (same digit).
- Optional: perform a comparative study of different variants of the DTW algorithm in terms of speed and accuracy.
