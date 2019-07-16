# IPGeo

## About IPGeo

The IPGeo repository on GitHub is a free version of the IP geolocation Module found on [Our Webpage](http://ipgeo.azurewebsites.net/).

Paid versions are described more in detail on [Our Webpage](http://ipgeo.azurewebsites.net/).

Our Free Version Includes 10 searches a month. Exceeding the 10 Searches a month will lead to an error as the server will not send back the IP Search Data.

Feel Free to check out the [IPGeoSearch](https://github.com/MatthiasRathbun/IPGeo-Search) library on GitHub for more ways to use our API!

## Requirements

Before running on your local computer, make sure you have `python 3.6+` with the latest version of `pandas` and `IPGeoSearch` installed and `ipList.txt` in the same folder as the python file.

To Install Pandas, run

```cmd
pip install pandas
```

To Install IPGeoSearch, run

```cmd
pip install IPGeoSearch
```

Request.txt should be formatted in one IP address per line like such:

```txt
8.8.8.8
8.8.8.8
8.8.8.8
8.8.8.8
8.8.8.8
```

## How To Use

### Python Example

 The `results` folder will have all the `.json` and `.csv` files stored in it after running.

To query IP using our sample file, run

```cmd
python request.py
```

in your command prompt environment with the pandas installed.

Files named `x.x.x.x.csv` and `x.x.x.x.json` are saved which have the relevant information regarding your IP Search. Files are named with the IP in the file Name. An example csv for a search of Google's IP `8.8.8.8` would be named `8.8.8.8.csv`.

Errors are more than likely caused by a non existent IP in the data base.

### Curl

You can also use `curl` to send requests on the command line as such:

```curl
curl https://ipgeo.azurewebsites.net/try -H "Content-type:application/json" -X POST -d '{"ip":"8.8.8.8"}' -o result.json
```

Using Curl is not recommended as it will not automatically parse the json into a csv and will not automate requests.
