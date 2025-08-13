# Step 1: Load dataset
import os
import pandas as pd
file_path = 'Downloads/dummy dataset.txt'
data = pd.read_csv(file_path, sep = "|")

#Display sample data
data.head()

# Step 1: Load dataset
import os
import pandas as pd
file_path = 'Downloads/dummy dataset.txt'
data = pd.read_csv(file_path, sep = "|")

#Display sample data
data.head()

# Step 3: Handle missing values
data.dropna(subset=['cus_no'], inplace=True)
data['chn'] = data['chn'].fillna(data['chn'].mode()[0])
data['gndr'] = data['gndr'].fillna(data['gndr'].mode()[0])
data['age'] = data['age'].fillna(data['age'].median())

#Step 4: Checking for duplicate values
duplicate_values=data[data.duplicated()]
len(duplicate_values)

# Step 5: Remove duplicate values
data = data.drop_duplicates()
data.head()

#Step 6: Checking for data types
print("Data Type:\n",data.dtypes)

# Step 7: Converting data types
data['trn_dt'] = pd.to_datetime(data['trn_dt'])
data['cus_no'] = data['cus_no'].astype('int64')
data['age'] = data['age'].astype('int64')
print(data.dtypes)
