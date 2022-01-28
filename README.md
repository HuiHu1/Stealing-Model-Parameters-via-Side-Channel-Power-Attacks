C and Python implementation of "Stealing Model Parameters via Side Channel Power Attacks" (ISVLSI-2021)[[Link]](https://ieeexplore.ieee.org/document/9516772).

### Abstract
Side-channel attacks target system implementation statistics, such as the electricity required to run a cryptographic function. Deriving cryptographic keys, such as AES keys, has become such a simplified process that extracting sensitive information from an otherwise secure algorithm requires only a $35USD microcontroller. While cryptographic algorithms indicate the presence of sensitive data, making them a preferable target, other systems hold valuable data with significantly less protection. Due to the ubiquity and rigidity of machine learning algorithms, the ability to infer model parameters has drastic security implications. This investigation extracted information from machine learning models through the use of traditional side-channel techniques. Specifically, a side-channel power analysis was performed using a ChipWhisperer Lite to extract information from Neural Networks and Linear Regression models running on a target microcontroller. Then, time series classification tasks were performed on the resultant power traces to determine the differences between the two models and their varied hyperparameters. Three such classification tasks were tested. In the first, a neural network was differentiated from a linear regression model with 100% accuracy. In the second, two neural networks with different sized hidden layers are classified with 97.92% accuracy. In the third, two virtually identical linear regression models are compared that differ only in the initial value of one hyperparameter. These models were only classified with 67.92% accuracy. Although the accuracy decreases as the models become more alike, these results indicate that machine learning model parameters can be inferred from power-based side-channel attacks.

### Requirements

ChipWhisperer Lite 1200, Jupyter Notebook.

### Run the code

```
Step 1: Getting the VM and Jupyter Up and Running.

(1) Download the Latest Version of VirtualBox [[Download]](https://www.virtualbox.org/wiki/Downloads).

(2) Download/Install the extension pack [[Download]](https://download.virtualbox.org/virtualbox/6.1.18/). 

(3) Download the current ChipWhisperer VM [[Download]](https://github.com/newaetech/chipwhisperer/releases/). 

(4) Download 7Zip [[Download]](https://www.7-zip.org/download.html). 

(5) UnZip The VM you just downloaded.

(6) Launch Virtualbox > Machine > Add... > Select File You Just Unzipped.

(7) Start/Run The virtual Machine and login.

(8) Setup a password for Jupyter.

(9) Reboot the VM. sudo reboot and open Firefox/Chrome (ONLY) - navigate to 127.0.0.1:8888 or localhost:8888.
 
Step 2: Target Board Setup (SCOPETYPE = 'OPENADC'  PLATFORM = 'CWLITEXMEGA'  SS_VER='SS_VER_1_1').

Step 3: %run /home/vagrant/work/projects/chipwhisperer/jupyter/Setup_Scripts/Setup_Generic.ipynb.

Step 4: Compile Program to Run on Board. 

PATH = "/home/vagrant/work/projects/chipwhisperer/hardware/victims/firmware/"
TARGET_MODEL = "Model Name" 
%%bash -s "$PLATFORM" "$PATH" "$TARGET_MODEL" "$SS_VER"
cd $2$3 
make PLATFORM=$1 CRYPTO_TARGET=NONE SS_VER=$4

Step 5: Pass Model Data Over Serial.

Step 6: Run Model and Collect Power Traces.
 
```

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
