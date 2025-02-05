## Modifications

This project was originally created by Zackary Young.

Modifications and maintenance by P-fury.



# UFC API

UFC API is a lightweight web crawler built in Python to retrieve data on UFC fighters and events.
After success in finding fighter, program gonna create .CSV file in program folde, titled as figher name.
Also gonna print JSON file with statistics.

# Installation

You can install UFC API using pip:

```
pip install ufc_api
```

# Usage

Usage is simple. To get stats on a particular fighter returned as a json:
Name can be with small letters but need 'space' between first name and last name.

```
>>> from ufc import get_fighter

>>> get_fighter('Jon Jones')

>>> {'name': 'Jon Jones',
 'nickname': 'Bones',
 'nationality': 'United States',
 'birthplace': 'Rochester, New York',
 'birthdate': 'Jul 19, 1987',
 'age': '35',
 'height': '6\'4"',
 'weight': '248 lbs',
 'association': 'Jackson-Wink MMA',
 'weight_class': 'Heavyweight',
 'wins': {'total': '27',
  'ko/tko': '10',
  'submissions': '7',
  'decisions': '10',
  'others': '0'},
 'losses': {'total': '1',
  'ko/tko': '0',
  'submissions': '0',
  'decisions': '0',
  'others': '1'},
 'fights': [{'name': 'UFC 285 - Jones vs. Gane',
   'date': 'Mar / 04 / 2023',
   'url': 'https://www.sherdog.com/events/UFC-285-Jones-vs-Gane-95232',
   'result': 'win',
   'method': 'Submission (Guillotine Choke)',
   'referee': 'Marc Goddard',
   'round': '1',
   'time': '2:04',
   'opponent': 'Ciryl Gane'},
   ...
   
```

To get data on an event, the usage is similar:
UFC events can be type without 'space'.

```
>>> from ufc import get_event

>>> get_event('UFC 280')

>>> {'name': 'UFC 280: Oliveira vs. Makhachev',
 'date': '2022-10-22',
 'location': 'Yas Island/Yas West United Arab Emirates',
 'venue': 'Etihad Arena',
 'fights': [{'weightclass': 'Lightweight Title',
   'red corner': {'name': 'Charles Oliveira',
    'ranking': 'Unranked',
    'odds': '+165',
    'link': 'https://www.ufc.com/athlete/charles-oliveira',
    'result': 'Loss'},
   'blue corner': {'name': 'Islam Makhachev',
    'ranking': 'Unranked',
    'odds': '-195',
    'link': 'https://www.ufc.com/athlete/islam-makhachev',
    'result': 'Win'},
   'round': '2',
   'time': '3:16',
   'method': 'Submission'},
  {'weightclass': 'Bantamweight Title',
   'red corner': {'name': 'Aljamain Sterling',
    'ranking': 'Unranked',
    'odds': '-175',
    'link': 'https://www.ufc.com/athlete/aljamain-sterling',
    'result': 'Win'},
   'blue corner': {'name': 'TJ Dillashaw',
    'ranking': 'Unranked',
    'odds': '+150',
    'link': 'https://www.ufc.com/athlete/tj-dillashaw',
    'result': 'Loss'},
   'round': '2',
   'time': '3:44',
   'method': 'KO/TKO'},
  {'weightclass': 'Bantamweight',
   'red corner': {'name': 'Petr Yan',
    'ranking': 'Unranked',
    'odds': '-275',
    'link': 'https://www.ufc.com/athlete/petr-yan',
    'result': 'Loss'},
   'blue corner': {'name': "Sean O'Malley",
    'ranking': 'Unranked',
    'odds': '+230',
    'link': 'https://www.ufc.com/athlete/sean-omalley',
    'result': 'Win'},
   'round': '3',
   'time': '5:00',
   'method': 'Decision - Split'},
   ...

```
