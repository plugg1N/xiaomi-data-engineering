
# 🛠 Xiaomi-Phones | Data Engineering/Prep

This is a **Jupyter Notebook** that prepares `mi_info.csv` file (its Dataframe) for working and future analization

# 👀 First Look

![](https://github.com/plugg1N/xiaomi-data-engineering/blob/main/Images/image1.png?raw=true)

As we can observe, those factors needed some touch:
- "model_names"
- "price"
- "storage_ram"
- "os_processor"
- "network"
- "battery"

Here are their `pandas.Dataframe.dtypes`:
![](https://github.com/plugg1N/xiaomi-data-engineering/blob/main/Images/image2.png?raw=true)

## 📖 Plan

1. I've **dropped some columns**, that I personally won't work with *(they can be returned back if needed).* Those columns are:
    - "imgURL"
    - "network" 

2. Changed `dtypes` of objects to normal ones:
    ```
    index                int64
    model_names         object
    ratings            float64
    price                Int16
    battery             object
    storage              Int16
    ram                  Int16
    processor           object
    android_version     object
    ```

3. Made "model_names" normalized:
    - `REDMI 10 Power (Sporty Orange, 128 GB)`
    - `REDMI 10 Power (Power Black, 128 GB)`
    - etc.

4. Removed rows with nonsensical prices that are **lower than 1**

5. Noramlized:
    - "storage"
    - "ram"
    - "battery"
    - "price"
    - "processor"
    - "android_version"



## 🎯 Results

Those are **RESULTS** (end Dataframe):

![](https://github.com/plugg1N/xiaomi-data-engineering/blob/main/Images/image3.png?raw=true)

**EXAMPLE OF DATA-ANALYZING** (mean price of a phone based on its rating):

![](https://github.com/plugg1N/xiaomi-data-engineering/blob/main/Images/image4.png?raw=true)
