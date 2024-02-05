# Comparing dogs and cat ownerships in Taiwan

#### Check out my project over [here](https://sabinahung.github.io/pet-ownership-taiwan/)!

## Goal
I initally wanted to find out: 
1. Dog-cat ownership change by city/county over the years
2. Whether dog ownership correlates with number of stray dogs
3. Line chart of changes of pet ownership

## Findings
1. Cat popularity is on the rise but hasn't outnumbered household dogs
2. Keelung registered the most cats in 2023
3. Two counties showed up in both cat and dog top five lists

## Data collection process
I used two datasets to complete this project. 

1. One from the [open data site](https://data.coa.gov.tw/open_search.aspx?id=ccezNvv4oYbO) maintained by Ministry of Agriculture in Taiwan. 
2. Another from an [interactive map](https://www.pet.gov.tw/PetsMap/PetsMap.aspx) of the pet registration system.

The data collection for the open data was simple. They've complied the data so it is retrievable with an API and also available in csv.

The data collection of the interactive map was what took me the longest working on this project. I was accessing the data with Playwright and tried retrieving the table with `pd.read_html` and BeautifulSoup, but the table contains .many `</br>` and whitespaces which makes scraping difficult. At one point I was able to get the table into pandas dataframe, but it didn't come out in the format I prefered. All columns was squeezed into one cell. So I resorted to the most *straightforward* method -- copy and pasting to excel :)

I am glad
## Data analysis process


## What I learned

## What I wished to improve 

Potential Roadblocks:
There was plenty of missing data when I looked at the stray dogs data. So even though I have cleaned the data needed (?) for the analysis, the missing data could l lose its value? 
But the dog-cat ownership data was sufficient, will just visualize this if the stray dog one doesn’t work out. 
