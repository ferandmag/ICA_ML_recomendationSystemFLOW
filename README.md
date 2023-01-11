# A recommendation system to predict which new, previously unviewed content is most likely to be chosen for viewing on Flow by a group of users based on their viewing history.

## Software and Tools Requirements

1. [Github Account](https:/github.com)
2. [VS Code IDE](http:/code.visualstudio.com)
3. [Git CLI](https://cli.github.com)

## Datasets

### train.csv:
This dataset contains Flow's video on demand (VOD) content visualization records, corresponding to a random sample of more than 113 thousand profiles. The dictionary of variables of this table is detailed below:

* customer_id: identification code of each Flow customer (may have one or more associated account_id)
* account_id: identification code of each Flow profile (corresponds to a unique customer_id)
* device_type: indicates the type of device from which the display was made. The possible categories are:
  * CLOUD: web client
  * PHONE: cellphone
  * STATIONARY: smart TV
  * STB: set-top box, Flow decode
  * TABLET
* asset_id: identification code of each asset (video) available on the platform
* tunein: date and start time of each viewing
* tuneout: date and time of the end of each display
* resume: dummy variable indicating if a previous consumption of the same asset_id is resumed