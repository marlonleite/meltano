## Extract

1 - meltano add loader target-postgres

2 - meltano add --custom extractor tap-postgres

3 - Check configs:
meltano config tap-postgres

meltano config target-postgres

4 - Add select to tap:

meltano select tap-postgres "palma-public-cnaes" "*"


5- Check select:
meltano select tap-postgres --list

6 - Optional check stream:

meltano invoke tap-postgres --discover > .meltano/run/tap-postgres/tap.properties.json


7 - Run

meltano elt tap-postgres target-postgres