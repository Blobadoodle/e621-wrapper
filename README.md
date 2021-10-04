# e621-wrapper
A python3 "library" for using the e621 api.

# Dependencies:

```bash
pip3 install ratelimit
pip3 install requests
```

# Tutorial

Here is a quick example showing some stuff you can do with this library.

Make sure you put the yiff.py file in your project directory first

Where it says `YOUR-CHOSEN-HEADER` in the yiff.py file (line 133) you should replace with something descriptive as said in the e621 api something like "Api-wrapper-test/0.1 (by *your-username*)"

I tried to add this as an argument in the yiff.api call but for whatever fucking reason it would not work at all.

```python3
import yiff

e6 = yiff.api("YOUR-E6-USERNAME", "YOUR-E6-API-KEY")
```

## Posts

Then you can do `e6.getpost(POSTID)` to get info about a post from its id and it will return an object with the "sub" python3 class. In this you can then do `sub.id, sub.tags, sub.score` etc etc.

Or if you want to search you can do `e6.search(LIST_OF_TAGS, POSTS_PER_PAGE, PAGE)` with list_of_tags being a list type and the other 2 being integers and it will return a list of `sub` class objects.

## Users

`e6.getuser(USER_ID)` is used to get info about a user from their id. It returns an object with the `user` class. you can then list `user.id, user.name user.forum_post_count` etc.

`e6.searchuser(USER_NAME)` works very similary to getuser except instead of taking their id it takes their username and out puts the same object.
