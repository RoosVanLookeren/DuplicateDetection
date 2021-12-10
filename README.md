# DuplicateDetection

This project implements an duplicate detection method by implement an LSH approach to reduce computation time of duplicate detection, based on the work of Hartveld et al. [1]. The code is written in collaboration between Anonym530 and van Wessel

This project is an assignment for the Erasmus School of Economics on duplicate detection for TVs sellend on four different webshops. An LSH approach is used to reduce the number of comparisons needed to be made for the detection method. More informations can be found at Van Lookeren Campagne (2021).

The project is structured as follows; The data is uploaded and structured to be effectively used. A bootstrap of 60% of the data is taken for evaluation of the method

The LSH and the Single Similarity Method (SSM) which output the final product candidate pairs is implemented in the following way:
1. All product titles are cleaned and preprocessed, such that model words can be extracted from them.
2. The model words are extrated from the each product product and added to the vector of model words. 
3. Binary vectors are created from the vector of model words. 
4. The minhashing takes as input the binary vectors and signatures the binary vectors for each product. 
5. The LSH uses these signatures to produce candidate pairs for comparison. 
6. Last, the final candidate pairs are provided by the SSM 

In the program, we set we manually set the number of hashes equal to 720 which approximately 50% of the highest size of the binary vectors. Furthermore, we have the threshold for similairty in the SSM algorithm to 0.6, for our data this value achieves good final product candidate pairs.

[1] Hartveld, A., van Keulen, M., Mathol, D., van Noort, T., Plaatsman, T., Frasincar, F., Schouten, K.: An LSH-based model-words-driven product duplicate detection method, In: 30th International Conference on Advanced Information Systems Engineering (CAiSE 2018). Lecture Notes in Computer Science, vol. 10816, pp. 149-161. Springer (2018)
