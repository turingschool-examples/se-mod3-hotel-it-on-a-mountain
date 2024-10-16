# Hotel It on the Mountain

This repository requires and has been tested on Ruby v3.2.2 and is based on Rails 7.1.4.

RSpec and Shoulda-Matchers have been installed and set up.

## Setup

1. fork this repo
2. clone your fork
3. `git clone <repo_name>`
4. `cd <repo_name>`
5. `bundle install`
6. `rails db:{drop,create,migrate,seed}`

When you run `bundle exec rspec` you should have 2 passing tests.

## Overview

You have been contracted by a luxurious mountain ski hotel & resort to keep track of all of the hotels, the rooms of that hotel, and the guests that stay there. 

* Hotels have a name and a location.
  * ex: `name: 'Echo Mountain Inn', location: 'Echo Mountain'`
* Rooms have a rate (price per night), and a suite designation. (For simplicity, let's assume the rate is a whole dollar price and use an integer.)
  * ex: `rate: 125, suite: "Presidential"`
* Guests have a name and the number of nights they'll be staying.
  * ex: `name: 'Charlize Theron', nights: 3`

## Model Setup
* Hotels have many Rooms. 
* Rooms belong to a Hotel.
* Guests have many Rooms.
* Rooms have many Guests.

Some of the initial model set up and testing has been done for you. Make sure your models & relationships are ready before starting endpoint development.

## Endpoints

We are not providing example responses - you may craft your responses in order to adhere to requirements. 

```
#1 Guest's Room History

When given a guest ID, endpoint returns a list of all the rooms they have stayed in and all the room attributes
```

```
#2 Add Guest to Room

When given a guest ID and room ID, endpoint will create relevant record(s) to add a guest to that room's history.
```

```
#3 Hotel Guest List

When given a hotel ID, endpoint returns a list of all the guests that have every stayed there in alphabetical order
```

## Extensions

* Room List, with count of guests listed as a room attribute