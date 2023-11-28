# Accessing Reddit API

The Reddit API uses OAuth2 for authentication. To authenticate with the Reddit API, you need to create an app on Reddit following the instructions below.

1. Go to https://www.reddit.com/prefs/apps
    - Sign up for a Reddit account if you don't have one (Copy `username` and `password`)

2. Click on "are you a developer? create an app..."

3. Fill in the form (randomly)
    - name: random app name
    - type: select "script"
    - description: random description
    - about url, redirect url: random url (e.g., https://pyprogramming.net)

4. Click on "create app"

5. Copy `client ID` and `client secret`

These four pieces of information are needed to generate authentication headers using the `get_authheaders()` function.

```python
headers = get_authheaders(username, password, client_id, client_secret)
```

The authentication headers must be passed to the `requests.get()` when making a request to the Reddit API.

```python
response = requests.get(url, headers=headers, params=params)
```
