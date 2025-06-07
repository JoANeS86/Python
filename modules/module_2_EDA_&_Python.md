## EDA using basic data functions with Python

<ins>Packages and Libraries</ins>

    pandas, numpy, and datetime for operations
    matplotlib, pyplot, and seaborn for plotting

The following code has been applied to the 2018 lightning strike data collected by the National Oceanic and Atmospheric Administration (NOAA).

    import pandas as pd
    import numpy as np
    import datetime as dt
    import matplotlib.pyplot as plt

*df = pd.read_csv('eda_using_basic_data_functions_in_python_dataset1.csv')*

*df.head(10)*

*df.shape* --> Number of rows and columns.

*df.info()* --> Additional info of the data, including the data types of each column.

*df['date']= pd.to_datetime(df['date'])* --> Function pd.to_datetime() will convert the date into datetime type: In this example, data type assigned to
date was object (objects are strings), so it's better to turn the date into datetime to work with it.

*df.groupby(['date']).sum().sort_values('number_of_strikes', ascending=False).head(10)* --> Calculate the days with the most strikes.

*df['month'] = df['date'].dt.month* --> Create new column for the month.

*df.groupby(['month']).sum().sort_values('number_of_strikes', ascending=False).head(12)* --> Number of strikes per month.

*df['month_txt'] = df['date'].dt.month_name().str.slice(stop=3)* --> Convert date to text (month name).

*df_by_month = df.groupby(['month','month_txt']).sum().sort_values('month', ascending=True).head(12).reset_index()* --> New dataframe, so see data by month.

Finally, the following piece of work will create a bar chart:

    plt.bar(x=df_by_month['month_txt'],height= df_by_month['number_of_strikes'], label="Number of strikes")
    plt.plot()
    
    plt.xlabel("Months(2018)")
    plt.ylabel("Number of lightning strikes")
    plt.title("Number of lightning strikes in 2018 by months")
    plt.legend()
    plt.show()

