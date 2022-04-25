# Network Monitoring Tool Project for Rasperry Pi

## Creating Virtual Environment
```bash
python -m venv .venv
```

## Activating Virtual Environment

```bash 
source .venv/bin/activate
```

## Deactivating Virtual Environment

```bash
deactivate
```

## Installing Python Packages

```bash
python -m pip install psycopg2-binary
```

## Creating the Database

- The bash script inside this project only contains the path for Raspberry Pi's Linux system
- Make sure you have a /home/pi folder and clone this repository inside /home/pi/Repos (create Repos inside the /home/pi folder)
- Make sure postgres service is running on port 5432
- You can edit the script to choose the path of your preference or change the username as your own
- If all the above requirements are met:

Run the following commands:

```bash
chmod +x database/createdb.bash
```

```bash
./database/createdb.bash
```

Now the database is created and registered with the Raspberry Pi inside it. To start collecting data edit the file `client_scripts/monitor.py` to ping the desired IP, then you can set the script to run with a crontab job or run it manually.

## License
[MIT](https://github.com/pedro-carmine/networking-monitoring-raspberry/blob/main/LICENSE)

## External Library:
[pingparser](https://github.com/ssteinerx/pingparser)
