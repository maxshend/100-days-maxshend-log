# #100DaysOfCode Log - Round 1 - Maksim Shendrik

Started on September 12, Saturday, 2020.

## Log
### Day 1: September 12

Started implementation of an authentication/authorization service written in Go. Basic project set up.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/96bbc77807cff233b5d460b9b4014a0bab0e245a)
### Day 2: September 13

Trying to figure out how to handle database migrations in a Go app.
### Day 3: September 14

Set up simple database migrations handling. Added migration files for basic database model of the authentication service.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/41eedf61bac9da2d839708aa4b4c50721569dd4a)
### Day 4: September 15

Learned how to organize database access in an application using dependency injection.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/726a9cba0a29222edc12edbd515feda37f343252)
### Day 5: September 16

Learning about handling HTTP requests in Go. Created "dumb" handler for email registration to define basic steps of the handler.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/7c8a7fbbe52a8aa6c4423e3074a1742768933ec1)
### Day 6: September 17

Added password hashing. Created a few helpers for request handlers. Need to learn about [layout for Go application projects](https://github.com/golang-standards/project-layout). 

[Link to work](https://github.com/maxshend/tiny-goauth/commit/d8872214d60d491bf6fd026242012d2f8a542537)
### Day 7: September 18

Learning about unit testing in Go. Added user struct validations and unit tests to test this validations.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/6f3d7e451627d9070885f702691f7367fd7f5b9e)
### Day 8: September 19

Learned basisc of testing HTTP handlers in Go. Added unit tests for the current implementation of the sign up handler, but only for cases of responses with errors. Need to learn about mocking database calls. Started to read [Learn Go with Tests](https://github.com/quii/learn-go-with-tests), learned about test helpers and subtests.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/5c27346a7ee7b7ea5e7f0c6df112857853405c28)
### Day 9: September 20

Added more informative validation errors. Moving towards translatable error messages. Made string literals (like "application/json", "Content-Type") package-level constants so I don't have to type them over and over.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/d34e48ff4c1763af37e81d6c2758a09b086159a7)
### Day 10: September 21

Created interface DataLayer that wraps methods for the database access. This interface allows me to write unit tests without hitting the database. Added named return values for the init validator function to make it more clear.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/b13654ff4d35815c8878b183afbf302c7c688e45)
### Day 11: September 22

Set up hot reloading to speed up my development. Added custom validation for user's email uniqueness. Learned about cyclic dependency and why it's bad.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/2cd97bd167b2331cb43917f4b60ba99e94d129e6)

[Link to work](https://github.com/maxshend/tiny-goauth/commit/2eef47a94ee827205324746638b24024052b31da)

### Day 12: September 23

Learning about using jwt for Authentication in a Go app. Playing around with jwt libary. Change arguments for the method that checks existing db records to make it more safe. Add migration tasks to Makefile.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/07dfedca0b68a84c960720a6900dec200346c320)

### Day 13: September 24

Created a struct to organize authentication tokens details. Created a function that generates JWT access and refresh tokens that will be used in the authentication flow.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/2f6c587180578c4147d41db6ae6c78ff8e496a6c)
