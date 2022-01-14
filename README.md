C implementation of "Stealing Model Parameters via Side Channel Power Attacks" (ISVLSI-2021)[[Link]](https://ieeexplore.ieee.org/document/9516772).

### Abstract
Side-channel attacks target system implementation statistics, such as the electricity required to run a cryptographic function. Deriving cryptographic keys, such as AES keys, has become such a simplified process that extracting sensitive information from an otherwise secure algorithm requires only a $35USD microcontroller. While cryptographic algorithms indicate the presence of sensitive data, making them a preferable target, other systems hold valuable data with significantly less protection. Due to the ubiquity and rigidity of machine learning algorithms, the ability to infer model parameters has drastic security implications. This investigation extracted information from machine learning models through the use of traditional side-channel techniques. Specifically, a side-channel power analysis was performed using a ChipWhisperer Lite to extract information from Neural Networks and Linear Regression models running on a target microcontroller. Then, time series classification tasks were performed on the resultant power traces to determine the differences between the two models and their varied hyperparameters. Three such classification tasks were tested. In the first, a neural network was differentiated from a linear regression model with 100% accuracy. In the second, two neural networks with different sized hidden layers are classified with 97.92% accuracy. In the third, two virtually identical linear regression models are compared that differ only in the initial value of one hyperparameter. These models were only classified with 67.92% accuracy. Although the accuracy decreases as the models become more alike, these results indicate that machine learning model parameters can be inferred from power-based side-channel attacks.

### Citation
```
{
@inproceedings{wolf2021stealing,
  title={Stealing Machine Learning Parameters via Side Channel Power Attacks},
  author={Wolf, Shaya and Hu, Hui and Cooley, Rafer and Borowczak, Mike},
  booktitle={2021 IEEE Computer Society Annual Symposium on VLSI (ISVLSI)},
  pages={242--247},
  year={2021},
  organization={IEEE}
}
```
### Requirements

Update soon

### Run the code

Update soon
