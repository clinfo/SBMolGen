# Structure-based de novo Molecular Generator (SBMolGen)
Supporting Information for the paper _"[Structure-based de novo molecular generator combined with artificial intelligence and docking simulations](https://doi.org/10.26434/chemrxiv.14371967.v1)"_.

In this study, we developed a new deep learning-based molecular generator, SBMolGen, that integrates a recurrent neural network, a Monte Carlo tree search, and docking simulations. The results of an evaluation using four target proteins (two kinases and two G protein-coupled receptors) showed that the generated molecules had a better binding affinity score (docking score) than the known active compounds, and they possessed a broader chemical space distribution. SBMolGen not only generates novel binding active molecules but also presents 3D docking poses with target proteins, which will be useful in subsequent drug design.

SBMolGen is modify based [ChemTS](https://github.com/tsudalab/ChemTS).
## Requirements
1. [Python](https://www.anaconda.com/download/)>=2.7 
2. [Keras](https://github.com/fchollet/keras) (version 2.0.5) If you installed the newest version of keras, some errors will show up. Please change it back to keras 2.0.5 by pip install keras==2.0.5. 
3. [rdkit](https://anaconda.org/rdkit/rdkit)
4. [rDock](http://rdock.sourceforge.net/installation/)

## How to use

1. Get SBMleGen.
```
git clone https://github.com/clinfo/SBMolGen.git
cd SBMolGen
```
2. Train the RNN model.
```
cd train_RNN
python train_RNN.py
```
3. Make a setting file for molecule desgin.
a sample of setting file, setting.yaml.

```

```
4. Prepare the target file.
Refer to the [rDock Tutorials](http://rdock.sourceforge.net/docking-in-3-steps/) for instructions on preparing the required files for docking.
5. Molecule generation.
```
python main.py setting.yaml
```

