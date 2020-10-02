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
### Day 14: September 25

Created a handler for email login HTTP request. Added unit tests to check HTTP status code of the response. Learned more details about Go slices.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/f2a3d8b2acc086d895b3d91979aaf25585b35939)
### Day 15: September 26

Created a function to validate Access JWT. Added respective unit tests. Learned about Table Driven Tests in Go.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/4f8640a397880b508cac96457b72fde1429541e3)
### Day 16: September 27

Created a struct for JWT claims. Set up connection to Redis from the app. Redis will be used in the JWT invalidation flow.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/a2202f4fb3d3c6da6a1e70c4bc48353556806c54)

[Link to work](https://github.com/maxshend/tiny-goauth/commit/3e8cee5d831f37e2a7ff9b88b41a5c0e03382d57)
### Day 17: September 28

Added logout HTTP handler. Organized storing of the access and refresh token UUID in the redis. Created a middleware handler for authenticated requests.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/4a173f30ee8227ec243231329f5b4e95f94c6e86)
### Day 18: September 29

Created an HTTP handler for getting an access token from a valid refresh token. 

[Link to work](https://github.com/maxshend/tiny-goauth/commit/3798beb9b031d00948ed3bf44eebc19c2006bdfa)
### Day 19: September 30

Learning about writing and storing Go app logs. Trying to figure out what and how to log. Playing around with a logging library. Created a log wrapper to standardize log output inside the app.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/503b1da2988cee6ccb3b42e0256b9431196bac67)
### Day 20: October 1

Created HTTP middleware handler for loggin. Need to learn more about organizing and using HTTP handlers in Go. Think that I'm doing something wrong.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/b6132283be924a841e04e608e3ae2d6a8a9ea375)
### Day 21: October 2

Figured out how to disable logging in unit tests without stubs. Added logging for internal server errors and fatal errors. Added more unit tests to increase test coverage (my aim is more than 90%). Need to learn about reusing test helpers.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/d00498b961d2de0e15a0c59f9ef59de06947ce68)
