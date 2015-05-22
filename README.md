# python3-oneall

Authentication with 20+ social networks using OneAll, with Django support.

This is a fork of `leandigo/django-oneall` with the following changes:

- **Python 3!** The modules I've forked from are Python 2 only.
  I could've just futurized instead, but I find it pollutes the code too much,
  and I actually want to help motivating the switch away from Py2.
- **Merged requisite OneAll support into the module,** leaving Django support as an optional component of the module.
  Support frameworks other than Django can be added in the same way.
  This is inspired by the architecture of `python-social-auth`.
- **New views,** compatible with `django.contrib.auth`, for ease of integration.
  This is very much in flux, but final goal is adding an `'^accounts/'` route,
  putting settings in, and done.

## Documentation for actual use can be found:

- [For the pure Python part of the module](django-oneall/README.rst)
- [And for the Django__ part of the module](pyoneall/README.rst)

## Sample Django settings

```python
ONEALL_SITE_NAME = 'py3tests'
ONEALL_PUBLIC_KEY = 'bf3a6a88-...'
ONEALL_PRIVATE_KEY = '35fc1a5e-...'
ONEALL_LOGIN_WIDGET = {
    'providers': ['amazon', 'blogger', 'disqus', 'draugiem', 'facebook',
                  'foursquare', 'github', 'google', 'instagram', 'linkedin',
                  'livejournal', 'mailru', 'odnoklassniki', 'openid',
                  'paypal', 'reddit', 'skyrock', 'stackexchange', 'steam',
                  'twitch', 'twitter', 'vimeo', 'vkontakte', 'windowslive',
                  'wordpress', 'yahoo', 'youtube'],
    'grid_sizes': [7, 5],
}
```