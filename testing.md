# Unit Test
This section was completed in index.js and index.test.js

# Functional Test
A shopping cart checkout feature that allows a user to check out as a guest (without an account), or as a logged-in user. They should be allowed to do either, but should be asked if they want to create an account or log in if they check out as a guest.

## Expectations:
* The user can use the checkout feature if they are either a guest or are logged in.
* If the user is a guest they should get an alert asking them if they would like to log in or proceed as a guest.
* If the user is a new guest they should get an alert asking if they would like to create a new account or proceed as a guest.
* If the user is a new guest, and does not want to create an account, they should be able to proceed checking out as a guest.
* If the user is logged in there should be no alerts displayed.

## Test Specs
GIVEN I am a new guest using the checkout feature

WHEN I go to checkout
THEN I see an alert asking me if I would like to create a new account or continue as a guest.

GIVEN I am a guest using the checkout feature

WHEN I go to checkout
THEN I see an alert asking me if I would like to sign in or continue as a guest.

GIVEN I am a new guest, that does not want to create an account, using the checkout feature

WHEN I go to checkout
THEN I see an alert asking if I would like to create an account, or proceed as a guest, and am able to proceed as a guest.

GIVEN I am logged in using the checkout feature

WHEN I go to checkout
THEN I see no alerts display on my screen.