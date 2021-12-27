# gudlift-registration

1. Why


    This is a proof of concept (POC) project to show a light-weight version of our competition booking platform. The aim is the keep things as light as possible, and use feedback from the users to iterate.

2. Getting Started

    This project uses the following technologies:

    * Python v3.x+

    * [Flask](https://flask.palletsprojects.com/en/1.1.x/)

        Please note that we use Flask v.1.1, which is not the latest version. As such, do not try to upgrade any library without checking compatibility.


    * [Virtual environment](https://virtualenv.pypa.io/en/stable/installation.html)

        This ensures you'll be able to install the correct packages without interfering with Python on your machine.

        Before you begin, please ensure you have this installed globally.

    * [Pytest](https://docs.pytest.org/en/6.2.x/)

        We use pytest for testing.


3. Installation

    - After cloning, change into the directory and type <code>virtualenv .</code>. This will then set up a a virtual python environment within that directory.

    - Next, type <code>source bin/activate</code>. You should see that your command prompt has changed to the name of the folder. This means that you can install packages in here without affecting affecting files outside. To deactivate, type <code>deactivate</code>

    - Rather than hunting around for the packages you need, you can install in one step. Type <code>pip install -r requirements.txt</code>. This will install all the packages listed in the respective file. If you install a package, make sure others know by updating the requirements.txt file. An easy way to do this is <code>pip freeze > requirements.txt</code>

    - Environment variables are already set in the .env and .flaskenv files.

    - You should now be ready to test the application. In the directory, type either <code>flask run</code> or <code>python -m flask run</code>. The app should respond with an address you should be able to go to using your browser.

4. Current Setup

    The app is powered by [JSON files](https://www.tutorialspoint.com/json/json_quick_guide.htm). This is to get around having a DB until we actually need one. The main ones are:

    * competitions.json - list of competitions
    * clubs.json - list of clubs with relevant information. You can look here to see what email addresses the app will accept for login.

5. Testing

    We use [Pytest](https://docs.pytest.org/en/6.2.x/) for testing, as well as [coverage](https://coverage.readthedocs.io/en/coverage-5.1/) to check what code is covered by our test.

    To launch testing, please ensure that the MODE variable in the .env file is set to 'TESTING'.

    Use the console to navigate to the app's folder after activating your virtual environment, then run the command <code>pytest</code> on Windows or <code>python3 pytest</code> on other operating systems.

    To run Coverage, navigate to the app's folder and then type the command <code>coverage run -m pytest</code>.

    To run [Locust](https://github.com/locustio/locust/tree/1.2.3) so as to check performance, navigate to the app's folder and type <code>locust</code>. Then, go to the page http://localhost:8089 on your browser.

6. General conventions

    We follow the python naming convention, which means that class names use pascalcase (MyClassName), functions use under_score (my_function_name) and constant use capslocks (CONSTANT).

    For general formating, we use the PEP, though with more liberal # commenting for clarity's sake.
