A Django middleware for verifying the user's age before allowing them access to a resource.
Developed for the purposes of the PSE Hackathon held in Sep 2024.

The user is expected to own an Android or iOS device with an **NFC reader** and a compatible passport.

### Installation

- pip install age_verification_psehack

In your Django project's `settings.py`:

Add the following line the bottom of the MIDDLEWARE section:

- "age_verification_psehack.middleware.AgeVerificationMiddleware"

Add a new AGE_VERIFICATION_PATHS setting containing all paths requiring age verification:

- AGE_VERIFICATION_PATHS = ['/protected_path1', '/protected/path2']


### Installing a local build (not from pypi):

In case if you need to make changes and test them, in the root of this repo run

python pip install build
python -m build

In the root of your Django project create a file `requirements.txt` with the following:

-e path/to/the/root/of/this/repo

Then run:

python -m pip install -r requirements.txt


