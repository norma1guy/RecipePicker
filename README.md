# Recipe Picker using NLP

## Stages 

### Datasets

- For nutrition dataset the OpenNutrition dataset was used from https://www.opennutrition.app/download
- For recipes dataset the data aggregated from Food.com was used https://www.kaggle.com/datasets/shuyangli94/foodcom-recipes-with-search-terms-and-tags
- Spark is used for data manipulation and creation(Pandas is much slower)

### Preprocessing
- Clean ingredient names
- Parse fractions in quantities
- Remove plurals

### Matching ingredients from both datasets
- First logic is to use set theory to match the ingredients
- Second layer is to use sentence transformer to convert the ingredients into embeddings and then use cosine similarity to match them

### Calculate Nutrients
- Calculate the quantity of ingredients used from raw_str
- Convert quantities to metrics.
- For unitless use nutrition dataset to calculate the weights
- Use quants to calculate nutrition.

