# Animal-Traits-Explorer

The dataset contains 101 entries and 18 columns, summarizing characteristics of various animals. Here's a breakdown of its structure:

Columns:
animal: The name of the animal (e.g., "aardvark," "antelope").
hair: Whether the animal has hair (boolean-like data).
feathers: Whether the animal has feathers.
eggs: Indicates if the animal lays eggs.
milk: Indicates if the animal produces milk.
airborne: Indicates if the animal can fly.
aquatic: Indicates if the animal is aquatic.
predator: Indicates if the animal is a predator.
toothed: Indicates if the animal has teeth.
backbone: Indicates if the animal has a backbone.
breathes: Indicates if the animal breathes.
venomous: Indicates if the animal is venomous.
fins: Indicates if the animal has fins.
legs: Number of legs the animal has (numeric value).
tail: Indicates if the animal has a tail.
domestic: Indicates if the animal is domesticated.
catsize: Indicates if the animal is "cat-sized."
type: The category/type of the animal (e.g., "mammal," "fish").
Data Details:
Most columns have boolean-like values (e.g., b'true' or b'false'), likely indicating characteristics as true or false.
The legs column contains numerical values representing the count of legs.
The type column serves as the classification or grouping of the animal.
Observations:
All columns are fully populated with no missing values.
The data appears to use byte-string formatting (e.g., b'true'). This may require decoding or cleaning for easier analysis.


Code to find the average number of legs for animals that are both aquatic and have fins
aquatic_fins = zoo_data[(zoo_data['aquatic'] == b'true') & (zoo_data['fins'] == b'true')]
average_legs = aquatic_fins['legs'].mean()
average_legs

 code to find the correlation between animals being venomous and tooth

zoo_data['venomous_num'] = (zoo_data['venomous'] == b'true').astype(int)
zoo_data['toothed_num'] = (zoo_data['toothed'] == b'true').astype(int)
correlation = zoo_data['venomous_num'].corr(zoo_data['toothed_num'])
correlation

 

