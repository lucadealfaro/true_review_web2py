## Readme

TrueReview is a web site that enables the post-publication review and ranking of publications. 

TrueReview is built as a web2py application.  This repository is a clone of web2py, with some additional files that are needed by true_review.  You can clone this repository with: 

    git clone --recursive https://github.com/lucadealfaro/true_review_web2py.git

This will clone the version of web2py we are using for TrueReview, which contains minor changes (app.yaml, routes.py) with respect to the official version, and also as git submodules:

- true_review (https://github.com/lucadealfaro/true_review), the TrueReview application proper,
- pydal (https://github.com/web2py/web2py.git) for database access.
