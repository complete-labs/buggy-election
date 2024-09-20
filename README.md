## What is this?

The current polling system has several key features that are essential for
comprehensive poll management. Users have control over the polls they create and
participate in. Specifically, the system should allow users to close polls, add new
polls with various options, and view all closed polls.

## Existing Capabilities
1. Ability to "create" and “close” a poll (Question) via Django admin.
2. Ability to view all the closed polls with votes.

## Local set up

```
# Set up your virtual env
python -m venv buggy-election
source buggy-election/bin/activate

# Install the requirements
pip install -r requirements.txt

# Run the DB migrations
python manage.py migrate

# Run the server
python manage.py runserver

```

## Django admin

The Django admin is served on the default path `/admin` and a super user is created by default with username `admin` and password `coderpad`.

## Bugs

1. The voting seems to be broken.
2. Once you close the poll, it looks like you can still vote.
3. A newly created poll says "This poll is more than a day old" message, which seems to be incorrect.
4. The polls should be sorted "most recently created first" on the homepage.
5. Deleting a question via Django admin does not delete the associated choices.

All bugs have 1-liner fixes. Good luck!