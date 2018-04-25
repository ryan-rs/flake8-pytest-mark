===============
Release Process
===============

The easiest way to release a new version of flake8-pytest-mark is to use make.

1. First you will need to know the username and password for the account you want to use to release to PyPI with

2. You will need to make sure that you are on the master branch, your working directory is clean and up to date.

3. Decide if you are going to increment the major, minor, or patch version.  You can refer to semver_ to help you make that decision.

4. Use the `release` task.  You will need to set the environment variable `BUMP` to 'major', 'minor', or 'patch'.
**make release** ::

    BUMP=minor make release
5. The task will stop and prompt you for you PyPI username and password if you dont have these set in your `.pypirc` file.

6. Once the task has successfully completed you need to push the tag and commit.
**push tag** ::

    git push origin && git push origin refs/tags/<tagname>

.. _semver: https://semver.org