# Autoencoding Models

This repository contains configuration files of different autoencoders used in our anomaly detection experiments.

Load and train the models as the following:

```python
import json
from tensorflow import keras


with open( 'configs/model.json', 'r') as f:
    json_config = json.load(f)
 
autoencoder = keras.models.model_from_json(json_config)

autoencoder.compile(optimizer='adam', loss='binary_crossentropy')
autoencoder.fit(train_data, epochs=1000)
```

Please, refer to the table below for model namings:

| Model         | Skip Connections | Pro-SiVIC  | CARLA      |
| :-----------: | :--------------: | :--------: | :--------: |
| simpler model | yes              | `model_01` | `model_05` |
| simpler model | no               | `model_02` | `model_06` |
| complex model | yes              | `model_03` | `model_07` |
| complex model | no               | `model_04` | `model_08` |
