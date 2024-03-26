# Comparing dogs and cat ownerships in Taiwan

### Check out my project over [here](https://sabinahung.github.io/pet-ownership-taiwan/)!

## Goal
I initally wanted to find out: 
1. Dog-cat ownership change by city/county over the years
2. Whether dog ownership correlates with number of stray dogs
3. Line chart of changes of pet ownership

## Findings
1. Cat popularity is on the rise but hasn't outnumbered household dogs
2. Keelung registered the most cats in 2023
3. Two counties showed up in both cat and dog top five lists

## Data collection 
I used two datasets to complete this project: 
1. One from the [open data site](https://data.coa.gov.tw/open_search.aspx?id=ccezNvv4oYbO) maintained by Ministry of Agriculture in Taiwan. 
2. Another from an [interactive map](https://www.pet.gov.tw/PetsMap/PetsMap.aspx) of the pet registration system.

The data collection for the open data was simple. They've complied the data so it is retrievable with an API and also available in csv.

The data collection of the interactive map was what took me the longest working on this project. I was accessing the data with Playwright and tried retrieving the table with `pd.read_html` and BeautifulSoup, but the table contains .many `</br>` and whitespaces which makes scraping difficult. At one point I was able to get the table into pandas dataframe, but it didn't come out in the format I prefered. All columns was squeezed into one cell. So I resorted to the most *straightforward* method -- copy and pasting to excel :) Nevertheless, I am glad that the excel sped up the data cleaning process very quick.  
## Data analysis 
Cleaning the [yearly household pets estimate](https://data.coa.gov.tw/open_search.aspx?id=ccezNvv4oYbO) was a pain. Although the data was published by city/county, not all counties are collected in each year, there are several counties weren't available for comparing across time. 

Second biggest challenge was the change of name in places. It also adds to the difficulty to compare same city/county across time. I later found out that the `cityID` column was consistent acorss geographical territory, that solved the difference-in-city-name problem. 

With yearly household pets estimate data, I removed all the counties that are not present throughout (they are the outlying islands) and sum all the household dog and cat estimates to get the national total of each year. 

And with the [pet registration data](https://www.pet.gov.tw/PetsMap/PetsMap.aspx), it provided both registered total and the total of household who came for pet registration. I calculated the average number cats and dogs per household by city/county to get the top 5 lists.
## What I learned
1. Don't get too hung up on one dataset!! Always have backup datasets or always be ready to look for other datasets!
2. Risk management! Know your time limit, it's okay to copy-paste! (Is it? I do wish to improve my scraping skills ultimately)
## What I wished to improve 
1. Spend more time on the write up
2. Get better at scraping 
3. Regression analysis on stray dog and dog ownership
4. <ins>Find out why there was a significant increase in 2023 pet registration data</ins>

