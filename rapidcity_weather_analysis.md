# Climate change is impacting the way people live around the world

::: {.cell .markdown}

Higher highs, lower lows, storms, and smoke – we’re all feeling the
effects of climate change. In this workflow, you will take a look at
trends in temperature over time in Rapid City, SD.

> **Important**
>
> [Read about some of the effects of – and solutions for – climate
> change on the Pine Ridge Reservation southeast of Rapid
> City.](https://www.theguardian.com/environment/2022/dec/03/south-dakota-reservation-food-desert-residents-transforming-crop-oasis)

## Get started with open reproducible science!

[Open reproducible
science](https://www.earthdatascience.org/courses/intro-to-earth-data-science/open-reproducible-science/get-started-open-reproducible-science/)
makes scientific methods, data and outcomes available to everyone. That
means that *everyone* who wants should be able to **find**, **read**,
**understand**, and **run** your workflows for themselves.

<img src="https://www.earthdata.nasa.gov/s3fs-public/2021-11/Circle_Diagram_UPDATE_2.jpg?VersionId=pFRniRpjtgc_MEXUJKi9_sXLoMsSX.pB" alt-text="Components of open science - accessible, reproducible, inclusive" width="500"/>

> Image from
> https://www.earthdata.nasa.gov/esds/open-science/oss-for-eso-workshops

Few if any science projects are 100% open and reproducible (yet!).
However, members of the open science community have developed open
source tools and practices that can help you move toward that goal. You
will learn about many of those tools in [the Intro to Earth Data Science
textbook](https://www.earthdatascience.org/courses/intro-to-earth-data-science/).
Don’t worry about learning all the tools at once – we’ve picked a few
for you to get started with.

------------------------------------------------------------------------

> **<i class="fa fa-solid fa-glasses fa-large" aria-label="glasses"></i>
> Further reading**
>
> Read [our textbook chapter about open reproducible
> science](https://www.earthdatascience.org/courses/intro-to-earth-data-science/open-reproducible-science/get-started-open-reproducible-science/).

> **<i class="fa fa-solid fa-pencil fa-large" aria-label="pencil"></i>
> What does open reproducible science mean to you?**
>
> <i class="far fa-regular fa-square" aria-label="square"></i> Create a
> new Markdown cell below this one using the `+ Markdown` button in the
> upper left.
>
> <i class="far fa-regular fa-square" aria-label="square"></i> In the
> new cell, answer the following questions using a **numbered list** in
> Markdown:
>
> 1.  In 1-2 sentences, define open reproducible science.
> 2.  In 1-2 sentences, choose one of the open source tools that you
>     have learned about (i.e. Shell, Git/GitHub, Jupyter Notebook,
>     Python) and explain how it supports open reproducible science.

1. Open reproducible science promotes easy access to shared data for others to replicate. 
2. Github is well organized and collaboritive.

## <i class="fa fa-solid fa-pencil fa-large" aria-label="pencil"></i> Human-readable and Machine-readable

<i class="far fa-regular fa-square" aria-label="square"></i> Create a
new Markdown cell below this one using the <kbd>ESC</kbd> + <kbd>b</kbd>
keyboard shortcut.

<i class="far fa-regular fa-square" aria-label="square"></i> In the new
cell, answer the following question in a Markdown **quote**: In 1-2
sentences, does this Jupyter Notebook file have a machine-readable name?
Explain your answer.

------------------------------------------------------------------------

## What the fork?! Who wrote this?

Below is a scientific Python workflow. But something’s wrong – The code
won’t run! Your task is to follow the instructions below to **clean and
debug** the Python code below so that it runs.

> **Tip**
>
> Don’t worry if you can’t solve every bug right away. We’ll get there!
> The most important thing is to identify problems with the code and
> write high-quality [**GitHub
> Issues**](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-an-issue#creating-an-issue-from-a-repository).

At the end, you’ll **repeat the workflow** for a location and
measurement of your choosing.

Alright! Let’s clean up this code. First things first…

> **<i class="fa fa-solid fa-keyboard fa-large" aria-label="keyboard"></i>
> Machine-readable file names**
>
> Rename this notebook (if necessary) with an [**expressive and
> machine-readable file
> name**](https://www.earthdatascience.org/courses/intro-to-earth-data-science/open-reproducible-science/get-started-open-reproducible-science/best-practices-for-organizing-open-reproducible-science/)

------------------------------------------------------------------------

## Python **packages** let you use code written by experts around the world

Because Python is open source, lots of different people and
organizations can contribute (including you!). Many contributions are in
the form of **packages** which do not come with a standard Python
download.

> **<i class="fa fa-solid fa-glasses fa-large" aria-label="glasses"></i>
> Read more**
>
> [Packages need to be installed and
> **imported**](https://www.earthdatascience.org/courses/intro-to-earth-data-science/python-code-fundamentals/use-python-packages/).

In the cell below, someone was trying to import the **pandas package**,
which helps us to work with [**tabular data** such as comma-separated
value or csv
files](https://www.earthdatascience.org/courses/intro-to-earth-data-science/file-formats/use-text-files/).

> **<i class="fa fa-solid fa-keyboard fa-large" aria-label="keyboard"></i>
> Your task**
>
> 1.  Correct the typo below to properly import the pandas package under
>     its **alias** pd.
> 2.  Run the cell to import pandas
>
> NOTE: **Run your code in the right **environment\*\* to avoid import
> errors\*\*
>
> We’ve created a coding **environment** for you to use that already has
> all the software and libraries you will need! When you try to run some
> code, you may be prompted to select a **kernel**. The **kernel**
> refers to the version of Python you are using. You should use the
> **base** kernel, which should be the default option.


```python
# Import pandas
import pandas as pd
```

Once you have run the cell above and imported `pandas`, **run the cell
below**. It is a test cell that will tell you if you completed the task
successfully. If a test cell isn’t working the way you expect, check
that you ran your code **immediately before** running the test.


```python
# DO NOT MODIFY THIS TEST CELL
points = 0
try:
    pd.DataFrame()
    points += 5
    print('\u2705 Great work! You correctly imported the pandas library.')
except:
    print('\u274C Oops - pandas was not imported correctly.')
print('You earned {} of 5 points for importing pandas'.format(points))
```

    ✅ Great work! You correctly imported the pandas library.
    You earned 5 of 5 points for importing pandas


------------------------------------------------------------------------

## There are more Earth Observation data online than any one person could ever look at

[NASA’s Earth Observing System Data and Information System (EOSDIS)
alone manages over 9PB of
data](https://www.earthdata.nasa.gov/learn/articles/getting-petabytes-people-how-eosdis-facilitates-earth-observing-data-discovery-and-use).
1 PB is roughly 100 times the entire Library of Congress (a good
approximation of all the books available in the US). It’s all available
to **you** once you learn how to download what you want.

Here we’re using the NOAA National Centers for Environmental Information
(NCEI) [Access Data
Service](https://www.ncei.noaa.gov/support/access-data-service-api-user-documentation)
application progamming interface (API) to request data from their web
servers. We will be using data collected as part of the Global
Historical Climatology Network daily (GHCNd) from their [Climate Data
Online library](https://www.ncdc.noaa.gov/cdo-web/datasets) program at
NOAA.

For this example we’re requesting [daily summary data in Rapid City, CO
(station ID
USC00396947)](https://www.ncdc.noaa.gov/cdo-web/datasets/GHCND/stations/GHCND:USC00396947/detail).

> **<i class="fa fa-solid fa-pencil fa-large" aria-label="pencil"></i>
> Your task:**
>
> 1.  Research the [**Global Historical Climatology Network -
>     Daily**](https://www.ncei.noaa.gov/metadata/geoportal/rest/metadata/item/gov.noaa.ncdc:C00861/html)
>     data source.
> 2.  In the cell below, write a 2-3 sentence description of the data
>     source. You should describe:
>     -   who takes the data
>     -   where the data were taken
>     -   what the maximum temperature units are
>     -   how the data are collected
> 3.  Include a citation of the data (**HINT:** See the ‘Data Citation’
>     tab on the GHCNd overview page).

**YOUR DATA DESCRIPTION AND CITATION HERE** 🛎️

The Global Historial Climatology Network - Daily utilizes thousands of different station networks to continuously update their climate observations. This process analyzes temperature, snow fall and snow depth along with the time of observation.

Menne, Matthew J., Imke Durre, Bryant Korzeniewski, Shelley McNeill, Kristy Thomas, Xungang Yin, Steven Anthony, Ron Ray, Russell S. Vose,
Byron E.Gleason, and Tamara G. Houston (2012): Global Historical Climatology Network - Daily (GHCN-Daily), Version 3. [indicate subset used].,
NOAA National Climatic Data Center. doi:10.7289/V5D21VHZ [access date].

## You can access NCEI GHCNd Data from the internet using its API 🖥️ 📡 🖥️

The cell below contains the URL for the data you will use in this part
of the notebook. We created this URL by generating what is called an
**API endpoint** using the NCEI [API
documentation](https://www.ncei.noaa.gov/support/access-data-service-api-user-documentation).

> **Note**
>
> An **application programming interface** (API) is a way for two or
> more computer programs or components to communicate with each other.
> It is a type of software interface, offering a service to other pieces
> of software ([Wikipedia](https://en.wikipedia.org/wiki/API)).

However, we still have a problem - we can’t get the URL back later on
because it isn’t saved in a **variable**. In other words, we need to
give the url a name so that we can request in from Python later (sadly,
Python has no ‘hey what was that thingy I typed yesterday?’ function).

> **<i class="fa fa-solid fa-glasses fa-large" aria-label="glasses"></i>
> Read more**
>
> Check out the [textbook section on
> variables](https://www.earthdatascience.org/courses/intro-to-earth-data-science/python-code-fundamentals/get-started-using-python/variables/)

> **<i class="fa fa-solid fa-keyboard fa-large" aria-label="keyboard"></i>
> Your task**
>
> 1.  Pick an expressive variable name for the URL. HINT: click on the
>     `Variables` button up top to see all your variables. Your new url
>     variable will not be there until you define it and run the code
> 2.  Reformat the URL so that it adheres to the [79-character PEP-8
>     line
>     limit](https://peps.python.org/pep-0008/#maximum-line-length).You
>     should see two vertical lines in each cell - don’t let your code
>     go past the second line
> 3.  At the end of the cell where you define your url variable, **call
>     your variable (type out its name)** so it can be tested.


```python
daily_sum = ('https://www.ncei.noaa.gov/access/services/da'
'ta/v1?dataset=daily-summaries&dataTypes=TOBS,PRCP&stations'
'=USC00396947&startDate=1949-10-01&endDate=2024-05-05&'
'includeStationName=true&includeStation'
'Location=1&units=standard')
daily_sum
```




    'https://www.ncei.noaa.gov/access/services/data/v1?dataset=daily-summaries&dataTypes=TOBS,PRCP&stations=USC00396947&startDate=1949-10-01&endDate=2024-05-05&includeStationName=true&includeStationLocation=1&units=standard'




```python
# DO NOT MODIFY THIS TEST CELL
resp_url = _
points = 0

if type(resp_url)==str:
    points += 3
    print('\u2705 Great work! You correctly called your url variable.')
else:
    print('\u274C Oops - your url variable was not called correctly.')

if len(resp_url)==218:
    points += 3
    print('\u2705 Great work! Your url is the correct length.')
else:
    print('\u274C Oops - your url variable is not the correct length.')

print('You earned {} of 6 points for defining a url variable'.format(points))
```

    ✅ Great work! You correctly called your url variable.
    ✅ Great work! Your url is the correct length.
    You earned 6 of 6 points for defining a url variable


------------------------------------------------------------------------

## **Download and get started working with NCEI data**

The `pandas` library you imported can download data from the internet
directly into a type of Python **object** called a `DataFrame`. In the
code cell below, you can see an attempt to do just this. But there are
some problems…

> **<i class="fa fa-solid fa-keyboard fa-large" aria-label="keyboard"></i>
> You’re ready to fix some code!**
>
> Your task is to:
>
> 1.  Leave a space between the `#` and text in the comment and try
>     making the comment more informative
>
> 2.  Make any changes needed to get this code to run. HINT: The
>     `my_url` variable doesn’t exist - you need to replace it with the
>     variable name **you** chose.
>
> 3.  Modify the `.read_csv()` statement to include the following
>     parameters:
>
>     -   `index_col='DATE'` – this sets the `DATE` column as the index.
>         Needed for subsetting and resampling later on
>     -   `parse_dates=True` – this lets `python` know that you are
>         working with time-series data, and values in the indexed
>         column are **date time objects**
>     -   `na_values=['NaN']` – this lets `python` know how to handle
>         missing values
>
> 4.  Clean up the code by using **expressive variable names**,
>     **expressive column names**, **PEP-8 compliant code**, and
>     **descriptive comments**

**Make sure to call your `DataFrame` by typing it’s name as the last
line of your code cell** Then, you will be able to run the test cell
below and find out if your answer is correct.


```python
# use pandas to download data into data frame
rapid_df = pd.read_csv(
  daily_sum,
  index_col='DATE',
  parse_dates=True,
  na_values=['NaN'])

rapid_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>STATION</th>
      <th>NAME</th>
      <th>LATITUDE</th>
      <th>LONGITUDE</th>
      <th>ELEVATION</th>
      <th>PRCP</th>
      <th>TOBS</th>
    </tr>
    <tr>
      <th>DATE</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1949-10-01</th>
      <td>USC00396947</td>
      <td>RAPID CITY 4 NW, SD US</td>
      <td>44.12055</td>
      <td>-103.28417</td>
      <td>1060.4</td>
      <td>0.00</td>
      <td>51.0</td>
    </tr>
    <tr>
      <th>1949-10-02</th>
      <td>USC00396947</td>
      <td>RAPID CITY 4 NW, SD US</td>
      <td>44.12055</td>
      <td>-103.28417</td>
      <td>1060.4</td>
      <td>0.00</td>
      <td>51.0</td>
    </tr>
    <tr>
      <th>1949-10-03</th>
      <td>USC00396947</td>
      <td>RAPID CITY 4 NW, SD US</td>
      <td>44.12055</td>
      <td>-103.28417</td>
      <td>1060.4</td>
      <td>0.00</td>
      <td>52.0</td>
    </tr>
    <tr>
      <th>1949-10-04</th>
      <td>USC00396947</td>
      <td>RAPID CITY 4 NW, SD US</td>
      <td>44.12055</td>
      <td>-103.28417</td>
      <td>1060.4</td>
      <td>0.00</td>
      <td>45.0</td>
    </tr>
    <tr>
      <th>1949-10-05</th>
      <td>USC00396947</td>
      <td>RAPID CITY 4 NW, SD US</td>
      <td>44.12055</td>
      <td>-103.28417</td>
      <td>1060.4</td>
      <td>0.00</td>
      <td>50.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2024-04-30</th>
      <td>USC00396947</td>
      <td>RAPID CITY 4 NW, SD US</td>
      <td>44.12055</td>
      <td>-103.28417</td>
      <td>1060.4</td>
      <td>0.00</td>
      <td>44.0</td>
    </tr>
    <tr>
      <th>2024-05-01</th>
      <td>USC00396947</td>
      <td>RAPID CITY 4 NW, SD US</td>
      <td>44.12055</td>
      <td>-103.28417</td>
      <td>1060.4</td>
      <td>0.00</td>
      <td>33.0</td>
    </tr>
    <tr>
      <th>2024-05-02</th>
      <td>USC00396947</td>
      <td>RAPID CITY 4 NW, SD US</td>
      <td>44.12055</td>
      <td>-103.28417</td>
      <td>1060.4</td>
      <td>0.35</td>
      <td>39.0</td>
    </tr>
    <tr>
      <th>2024-05-04</th>
      <td>USC00396947</td>
      <td>RAPID CITY 4 NW, SD US</td>
      <td>44.12055</td>
      <td>-103.28417</td>
      <td>1060.4</td>
      <td>0.00</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2024-05-05</th>
      <td>USC00396947</td>
      <td>RAPID CITY 4 NW, SD US</td>
      <td>44.12055</td>
      <td>-103.28417</td>
      <td>1060.4</td>
      <td>0.00</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>26111 rows × 7 columns</p>
</div>




```python
# DO NOT MODIFY THIS TEST CELL
tmax_df_resp = _
points = 0

if isinstance(tmax_df_resp, pd.DataFrame):
    points += 1
    print('\u2705 Great work! You called a DataFrame.')
else:
    print('\u274C Oops - make sure to call your DataFrame for testing.')

print('You earned {} of 2 points for downloading data'.format(points))
```

    ✅ Great work! You called a DataFrame.
    You earned 1 of 2 points for downloading data


> HINT: Check out the `type()` function below - you can use it to check
> that your data is now in `DataFrame` type object


```python
# Check that the data was imported into a pandas DataFrame
type(rapid_df)
```




    pandas.core.frame.DataFrame



> **<i class="fa fa-solid fa-keyboard fa-large" aria-label="keyboard"></i>
> Clean up your DataFrame**
>
> Use double brackets to only select the columns you want in your
> DataFrame

**Make sure to call your `DataFrame` by typing it’s name as the last
line of your code cell** Then, you will be able to run the test cell
below and find out if your answer is correct.


```python
rapid_df = rapid_df[['PRCP', 'TOBS']]
rapid_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PRCP</th>
      <th>TOBS</th>
    </tr>
    <tr>
      <th>DATE</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1949-10-01</th>
      <td>0.00</td>
      <td>51.0</td>
    </tr>
    <tr>
      <th>1949-10-02</th>
      <td>0.00</td>
      <td>51.0</td>
    </tr>
    <tr>
      <th>1949-10-03</th>
      <td>0.00</td>
      <td>52.0</td>
    </tr>
    <tr>
      <th>1949-10-04</th>
      <td>0.00</td>
      <td>45.0</td>
    </tr>
    <tr>
      <th>1949-10-05</th>
      <td>0.00</td>
      <td>50.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2024-04-30</th>
      <td>0.00</td>
      <td>44.0</td>
    </tr>
    <tr>
      <th>2024-05-01</th>
      <td>0.00</td>
      <td>33.0</td>
    </tr>
    <tr>
      <th>2024-05-02</th>
      <td>0.35</td>
      <td>39.0</td>
    </tr>
    <tr>
      <th>2024-05-04</th>
      <td>0.00</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2024-05-05</th>
      <td>0.00</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>26111 rows × 2 columns</p>
</div>




```python
# DO NOT MODIFY THIS TEST CELL
tmax_df_resp = _
points = 0

summary = [round(val, 2) for val in tmax_df_resp.mean().values]
if summary == [0.05, 54.53]:
    points += 4
    print('\u2705 Great work! You correctly downloaded data.')
else:
    print('\u274C Oops - your data are not correct.')
print('You earned {} of 5 points for downloading data'.format(points))
```

    ❌ Oops - your data are not correct.
    You earned 0 of 5 points for downloading data


------------------------------------------------------------------------

## Plot the precpitation column (PRCP) vs time to explore the data

Plotting in Python is easy, but not quite this easy:


```python
rapid_df.plot(y='TOBS')
```




    <Axes: xlabel='DATE'>




    
![png](rapidcity_weather_analysis_files/rapidcity_weather_analysis_27_1.png)
    


> ****Label and describe your plots****
>
> <figure>
> <img src="https://imgs.xkcd.com/comics/convincing.png"
> alt="Source: https://xkcd.com/833" />
> <figcaption aria-hidden="true">Source: https://xkcd.com/833</figcaption>
> </figure>
>
> Make sure each plot has:
>
> -   A title that explains where and when the data are from
> -   x- and y- axis labels with **units** where appropriate
> -   A legend where appropriate

You’ll always need to add some instructions on labels and how you want
your plot to look.

> **<i class="fa fa-solid fa-keyboard fa-large" aria-label="keyboard"></i>
> Your task:**
>
> 1.  Change `dataframe` to **your** `DataFrame` name.
> 2.  Change `y=` to the name of your **observed temperature** column
>     name.
> 3.  Use the `title`, `ylabel`, and `xlabel` parameters to add key text
>     to your plot.
> 4.  Adjust the size of your figure using `figsize=(x,y)` where `x` is
>     figure width and `y` is figure height
>
> > **HINT:** labels have to be a *type* in Python called a **string**.
> > You can make a string by putting quotes around your label, just like
> > the column names in the sample code (eg `y='TOBS'`).


```python
# Plot the data using .plot
rapid_df.plot(
    y='TOBS',
    title='Rapid City Daily Temperature',
    xlabel='Date',
    ylabel='Temperature (F)',
    legend=False,
    color='orange',
    figsize=(10,5))
rapid_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PRCP</th>
      <th>TOBS</th>
    </tr>
    <tr>
      <th>DATE</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1949-10-01</th>
      <td>0.00</td>
      <td>51.0</td>
    </tr>
    <tr>
      <th>1949-10-02</th>
      <td>0.00</td>
      <td>51.0</td>
    </tr>
    <tr>
      <th>1949-10-03</th>
      <td>0.00</td>
      <td>52.0</td>
    </tr>
    <tr>
      <th>1949-10-04</th>
      <td>0.00</td>
      <td>45.0</td>
    </tr>
    <tr>
      <th>1949-10-05</th>
      <td>0.00</td>
      <td>50.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2024-04-30</th>
      <td>0.00</td>
      <td>44.0</td>
    </tr>
    <tr>
      <th>2024-05-01</th>
      <td>0.00</td>
      <td>33.0</td>
    </tr>
    <tr>
      <th>2024-05-02</th>
      <td>0.35</td>
      <td>39.0</td>
    </tr>
    <tr>
      <th>2024-05-04</th>
      <td>0.00</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2024-05-05</th>
      <td>0.00</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>26111 rows × 2 columns</p>
</div>




    
![png](rapidcity_weather_analysis_files/rapidcity_weather_analysis_29_1.png)
    


> **<i class="fa fa-solid fa-pepper-hot fa-large" aria-label="pepper-hot"></i>
> Want an EXTRA CHALLENGE?**
>
> There are many other things you can do to customize your plot. Take a
> look at the [pandas plotting
> galleries](https://pandas.pydata.org/docs/user_guide/visualization.html)
> and the [documentation of
> plot](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.html)
> to see if there’s other changes you want to make to your plot. Some
> possibilities include:
>
> -   Remove the legend since there’s only one data series
> -   Increase the figure size
> -   Increase the font size
> -   Change the colors
> -   Use a bar graph instead (usually we use lines for time series, but
>     since this is annual it could go either way)
> -   Add a trend line
>
> Not sure how to do any of these? Try searching the internet, or asking
> an AI!

------------------------------------------------------------------------

> **<i class="fa fa-solid fa-pepper-hot fa-large" aria-label="pepper-hot"></i>
> Convert units**
>
> Modify the code below to **add a column that includes temperature in
> Celsius**. The code below was written by your colleague. Can you fix
> this so that it correctly calculates temperature in Celsius and adds a
> new column?


```python
# Convert to celcius
rapid_df['TCel'] = (rapid_df['TOBS'] - 32) * 5 / 9
rapid_df
```

    /tmp/ipykernel_18301/1561760456.py:2: SettingWithCopyWarning: 
    A value is trying to be set on a copy of a slice from a DataFrame.
    Try using .loc[row_indexer,col_indexer] = value instead
    
    See the caveats in the documentation: https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#returning-a-view-versus-a-copy
      rapid_df['TCel'] = (rapid_df['TOBS'] - 32) * 5 / 9





<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PRCP</th>
      <th>TOBS</th>
      <th>TCel</th>
    </tr>
    <tr>
      <th>DATE</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1949-10-01</th>
      <td>0.00</td>
      <td>51.0</td>
      <td>10.555556</td>
    </tr>
    <tr>
      <th>1949-10-02</th>
      <td>0.00</td>
      <td>51.0</td>
      <td>10.555556</td>
    </tr>
    <tr>
      <th>1949-10-03</th>
      <td>0.00</td>
      <td>52.0</td>
      <td>11.111111</td>
    </tr>
    <tr>
      <th>1949-10-04</th>
      <td>0.00</td>
      <td>45.0</td>
      <td>7.222222</td>
    </tr>
    <tr>
      <th>1949-10-05</th>
      <td>0.00</td>
      <td>50.0</td>
      <td>10.000000</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2024-04-30</th>
      <td>0.00</td>
      <td>44.0</td>
      <td>6.666667</td>
    </tr>
    <tr>
      <th>2024-05-01</th>
      <td>0.00</td>
      <td>33.0</td>
      <td>0.555556</td>
    </tr>
    <tr>
      <th>2024-05-02</th>
      <td>0.35</td>
      <td>39.0</td>
      <td>3.888889</td>
    </tr>
    <tr>
      <th>2024-05-04</th>
      <td>0.00</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2024-05-05</th>
      <td>0.00</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>26111 rows × 3 columns</p>
</div>




```python
# DO NOT MODIFY THIS TEST CELL
tmax_df_resp = _
points = 0

if isinstance(tmax_df_resp, pd.DataFrame):
    points += 1
    print('\u2705 Great work! You called a DataFrame.')
else:
    print('\u274C Oops - make sure to call your DataFrame for testing.')

summary = [round(val, 2) for val in tmax_df_resp.mean().values]
if summary == [0.05, 54.53, 12.52]:
    points += 4
    print('\u2705 Great work! You correctly converted to Celcius.')
else:
    print('\u274C Oops - your data are not correct.')
print('You earned {} of 5 points for converting to Celcius'.format(points))
```

    ✅ Great work! You called a DataFrame.
    ❌ Oops - your data are not correct.
    You earned 1 of 5 points for converting to Celcius


> **<i class="fa fa-solid fa-pepper-hot fa-large" aria-label="pepper-hot"></i>
> Want an EXTRA CHALLENGE?**
>
> 1.  As you did above, rewrite the code to be more expressive
> 2.  Using the code below as a framework, write and apply a
>     **function** that converts to Celcius. \> **Functions** let you
>     reuse code you have already written
> 3.  You should also rewrite this function and parameter names to be
>     more expressive.


```python
def convert_to_celcius(fahrenheit):
    """Convert temperature to Celcius"""
    return (fahrenheit - 32) * 5 / 9

rapid_df['celcius_column'] = rapid_df['TOBS'].apply(convert_to_celcius)
rapid_df
```

    /tmp/ipykernel_18301/1212548583.py:5: SettingWithCopyWarning: 
    A value is trying to be set on a copy of a slice from a DataFrame.
    Try using .loc[row_indexer,col_indexer] = value instead
    
    See the caveats in the documentation: https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#returning-a-view-versus-a-copy
      rapid_df['celcius_column'] = rapid_df['TOBS'].apply(convert_to_celcius)





<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PRCP</th>
      <th>TOBS</th>
      <th>TCel</th>
      <th>celcius_column</th>
    </tr>
    <tr>
      <th>DATE</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1949-10-01</th>
      <td>0.00</td>
      <td>51.0</td>
      <td>10.555556</td>
      <td>10.555556</td>
    </tr>
    <tr>
      <th>1949-10-02</th>
      <td>0.00</td>
      <td>51.0</td>
      <td>10.555556</td>
      <td>10.555556</td>
    </tr>
    <tr>
      <th>1949-10-03</th>
      <td>0.00</td>
      <td>52.0</td>
      <td>11.111111</td>
      <td>11.111111</td>
    </tr>
    <tr>
      <th>1949-10-04</th>
      <td>0.00</td>
      <td>45.0</td>
      <td>7.222222</td>
      <td>7.222222</td>
    </tr>
    <tr>
      <th>1949-10-05</th>
      <td>0.00</td>
      <td>50.0</td>
      <td>10.000000</td>
      <td>10.000000</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2024-04-30</th>
      <td>0.00</td>
      <td>44.0</td>
      <td>6.666667</td>
      <td>6.666667</td>
    </tr>
    <tr>
      <th>2024-05-01</th>
      <td>0.00</td>
      <td>33.0</td>
      <td>0.555556</td>
      <td>0.555556</td>
    </tr>
    <tr>
      <th>2024-05-02</th>
      <td>0.35</td>
      <td>39.0</td>
      <td>3.888889</td>
      <td>3.888889</td>
    </tr>
    <tr>
      <th>2024-05-04</th>
      <td>0.00</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2024-05-05</th>
      <td>0.00</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>26111 rows × 4 columns</p>
</div>



## Subsetting and Resampling

Often when working with time-series data you may want to focus on a
shorter window of time, or look at weekly, monthly, or annual summaries
to help make the analysis more manageable.

> **<i class="fa fa-solid fa-glasses fa-large" aria-label="glasses"></i>
> Read more**
>
> Read more about
> [subsetting](https://www.earthdatascience.org/courses/use-data-open-source-python/use-time-series-data-in-python/date-time-types-in-pandas-python/subset-time-series-data-python/)
> and
> [resampling](https://www.earthdatascience.org/courses/use-data-open-source-python/use-time-series-data-in-python/date-time-types-in-pandas-python/resample-time-series-data-pandas-python/)
> time-series data in our Learning Portal.

For this demonstration, we will look at the last 40 years worth of data
and resample to explore a summary from each year that data were
recorded.

> **<i class="fa fa-solid fa-keyboard fa-large" aria-label="keyboard"></i>
> Your task**
>
> 1.  Replace `start-year` and `end-year` with 1983 and 2023
> 2.  Replace `dataframe` with the name of **your** data
> 3.  Replace `new_dataframe` with something more expressive
> 4.  Call your new variable
> 5.  Run the cell


```python
# Subset the data
rapid_89_23 = rapid_df['1989':'2023']
rapid_89_23
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PRCP</th>
      <th>TOBS</th>
      <th>TCel</th>
      <th>celcius_column</th>
    </tr>
    <tr>
      <th>DATE</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1989-01-01</th>
      <td>0.00</td>
      <td>7.0</td>
      <td>-13.888889</td>
      <td>-13.888889</td>
    </tr>
    <tr>
      <th>1989-01-02</th>
      <td>0.00</td>
      <td>25.0</td>
      <td>-3.888889</td>
      <td>-3.888889</td>
    </tr>
    <tr>
      <th>1989-01-03</th>
      <td>0.00</td>
      <td>19.0</td>
      <td>-7.222222</td>
      <td>-7.222222</td>
    </tr>
    <tr>
      <th>1989-01-04</th>
      <td>0.00</td>
      <td>47.0</td>
      <td>8.333333</td>
      <td>8.333333</td>
    </tr>
    <tr>
      <th>1989-01-05</th>
      <td>0.00</td>
      <td>27.0</td>
      <td>-2.777778</td>
      <td>-2.777778</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2023-12-27</th>
      <td>0.31</td>
      <td>32.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2023-12-28</th>
      <td>0.00</td>
      <td>17.0</td>
      <td>-8.333333</td>
      <td>-8.333333</td>
    </tr>
    <tr>
      <th>2023-12-29</th>
      <td>0.00</td>
      <td>28.0</td>
      <td>-2.222222</td>
      <td>-2.222222</td>
    </tr>
    <tr>
      <th>2023-12-30</th>
      <td>0.00</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2023-12-31</th>
      <td>0.00</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>12054 rows × 4 columns</p>
</div>




```python
# DO NOT MODIFY THIS TEST CELL
df_resp = _
points = 0

if isinstance(df_resp, pd.DataFrame):
    points += 1
    print('\u2705 Great work! You called a DataFrame.')
else:
    print('\u274C Oops - make sure to call your DataFrame for testing.')

summary = [round(val, 2) for val in df_resp.mean().values]
if summary == [0.06, 55.67, 13.15]:
    points += 5
    print('\u2705 Great work! You correctly converted to Celcius.')
else:
    print('\u274C Oops - your data are not correct.')
print('You earned {} of 5 points for subsetting'.format(points))
```

    ✅ Great work! You called a DataFrame.
    ❌ Oops - your data are not correct.
    You earned 1 of 5 points for subsetting


## Now we are ready to calculate annual statistics

Here you will **resample** the 1983-2023 data to look the annual mean
values.

> **<i class="fa fa-solid fa-keyboard fa-large" aria-label="keyboard"></i>
> Resample your data**
>
> 1.  Replace `new_dataframe` with the variable you created in the cell
>     above where you subset the data
> 2.  Replace `'TIME'` with a `'W'`, `'M'`, or `'Y'` depending on
>     whether you’re doing a weekly, monthly, or yearly summary
> 3.  Replace `STAT` with a `sum`, `min`, `max`, or `mean` depending on
>     what kind of statistic you’re interested in calculating.
> 4.  Replace `resampled_data` with a more expressive variable name
> 5.  Call your new variable
> 6.  Run the cell


```python
# Resample the data to look at yearly mean values
rapid_annual_avg_temp = rapid_89_23.resample('YS').mean()
rapid_annual_avg_temp
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PRCP</th>
      <th>TOBS</th>
      <th>TCel</th>
      <th>celcius_column</th>
    </tr>
    <tr>
      <th>DATE</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1989-01-01</th>
      <td>0.056359</td>
      <td>38.072829</td>
      <td>3.373794</td>
      <td>3.373794</td>
    </tr>
    <tr>
      <th>1990-01-01</th>
      <td>0.039068</td>
      <td>40.363112</td>
      <td>4.646174</td>
      <td>4.646174</td>
    </tr>
    <tr>
      <th>1991-01-01</th>
      <td>0.056875</td>
      <td>39.945869</td>
      <td>4.414372</td>
      <td>4.414372</td>
    </tr>
    <tr>
      <th>1992-01-01</th>
      <td>0.036714</td>
      <td>39.525862</td>
      <td>4.181034</td>
      <td>4.181034</td>
    </tr>
    <tr>
      <th>1993-01-01</th>
      <td>0.055881</td>
      <td>35.522581</td>
      <td>1.956989</td>
      <td>1.956989</td>
    </tr>
    <tr>
      <th>1994-01-01</th>
      <td>0.034540</td>
      <td>39.479769</td>
      <td>4.155427</td>
      <td>4.155427</td>
    </tr>
    <tr>
      <th>1995-01-01</th>
      <td>0.063609</td>
      <td>39.150568</td>
      <td>3.972538</td>
      <td>3.972538</td>
    </tr>
    <tr>
      <th>1996-01-01</th>
      <td>0.058785</td>
      <td>36.547486</td>
      <td>2.526381</td>
      <td>2.526381</td>
    </tr>
    <tr>
      <th>1997-01-01</th>
      <td>0.057634</td>
      <td>38.825073</td>
      <td>3.791707</td>
      <td>3.791707</td>
    </tr>
    <tr>
      <th>1998-01-01</th>
      <td>0.068343</td>
      <td>40.563739</td>
      <td>4.757633</td>
      <td>4.757633</td>
    </tr>
    <tr>
      <th>1999-01-01</th>
      <td>0.073104</td>
      <td>41.688202</td>
      <td>5.382335</td>
      <td>5.382335</td>
    </tr>
    <tr>
      <th>2000-01-01</th>
      <td>0.050771</td>
      <td>39.750751</td>
      <td>4.305973</td>
      <td>4.305973</td>
    </tr>
    <tr>
      <th>2001-01-01</th>
      <td>0.049639</td>
      <td>43.371134</td>
      <td>6.317297</td>
      <td>6.317297</td>
    </tr>
    <tr>
      <th>2002-01-01</th>
      <td>0.036126</td>
      <td>33.482143</td>
      <td>0.823413</td>
      <td>0.823413</td>
    </tr>
    <tr>
      <th>2003-01-01</th>
      <td>0.039186</td>
      <td>40.455253</td>
      <td>4.697363</td>
      <td>4.697363</td>
    </tr>
    <tr>
      <th>2004-01-01</th>
      <td>0.030242</td>
      <td>38.877828</td>
      <td>3.821016</td>
      <td>3.821016</td>
    </tr>
    <tr>
      <th>2005-01-01</th>
      <td>0.044620</td>
      <td>40.627119</td>
      <td>4.792844</td>
      <td>4.792844</td>
    </tr>
    <tr>
      <th>2006-01-01</th>
      <td>0.042870</td>
      <td>40.873278</td>
      <td>4.929599</td>
      <td>4.929599</td>
    </tr>
    <tr>
      <th>2007-01-01</th>
      <td>0.038515</td>
      <td>34.806931</td>
      <td>1.559406</td>
      <td>1.559406</td>
    </tr>
    <tr>
      <th>2008-01-01</th>
      <td>0.025892</td>
      <td>34.204969</td>
      <td>1.224983</td>
      <td>1.224983</td>
    </tr>
    <tr>
      <th>2009-01-01</th>
      <td>0.053828</td>
      <td>35.871324</td>
      <td>2.150735</td>
      <td>2.150735</td>
    </tr>
    <tr>
      <th>2010-01-01</th>
      <td>0.056767</td>
      <td>39.012384</td>
      <td>3.895769</td>
      <td>3.895769</td>
    </tr>
    <tr>
      <th>2011-01-01</th>
      <td>0.060282</td>
      <td>40.313846</td>
      <td>4.618803</td>
      <td>4.618803</td>
    </tr>
    <tr>
      <th>2012-01-01</th>
      <td>0.019341</td>
      <td>42.008746</td>
      <td>5.560415</td>
      <td>5.560415</td>
    </tr>
    <tr>
      <th>2013-01-01</th>
      <td>0.060685</td>
      <td>38.392638</td>
      <td>3.551466</td>
      <td>3.551466</td>
    </tr>
    <tr>
      <th>2014-01-01</th>
      <td>0.057726</td>
      <td>39.211310</td>
      <td>4.006283</td>
      <td>4.006283</td>
    </tr>
    <tr>
      <th>2015-01-01</th>
      <td>0.057260</td>
      <td>41.351275</td>
      <td>5.195153</td>
      <td>5.195153</td>
    </tr>
    <tr>
      <th>2016-01-01</th>
      <td>0.039508</td>
      <td>42.161644</td>
      <td>5.645358</td>
      <td>5.645358</td>
    </tr>
    <tr>
      <th>2017-01-01</th>
      <td>0.034082</td>
      <td>41.013889</td>
      <td>5.007716</td>
      <td>5.007716</td>
    </tr>
    <tr>
      <th>2018-01-01</th>
      <td>0.057335</td>
      <td>36.670732</td>
      <td>2.594851</td>
      <td>2.594851</td>
    </tr>
    <tr>
      <th>2019-01-01</th>
      <td>0.085056</td>
      <td>36.159544</td>
      <td>2.310858</td>
      <td>2.310858</td>
    </tr>
    <tr>
      <th>2020-01-01</th>
      <td>0.044006</td>
      <td>41.023438</td>
      <td>5.013021</td>
      <td>5.013021</td>
    </tr>
    <tr>
      <th>2021-01-01</th>
      <td>0.032225</td>
      <td>40.363248</td>
      <td>4.646249</td>
      <td>4.646249</td>
    </tr>
    <tr>
      <th>2022-01-01</th>
      <td>0.028421</td>
      <td>39.331395</td>
      <td>4.072997</td>
      <td>4.072997</td>
    </tr>
    <tr>
      <th>2023-01-01</th>
      <td>0.046313</td>
      <td>40.144578</td>
      <td>4.524766</td>
      <td>4.524766</td>
    </tr>
  </tbody>
</table>
</div>




```python
# DO NOT MODIFY THIS TEST CELL
df_resp = _
points = 0

if isinstance(df_resp, pd.DataFrame):
    points += 1
    print('\u2705 Great work! You called a DataFrame.')
else:
    print('\u274C Oops - make sure to call your DataFrame for testing.')

summary = [round(val, 2) for val in df_resp.mean().values]
if summary == [0.06, 55.37, 12.99]:
    points += 5
    print('\u2705 Great work! You correctly converted to Celcius.')
else:
    print('\u274C Oops - your data are not correct.')
print('You earned {} of 5 points for resampling'.format(points))
```

    ✅ Great work! You called a DataFrame.
    ❌ Oops - your data are not correct.
    You earned 1 of 5 points for resampling


> **<i class="fa fa-solid fa-keyboard fa-large" aria-label="keyboard"></i>
> Plot your resampled data**


```python
# Plot mean annual temperature values
rapid_annual_avg_temp.plot(
    y='TOBS',
    title='Rapid City Annual Average Temperature',
    xlabel='Date',
    ylabel='Temperature (F)',
    legend=False,
    color='lightgreen',
    figsize=(10,5))
rapid_annual_avg_temp
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PRCP</th>
      <th>TOBS</th>
      <th>TCel</th>
      <th>celcius_column</th>
    </tr>
    <tr>
      <th>DATE</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1989-01-01</th>
      <td>0.056359</td>
      <td>38.072829</td>
      <td>3.373794</td>
      <td>3.373794</td>
    </tr>
    <tr>
      <th>1990-01-01</th>
      <td>0.039068</td>
      <td>40.363112</td>
      <td>4.646174</td>
      <td>4.646174</td>
    </tr>
    <tr>
      <th>1991-01-01</th>
      <td>0.056875</td>
      <td>39.945869</td>
      <td>4.414372</td>
      <td>4.414372</td>
    </tr>
    <tr>
      <th>1992-01-01</th>
      <td>0.036714</td>
      <td>39.525862</td>
      <td>4.181034</td>
      <td>4.181034</td>
    </tr>
    <tr>
      <th>1993-01-01</th>
      <td>0.055881</td>
      <td>35.522581</td>
      <td>1.956989</td>
      <td>1.956989</td>
    </tr>
    <tr>
      <th>1994-01-01</th>
      <td>0.034540</td>
      <td>39.479769</td>
      <td>4.155427</td>
      <td>4.155427</td>
    </tr>
    <tr>
      <th>1995-01-01</th>
      <td>0.063609</td>
      <td>39.150568</td>
      <td>3.972538</td>
      <td>3.972538</td>
    </tr>
    <tr>
      <th>1996-01-01</th>
      <td>0.058785</td>
      <td>36.547486</td>
      <td>2.526381</td>
      <td>2.526381</td>
    </tr>
    <tr>
      <th>1997-01-01</th>
      <td>0.057634</td>
      <td>38.825073</td>
      <td>3.791707</td>
      <td>3.791707</td>
    </tr>
    <tr>
      <th>1998-01-01</th>
      <td>0.068343</td>
      <td>40.563739</td>
      <td>4.757633</td>
      <td>4.757633</td>
    </tr>
    <tr>
      <th>1999-01-01</th>
      <td>0.073104</td>
      <td>41.688202</td>
      <td>5.382335</td>
      <td>5.382335</td>
    </tr>
    <tr>
      <th>2000-01-01</th>
      <td>0.050771</td>
      <td>39.750751</td>
      <td>4.305973</td>
      <td>4.305973</td>
    </tr>
    <tr>
      <th>2001-01-01</th>
      <td>0.049639</td>
      <td>43.371134</td>
      <td>6.317297</td>
      <td>6.317297</td>
    </tr>
    <tr>
      <th>2002-01-01</th>
      <td>0.036126</td>
      <td>33.482143</td>
      <td>0.823413</td>
      <td>0.823413</td>
    </tr>
    <tr>
      <th>2003-01-01</th>
      <td>0.039186</td>
      <td>40.455253</td>
      <td>4.697363</td>
      <td>4.697363</td>
    </tr>
    <tr>
      <th>2004-01-01</th>
      <td>0.030242</td>
      <td>38.877828</td>
      <td>3.821016</td>
      <td>3.821016</td>
    </tr>
    <tr>
      <th>2005-01-01</th>
      <td>0.044620</td>
      <td>40.627119</td>
      <td>4.792844</td>
      <td>4.792844</td>
    </tr>
    <tr>
      <th>2006-01-01</th>
      <td>0.042870</td>
      <td>40.873278</td>
      <td>4.929599</td>
      <td>4.929599</td>
    </tr>
    <tr>
      <th>2007-01-01</th>
      <td>0.038515</td>
      <td>34.806931</td>
      <td>1.559406</td>
      <td>1.559406</td>
    </tr>
    <tr>
      <th>2008-01-01</th>
      <td>0.025892</td>
      <td>34.204969</td>
      <td>1.224983</td>
      <td>1.224983</td>
    </tr>
    <tr>
      <th>2009-01-01</th>
      <td>0.053828</td>
      <td>35.871324</td>
      <td>2.150735</td>
      <td>2.150735</td>
    </tr>
    <tr>
      <th>2010-01-01</th>
      <td>0.056767</td>
      <td>39.012384</td>
      <td>3.895769</td>
      <td>3.895769</td>
    </tr>
    <tr>
      <th>2011-01-01</th>
      <td>0.060282</td>
      <td>40.313846</td>
      <td>4.618803</td>
      <td>4.618803</td>
    </tr>
    <tr>
      <th>2012-01-01</th>
      <td>0.019341</td>
      <td>42.008746</td>
      <td>5.560415</td>
      <td>5.560415</td>
    </tr>
    <tr>
      <th>2013-01-01</th>
      <td>0.060685</td>
      <td>38.392638</td>
      <td>3.551466</td>
      <td>3.551466</td>
    </tr>
    <tr>
      <th>2014-01-01</th>
      <td>0.057726</td>
      <td>39.211310</td>
      <td>4.006283</td>
      <td>4.006283</td>
    </tr>
    <tr>
      <th>2015-01-01</th>
      <td>0.057260</td>
      <td>41.351275</td>
      <td>5.195153</td>
      <td>5.195153</td>
    </tr>
    <tr>
      <th>2016-01-01</th>
      <td>0.039508</td>
      <td>42.161644</td>
      <td>5.645358</td>
      <td>5.645358</td>
    </tr>
    <tr>
      <th>2017-01-01</th>
      <td>0.034082</td>
      <td>41.013889</td>
      <td>5.007716</td>
      <td>5.007716</td>
    </tr>
    <tr>
      <th>2018-01-01</th>
      <td>0.057335</td>
      <td>36.670732</td>
      <td>2.594851</td>
      <td>2.594851</td>
    </tr>
    <tr>
      <th>2019-01-01</th>
      <td>0.085056</td>
      <td>36.159544</td>
      <td>2.310858</td>
      <td>2.310858</td>
    </tr>
    <tr>
      <th>2020-01-01</th>
      <td>0.044006</td>
      <td>41.023438</td>
      <td>5.013021</td>
      <td>5.013021</td>
    </tr>
    <tr>
      <th>2021-01-01</th>
      <td>0.032225</td>
      <td>40.363248</td>
      <td>4.646249</td>
      <td>4.646249</td>
    </tr>
    <tr>
      <th>2022-01-01</th>
      <td>0.028421</td>
      <td>39.331395</td>
      <td>4.072997</td>
      <td>4.072997</td>
    </tr>
    <tr>
      <th>2023-01-01</th>
      <td>0.046313</td>
      <td>40.144578</td>
      <td>4.524766</td>
      <td>4.524766</td>
    </tr>
  </tbody>
</table>
</div>




    
![png](rapidcity_weather_analysis_files/rapidcity_weather_analysis_42_1.png)
    


------------------------------------------------------------------------

> **<i class="fa fa-solid fa-pencil fa-large" aria-label="pencil"></i>
> Describe your plot**
>
> We like to use an approach called “Assertion-Evidence” for presenting
> scientific results. There’s a lot of video tutorials and example talks
> available on [the Assertion-Evidence web
> page](https://www.assertion-evidence.com/). The main thing you need to
> do now is to practice writing a **message** or **headline** rather
> than descriptions or topic sentences for the plot you just made (what
> they refer to as “visual evidence”).
>
> For example, it would be tempting to write something like “A plot of
> maximum annual temperature in Rapid City, Colorado over time
> (1983-2023)”. However, this doesn’t give the reader anything to look
> at, or explain why we made this particular plot (we know, you made
> **this** one because we told you to)
>
> Some alternatives for different plots of Rapid City temperature that
> are more of a starting point for a presentation or conversation are:
>
> -   Rapid City, SD experienced cooler than average temperatures in
>     1995
> -   Temperatures in Rapid City, SD appear to be on the rise over the
>     past 40 years
> -   Maximum annual temperatures in Rapid City, CO are becoming more
>     variable over the previous 40 years
>
> We could back up some of these claims with further analysis included
> later on, but we want to make sure that our audience has some guidance
> on what to look for in the plot.

------------------------------------------------------------------------

## **YOUR Rapid City PLOT HEADLINE HERE** 📰 🗞️ 📻

## Presented is the average temperture for Rapid City, SD from 1983 to 2023
From 1990 to 2023 the average temperature fluxuates from 40-35 degrees Fahrenheit

<figure>
<img
src="https://pics.craiyon.com/2023-07-12/1d858937f1104df68803a2994c90453a.webp"
alt="Writing bear" />
<figcaption aria-hidden="true">Writing bear</figcaption>
</figure>

> Image credit: https://www.craiyon.com/image/OAbZtyelSoS7FdGko6hvQg

------------------------------------------------------------------------

# **THIS ISN’T THE END!** 😄

**Don’t forget to *reproduce your analysis* in a new location or time!**

<img src="https://static.independent.co.uk/s3fs-public/thumbnails/image/2008/12/26/20/107000.jpg" height="150" style="padding: 1em; border-style: solid; border-color: grey;"/>

> Image source:
> https://www.independent.co.uk/climate-change/news/by-the-left-quick-march-the-emperor-penguins-migration-1212420.html

------------------------------------------------------------------------

## Your turn: pick a new location and/or measurement to plot 🌏 📈

Below (or in a new notebook!), recreate the workflow you just did in a
place that interests you OR with a different measurement. See the
instructions above to adapt the URL that we created for Rapid City, CO
using the NCEI API. You will need to make your own new Markdown and Code
cells below this one, or create a new notebook.

------------------------------------------------------------------------

## **Congratulations, you’re almost done with this coding challenge** 🤩 – now make sure that your code is *reproducible*

<img src="https://dfwurbanwildlife.com/wp-content/uploads/2018/03/SnowGeese16.jpg" height="150" style="padding: 1em; border-style: solid; border-color: grey;"/>

> Image source:
> https://dfwurbanwildlife.com/2018/03/25/chris-jacksons-dfw-urban-wildlife/snow-geese-galore/

> **<i class="fa fa-solid fa-keyboard fa-large" aria-label="keyboard"></i>
> Your task**
>
> 1.  If you didn’t already, go back to the code you modified about and
>     write more descriptive **comments** so the next person to use this
>     code knows what it does.
>
> <!-- -->
>
> 1.  Make sure to `Restart` and `Run all` up at the top of your
>     notebook. This will clear all your variables and make sure that
>     your code runs in the correct order. It will also export your work
>     in Markdown format, which you can put on your website.
>
> > **Always run your code start to finish before submitting!**
> >
> > Before you commit your work, make sure it runs **reproducibly** by
> > clicking:
> >
> > 1.  `Restart` (this button won’t appear until you’ve run some code),
> >     then
> > 2.  `Run All`

------------------------------------------------------------------------

## BONUS: Create a shareable Markdown of your work

Below is some code that you can run that will save a Markdown file of
your work that is easily shareable and can be uploaded to GitHub Pages.
You can use it as a starting point for writing your portfolio post!


```python
%%capture
%%bash
jupyter nbconvert *.ipynb --to markdown
```
