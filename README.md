Late Show API
This project implements a Flask API for managing episodes and guest appearances on a fictional TV show. The API includes models for Episode, Guest, and Appearance, with appropriate relationships and validations.

Features
Models:

Episode: Represents a TV episode.
Guest: Represents a guest who appears on the show.
Appearance: Join table connecting Episode and Guest, with a rating.
Relationships:

An Episode has many Guests through Appearance.
A Guest has many Episodes through Appearance.
An Appearance belongs to both an Episode and a Guest.
Validations:

Appearance model validates that rating is between 1 and 5 (inclusive).
API Endpoints
GET /episodes
Returns a list of all episodes with their IDs, dates, and episode numbers.

GET /episodes/

Returns detailed information for a specific episode, including guest appearances and ratings.

GET /guests
Returns a list of all guests, including their names and occupations.

POST /appearances
Creates a new Appearance linking a guest and an episode with a rating. Validates the input and returns errors if invalid.
