This project downloads cmip6 data.

I found that the easiest way to download this data is through the cds api.
https://cds.climate.copernicus.eu/#!/home

# Installation

First step is to create a user on the site: 
https://cds.climate.copernicus.eu/#!/home

Next step is to view and follow this page:
https://cds.climate.copernicus.eu/api-how-to
Ensure that you are logged in when viewing this site, such that the url: and key: are your actual keys and not just placeholders that says {api-key} ect.

Next you need to install the python package cdsapi, if you created this environment in pycharm using poetry it is likely already installed, otherwise just install it using either poetry or pip.
Finally you need to accept the terms of use for every dataset that you intent to use. This is done on the webpage by finding the data that you want and clicking the accept link at the bottom.

The CMIP6 climate projection dataset can be found here:
https://cds.climate.copernicus.eu/cdsapp#!/dataset/projections-cmip6?tab=form

This link also provides a handy interface for downloading data, and gives you the relevant API at the bottom once filled out.

# Quick start

Running the cmip6_downloader.py should download a bunch of cmip6 data, and should be easy to change to your particular needs. Note that you can only download one experiment and model at a time, hence the for loops.
Currently, the requests are sequential since they seem to be running relatively fast anyway, but could easily be made parallel (though I haven't tested whether the service allows for multiple requests in parallel).

Before you run it for real, make sure you adjust the area to the exact desired area.

