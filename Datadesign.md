# Data design

There are three collections/tables in the database design

Users - stores users
Jokes - a top level container with metadata about a joke, but mainly to generate a unique joke ID
JokePost - individual posts relating to a joke.

User={
  //
}

Joke={
  JokeID: String,
  upvotes: [{userid, voteType}],
  comments: [{userid, comment, time}]
}

jokePost={
  userid: String,
  jokeid: String,
  jokeWords: String,
  time: Date,
  ellapsedTime: Date,
}
