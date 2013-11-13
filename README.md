Murdock
=======

I love it when a test plan comes together


- plugin based
    - activate/deactivate features via command line options
    - easily extended/updated
- multithreading that actually works
- layers/filters that can hook into events like pass, fail, error, others
    - allow for definition of a layer as a set of validations/checks
    - on failure/error, current page state gets passed through each specified layer
    - example: 
        - some test says it uses the "error message layer"
            - layer definition that checks for some specific error message element and certain error messages are okay, so test should pass, others are bad, and test should fail
        - on error/failure, Murdock runs through loaded layers
        - "error message layer" sees that the error message is an acceptable one, so changes the test state to Pass
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