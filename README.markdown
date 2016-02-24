## Readme

TrueReview is a web site that enables the post-publication review and ranking of publications. 

TrueReview is built as a web2py application.  This repository is a clone of web2py, with some additional files that are needed by true_review.  You can clone this repository with: 

    git clone --recursive https://github.com/lucadealfaro/true_review_web2py.git

This will clone the version of web2py we are using for TrueReview, which contains minor changes (app.yaml, routes.py) with respect to the official version, and also as git submodules:

- true_review (https://github.com/lucadealfaro/true_review), the TrueReview application proper,
- pydal (https://github.com/web2py/web2py.git) for database access.

Branches:

- master is the master branch of web2py
- true_review is the main branch of TrueReview, and contains additional things (site packages, routes, etc) needed by TrueReview.

When you check out the code, you are automatically on the true_review branch.

# Installation

To run locally, you will need:

- MySql running locally.  Version 5.5 is recommended as that is what we are using in the cloud. 
  Be sure to grant privileges in such a way that dev_appserver.py can create the databases it needs
  (see later).

- The MySql Python module.

- The Google Appengine source SDK. 

To run it, you can use a command line similar to the following one:

    dev_appserver.py --storage_path=<path_to_storage> --skip_sdk_update_check=True --port 8888 --admin_port 8844 <path>/true_review/
    
where of course you can choose any ports you want.  Above, <path_to_storage> is the path to a directory
where Google Appengine will store its copy of the mock datastore.  If you do not provide this
parameter, then Google Appengine will start each time with an empty datastore, which is not desirable.
