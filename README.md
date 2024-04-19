# bagconv-docker

Convert the official Dutch building/dwelling administration into a simpler format.
Also includes a small and fast web service for sharing this data.

## Requirements

On a Debian based system:

    sudo apt install build-essential cmake sqlite3 libsqlite3-dev nlohmann-json3-dev zlib1g-dev wget unzip 7zip

Or just docker if you run via Docker. You need 109G (gigabyte) of free disk space to run.

## Running

Either run:

    bash run.sh

Or run via docker with:

    bash docker-run.sh

Note that a run may take half an hour.

## Results

After a run you will find the following directories in the project:

    20M     build
    3,1G    data
    96G     unpack
    9,7G    dist

The most valuable (IMHO) files are:

    8,8G    dist/bag.sqlite
    17M     dist/postcodes-nl.7z
    40M     dist/postcodes-nl-geo.7z

Check [postcodes-nl](https://github.com/mevdschee/postcodes-nl/) and [postcodes-nl-geo](https://github.com/mevdschee/postcodes-nl-geo/) to load the CSV into a SQL database using PHP. 

You may run the clean script to clean up all build files:

    bash clean.sh

This will free up all generated and downloaded data.
