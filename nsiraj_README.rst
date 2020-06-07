Auth Changes
----------------

Original package didn't handle OAuth properly, so I made changes to make the redirect possible. Unfortunately, once you login via Goodreads, it doesn't take you back to the app. You will have to refresh the app and it will be logged in (I don't think this is something I can change from my end).

Currently, once you're loggin in Goodreads, you will be logged in the app.

Requirements:

- Need to have a login / authorize route for it to work properly
- Need to have a callback url prepared to send through: 

::

    oauth_callback = url_for('authorized', _external=True)