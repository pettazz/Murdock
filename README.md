Murdock
=======

I love it when a test plan comes together


- plugin based
    - activate/deactivate features via command line options
    - easily extended/updated
- multithreading that actually works
- doesn't require installation
    - runs in-place, with few dependencies
    - updates are as easy as git pull
    - jenkins can simply checkout the branch rather than depend on server's installation
- allows tagging of tests
    - dynamic test tags for things like "known issue" or "main-regression component"
    - run only specific tags, exclude specific tags
- hstf1 features that desperately needed refactoring are much improved
    - sharing data between plugins is standardized and not just shoveled in and out of a test object
    - take advantage of newer selenium features? 