# Rip Discs

A few scripts to make ripping your media easier (for personal backup purposes).

## rip-movie

## rip-episodes

## find-movie

Takes a movie name as its first argument and returns the correct title and year of its
release. Queries the [TMDb API][t] using [tmdbsimple][p], so install that first:

    pip install tmdbsimple

Register for an API key with TMDb, and put it in the file =~/.tmdb_api_key=.

Run the script by passing the movie name as the first argument:

    ❯ python find-movie TOP_GUN
    Top Gun (1986)

If a movie can't be found, it'll return error code 1 and report it:

    ❯ python find-movie AAAAA
    find-movie: movie not found

The movie returned will be the most popular one found that matches the string passed,
and unicode characters will be replaced to allow for filesystem compatibility:

    ❯ python find-movie 'the italian job'
    The Italian Job (2003)

    ❯ python find-movie amelie
    Am?lie (2001)



t: https://www.themoviedb.org/
p: https://github.com/celiao/tmdbsimple/
