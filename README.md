# youtube_search

Python function for searching for youtube videos to avoid using their heavily rate-limited API

To avoid using the API, this uses the form on the youtube homepage and scrapes the resulting page.

## Changes in this fork

Every results now contains a field "official_artist".
If the value is true, the video was uploaded to an official artist channel or a YouTube channel with the name "&lt;Artist Name&gt; - Topic".

## Example Usage

For a basic search (and all of the current functionality), you can use the search tool as follows:

```pip install youtube-search```

```python
from youtube_search import YoutubeSearch

results = YoutubeSearch('search terms', max_results=10).to_json()

print(results)

# returns a json string

########################################

results = YoutubeSearch('search terms', max_results=10).to_dict()

print(results)
# returns a dictionary
```
