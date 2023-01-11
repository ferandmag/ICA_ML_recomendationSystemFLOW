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

### metadata.csv:
This dataset contains the metadata associated with each of the contents. The variables included are:

* asset_id: identification code of each asset (video) available on Flow.
* content_id: identification code that groups the different asset_id associated with the same content (e.g. each episode of a series has its own asset_id, while the series is identified by a unique content_id).
* title: title.
* reduced_title: reduced title.
* episode_title: episode title (valid for episodic content, such as series).
* show_type: type of show - the categories are self-referential with the exception of "Rolling", which indicates that it is anincomplete series, and "Web", which refers to content designed entirely in digital format (web series).
* released_year: year of release.
* country_of_origin: country of origin - expressed with the two-letter code of the ISO 3166 international standardization standard.
* category: category or genre to which the content belongs - there may be one or more.
* keywords: keywords or tags associated with the content - there may be one or more.
* description: description (synopsis).
* reduced_desc: reduced description (synopsis).
* cast_first_name: name and surname of the main actors and actresses.
* credits_first_name: director's first and last name.
* run_time_min: total duration, expressed in minutes.
* audience: target audience.
* made_for_tv: dummy variable indicating whether the content was made for TV.
* close_caption: dummy variable that indicates whether the content has subtitles.
* sex_rating: dummy variable that indicates if the content has explicit sex scenes.
* violence_rating: dummy variable indicating whether the content has explicit scenes of violence.
* language_rating: dummy variable indicating whether the content contains language that may be considered offensive or inappropriate.
* dialog_rating: dummy variable that indicates whether the content has dialogs that may be considered offensive or inappropriate.
* fv_rating: dummy variable that indicates whether the content has an FV rating, which corresponds to a child audience with fictional violence.
* pay_per_view: dummy variable indicating whether it is a rental.
* pack_premium_1: dummy variable indicating if it is an exclusive content of the premium pack 1.
* pack_premium_2: dummy variable indicating whether it is an exclusive content of premium pack 2.
* create_date: creation date of the asset.
* modify_date: asset modification date.
* start_vod_date: date from which the asset is available on the platform.
* end_vod_date: end date of the asset's availability on the platform.