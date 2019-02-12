# Conflict Network Analysis

paper draft: https://www.overleaf.com/9127973233rkctnjhrbxdr


List of attributes/columns that scrapers should be capturing (when possible):

GROUPS:

0. ID
1. Religion (general category and also specific subset)
2. Location/area id
3. Number of members (estimate)
4. Territory size
5. GDP
6. GDP per person
7. Date of above measurements
8. One column per sources of information (source1, source2, source3, etc), would be source ids

In database, make a table GROUPS with each of these as a column. One date of measurement per row. Will have multiple rows of the same group, one row per measurement.
Foreign keys on: Religions, location, source columns

CONFLICT EVENTS:

0. ID
1. Number of people who fought
2. Number of casualties
3. Number of wounded
4. Number of buildings/structures destroyed
5. Location id
6. Date
7. Length of conflict
8. One column per sources of information (source1, source2, source3, etc)
9. Group ID
10. Source columns

In database, one row per agent in an event. If 3 agents are involved in an event, there are 3 rows for that event.
Foreign keys on: Location, group id, source columns

TRANSACTIONS:

0. ID
1. Items and amount traded (money, weapons, delegated, support, etc etc)
2. Time
3. Length of support
4. Group ID of giver
5. Group ID of receiver
6. Source ids
7. Location (if applicable) id

In database, one row per one-way transaction. If it was a 2-way transaction, there would be 2 rows for a single trade.
Foreign keys: Group ID, location, source

Then we will need tables for:
LOCATIONS (id, name, area, population, lat/lon of center)
SOURCES (id, url, name, date of publication)

5 tables total


So we need scrapers to get general inforamtion about the groups (to fill in the GROUPS table)
Scrapers to get events
And scrapers to get transactions
