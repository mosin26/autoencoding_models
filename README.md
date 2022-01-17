# Autoencoding Models

![autoencoder_light](https://user-images.githubusercontent.com/16051397/149675837-20a669e5-9dc4-49d8-a0e1-29f2d2d1af89.png#gh-light-mode-only)

![autoencoder_dark](https://user-images.githubusercontent.com/16051397/149675856-209c0474-f812-4bf0-b0b7-b8b61ca574db.png#gh-dark-mode-only)

## Keras Autoencoders

This repository contains configuration files for different Keras autoencoder models.

You can load and train the models as the following:

```python
import json
from tensorflow import keras


with open('./configs/model.json', 'r') as f:
    json_config = json.load(f)
 
autoencoder = keras.models.model_from_json(json_config)

autoencoder.compile(optimizer='adam', loss='binary_crossentropy')
autoencoder.fit(train_data, epochs=1000)
```

Please, refer to the table below for model namings:

| Model         | Skip Connections | Name       |
| :-----------: | :--------------: | :--------: |
| simpler model | no               | `model_01` |
| simpler model | yes              | `model_02` |
| complex model | no               | `model_03` |
| complex model | yes              | `model_04` |

These models work with any arbitrary size images.
