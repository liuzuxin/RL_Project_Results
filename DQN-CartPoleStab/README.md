# DQN - Experiment Results

This folder contains the experiment results on the CartPoleStab environment

The number in each file name represents the experiment number. For example, `config-1.yml` represents the configuration parameters in the first experiment.


## How to run

### Test the pre-trained

To try our pre-trained model, simply run

```angularjs
python test.py
```

The script will load the model from the path specified in the ```config.yml``` file
 
### Train your own model

To train your own model, you can change the hyper-parameters in the ```config.yml``` to whatever you want,
and then run

```angularjs
python train.py
```

The script will load the configurations in the ```config.yml``` file and begin to train

### Configuration parameter explanation

In the ```config.yml``` file, there are two set of configuration.
The first `model_config` is the configuration of the neural network architecture;
The second `training_config` is the configuration for the training process.

The `exp_number` parameter in the `training_config` is the number of your experiment. The name of saved figure results in the `./storage` folder will be determined by this parameter.

If you want to train your model from scratch, then set the `load_model` parameter to `False`. If set to `True`, the trainer will load the model from `model_path`.

If you think your training process is not stable and you want to save the model when the model has the best performance, set the `save_best` parameter to `True`.

