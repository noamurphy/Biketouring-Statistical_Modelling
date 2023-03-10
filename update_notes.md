## Update notes

Commit 3: city_bikes.ipynb
- Added time.sleep(1) under each API call to avoid data loss while response is being gathered
- Integrated getNetworks_df() into getNetwork_id to reduce redundancy
- Standardized delay after calls into new constant CALL_DELAY

Commit 5: yelp_foursquare_EDA.ipynb
- changes to reduce calls made to foursquare API:
    - getPOIDetails_FSQR() function has been assimilated into getPOIs_FSQR()
    - adjusted call to provide 'rating' and 'stats'
- Added manual insertion of params into url
- Added call delay
- Changed API_KEY to FOURSQUARE_API_KEY for clarity
- Removed popularity and total_stats from Foursquare results

Commit 6: yelp_foursquare_EDA.ipynb
- Completed framework for interfacing with Yelp API
- Added API columns to tag the originating API

Commit 7: city_bikes.ipynb, yelp_foursquare_EDA.ipynb
- Ingested name and unique id for each bike station into to the pipeline at the city_bikes notebook
- adjusted yelp_foursquare_EDA notebook to process station names and identifiers

Commit 8: yelp_foursquare_EDA.ipynb
- changed df.append() methods to pd.concat() to avoid deprecation and eliminate excessive warning output
- fixed issue where yelp lat and long were not changed each iteration
- removed JSON import from IPython
- removed redundant casting to str from getLatLong()
- moved parameters to set-up, so that they can be changed simultaneously for both APIs

Commit 9: city_bikes.ipynb
- updated table outputs and format to be suitable for export to a structured database

Commit 10: yelp_foursquare_EDA.ipynb, city_bikes.ipynb
- note: yelp_foursquare_EDA.ipynb was supposed to be included in this commit and was NOT
- made minor changes to EDA and citybikes notebooks to prepare data for database
- reorganized citybikes notebook for increased autonomy
- changed export location of citybikes csv files to data folder

Commit 11: yelp_foursquare_EDA.ipynb, joining_data.ipynb
- updates to EDA notebook meant for commit 10
- finished framework for sql database creation and data insertion

Commit 13: yelp_foursquare_EDA.ipynb, joining_data.ipynb, model_building.ipynb, data
- fixed issue in model generation
- completed base Yelp vs Foursquare comparison
- added lineplot generation for yelp vs foursquare generation
- embedded lineplot in joining_data.csv
- test run of full pipeline completed successfully
- included necessary directories inside of data directory