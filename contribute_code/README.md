# Contribute Code

The Minisat is an open source project that’s licensed under the GNU General Public License version 3. Contributions of all types are gladly accepted!

### Setting up the developement
To create a developement environment follow steps given for Minisat insallation at [chapter 1.2](/chapter_1/minisat_installation.html)

### Setting up test environment
In Minisat, [Pytest](https://docs.pytest.org/en/latest/) is used for testing and [Travis-ci](https://travis-ci.com/) for Continuous Integration.
All Minisat pull request are tested against testcases by [Travis-ci](https://travis-ci.org/miniSat/minisat). Sometimes tests fail, and when they do you can visit the test job that failed and view its console output.

It is possible for you to run these same tests locally. As most of our testing is done using Selenium. For that you need to download [Selenium](http://www.seleniumhq.org/) webdriver for Mozilla Firefox at [mozilla geckodriver](https://github.com/mozilla/geckodriver/releases)

Extract the driver.
Export path
```sh
export PATH=$PATH/:/path/of/driver
```
It will set a path variable to the webdriver.

And run the test
```sh
pytest
```

### Submit Patches
Patches to fix bugs or add new features are always appreciated. If you are going to work on a specific issue, make a note in the issue section so the developers will know what you’re working on. Please try to create an issue which is specific for your patch details.
- Fork the project and Clone it

On GitHub, navigate to the [Minisat repository](https://github.com/miniSat/minisat/). In the top-right corner of the page, click Fork.

![alt text](https://help.github.com/assets/images/help/repository/fork_button.jpg)

To clone repo
```sh
git clone https://github.com/<your-user-name>/minisat.git
```


- Create a feature/topic branch

```sh
git checkout -b <branchName>
```
- Make the changes required and commit the code

```sh
git add <modifiedFile(s)>
git commit -m "Fixes #<bug> - <message>"
```
- Push topic branch to your fork

```sh
git push origin <branchName>
```

- Issue a pull request

To create pull request follow the [link](https://help.github.com/articles/about-pull-requests/).





