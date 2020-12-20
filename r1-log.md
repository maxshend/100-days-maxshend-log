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
### Day 22: October 3

Learning how to implement JWT role-based authorization. Bug fixing.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/787381356c7020fc473bdeb6e381f1ba67b7653d)
### Day 23: October 4

Learned that env variables isn't set in unit tests until you specify them in the command. Fixed the bug related to this behaviour.
Created a package for test helpers.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/2ad92372b20cd2225273095fa5c239410692eafb)

[Link to work](https://github.com/maxshend/tiny-goauth/commit/7ef528447cb10ad1df1ccb70e01cc893364050ff)
### Day 24: October 5

Added roles data to JWT payload. Learned about ARRAY_AGG function in PostgreSQL.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/fd789bdbe82f3947545a475f8f5e1f704317bda9)
### Day 25: October 6

Learning about different ways to encode/decode JSON in Go. Created constant errors instead of simple variables containing `errors.New` to make errors more reusable and immutable.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/37cf14391c6265b7a8ecea3646dec91e4fb7e193)
### Day 26: October 7

Learning best practices of handling errors in Go. Added handlers helpers for sending responses. Need to refactor deps.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/89de33d85c558b3d49bf1774ee757dd65d481fe9)
### Day 27: October 8

Learned how to get details about test coverage using Go tools. Added more unit tests.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/6e345545f7a6fd3b121d9013d1fd7a3b3000e70e)
### Day 28: October 9

Started JavaScript30 course. Finished first lesson.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/7ce124ae306b8ca70f36bfbe02e71c319b3c4d5a)
### Day 29: October 10

Finished second challenge of JavaScript30.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/cc1d306ebd98f46cc88089fe55eb3d05732a7f2d)
### Day 30: October 11

Decided to change JWT signing method from HMAC to RSA.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/00bbcd1f9522407b1987a326e5f642cead2b3b48)
### Day 31: October 12

Fixing errors in unit tests that caused by the changed JWT signing method. Finished 3rd challenge of JS30. Learned about CSS custom properties (variables).

[Link to work](https://github.com/maxshend/myJavaScript30/commit/885529bbf28e731177c0477fd300a1b8e3350f3c)
### Day 32: October 13

Adapted unit tests to changed JWT signing method. Finished 4th challenge of JS30. Recapped JS array functions and their syntax.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/8d66d87c54c4eff152f6ae2dbd66f36ca356d41d)

[Link to work](https://github.com/maxshend/myJavaScript30/commit/9fd1a24aad685f81ae3bc8bced09f82a9e503a0f)
### Day 33: October 14

Learning about CSS Flexbox. Finished 5th challenge of JS30.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/346ef797286e4c644c2927a87f30f1c5036a7af6)
### Day 34: October 15

Learned about mocking in Go using interfaces. Started implementation of a ruby gem that will be used for integration with my auth service in ruby apps.

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/57ec3fecfe97870d410facab6bc14fcb0a6fdb26)
### Day 35: October 16

Finished 6th challenge of JS30.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/eae652e926c03ce9037daf51e84fd4829579ec55)
### Day 36: October 17

Started implementation of migrations/models generator for the gem, that will be used in Rails apps.

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/41bc331495d0e55d34026299947689437783f2bf)
### Day 37: October 18

Add a model generation and customizable model name to the gem. Finished 7th challenge of JS30.

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/8a353fff6955a19cdd38a87c33b2e7146ce638fd)

[Link to work](https://github.com/maxshend/myJavaScript30/commit/6ee31da4904d2b9b3a42453f93f6a87c94498f98)
### Day 38: October 19

Finished 8th challenge of JS30. Learned basics of HTML5 Canvas.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/61f0f5a86e1a797175623cace32231d52935d779)
### Day 39: October 20

Implemented ability to insert content to existing models when model file already exists, to create a different migration file based on existing models and migrations files.

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/77bb2a1c485f0c262cdbf4bbbc7cff3e1b4de9aa)
### Day 40: October 21

Added routes configurations, so new routes could be added to a Rails app from the gem. Finished 9th challenge of JS30.

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/f63247602fa2f357cb1dcafb7f14360e2afc5a44)

[Link to work](https://github.com/maxshend/myJavaScript30/commit/316b168f512d631a20e4f11fa4e211dea6e26b60)
### Day 41: October 22

Created base for users creation in the app from the auth service using the gem.

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/f51a432c008459770afbaa927f2e8a6e966632c4)
### Day 42: October 23

Created a JSON API method that creates user records in a Rails app from the auth service.

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/0e1a439a008d24097465d3c3775494f4380df7cd)
### Day 43: October 24

Finished 10th challenge of JS30.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/8cbf7cc6e2ef7150747f639509d5cc5a4707b480)
### Day 44: October 25

Started to implement creation of an external user record using JSON API of a Rails app (that uses the gem).

[Link to work](https://github.com/maxshend/tiny-goauth/commit/025019b902b44c0029e8fbd167398f3cc2b9401f)
### Day 45: October 26

Finished 11th challenge of JS30.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/aa54aad6ff5217ff1a6a8718c3591bf7d276ab03)
### Day 46: October 27

Allow additional payload in sign up requests. Finished 12th challenge of JS30.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/b81a868b89bfda026ee6505c73c11484d75bf77d)

[Link to work](https://github.com/maxshend/myJavaScript30/commit/ef5d3b6da8afa01294da9b808443b5f2118a926c)
### Day 47: October 28

Added the auth interactor to the list of generated files by the gem generator.

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/cca802d59abcefc8f361043501e798edb9797614)
### Day 48: October 29

Finished 13th challenge of JS30.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/599a2b917c2955397b39abdb29f15f55807549d4)
### Day 49: October 30

Learning about testing Rails engines and generators. Set up the gem project for testing.

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/4b0c5fece727d217cb99b987f5956cbc9fe4205d)
### Day 50: October 31

Finished 14th challenge of JS30.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/c652eeb07a2270c3332bb0a2d7e32fb7818e5937)
### Day 51: November 1

Writing specs for Rails generators.
### Day 52: November 2

Finished 15th challenge of JS30.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/746be2cde63d6270ba63311ffe3c7a3a9a256d04)
### Day 53: November 3

Finished 16th challenge of JS30.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/d3a9a4e00747a6ff8938cee5789f53bbf6dd0be2)
### Day 54: November 4

Added specs for generated by the gem set of files (for cases without existing user model). Figured out how to create a dummy Rails app for testing purposes without need to create a full Rails app.

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/9d4e3e8a013c0fe58d018facdf7940c7516486ac)
### Day 55: November 5

Added specs to the gem for cases when user model already exists. Created test helpers to supress stdout (to hide output from Rails generators) and get a file content.

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/d3c3b99697f362acc97f394359f3a5d211e6d917)
### Day 56: November 6

Finished 17th challenge of JS30.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/860aa5d8968677896c3cbb618e6e0a5500dd84cd)
### Day 57: November 7

Adding JWT validation to the gem so there will be ability in an app to create requests with authentication.

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/3082c58ac6359bba5eb3c0b676a1889006e39c4a)
### Day 58: November 8

Finished 18th challenge of JS30.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/587632e2b677a289de54963367a84c2a72d444be)
### Day 59: November 9

Added the initializer generation to the gem. Added a locales file. Fixed check_token errors.

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/2b816b5f00a0f353c7aa3299e8d6bda1a7b4c5b5)
### Day 60: November 10

Added dynamic name for the method that returns an authenticated resource, so an app that uses the gem won't be restricted to "User" model only.

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/5d93a26d711e672e8c98fa184b514188ab4ccfeb)

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/b1d43f4d2356c38158096fadff9c47b5c9de0b10)
### Day 61: November 11

Finished 19th challenge of JS30.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/629baaa0a1ee00d5614e47189f87f419cd405d2d)
### Day 62: November 12

Gem: Added model name to the initializer. Fixed controllers authentication concern (used incorrect method). Added method to get user roles.
Auth: Fixed bug in the email login handler that were caused by the empty roles array from the db.

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/edc845e43af66722c79f1c112a7e39e6a89adf75)

[Link to work](https://github.com/maxshend/tiny-goauth/commit/5534eba56b837ccd8ef5c047070ec0f6f3861734)
### Day 63: November 13

Finished 20th challenge of JS30. Learned basics of Web Speech API.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/2918c8fc4326b6da0e58b481fb60a4e860b071c9)
### Day 64: November 14

Figured out how to stub external requests in auto tests using httptest Go package.
Finished 21th challenge of JS30.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/98e76998ad1240e4587ba832cdf9a46c1bdba81f)

[Link to work](https://github.com/maxshend/myJavaScript30/commit/36f4e63323fd3b36ff2e0676dd1cc0bbd944bd72)
### Day 65: November 15

Finished 22th challenge of JS30. Learned about moveable link highlighter and scroll compensation.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/541408b4916d8f5b1da6a3b54ae0d616d47274b4)
### Day 66: November 16

Finished 23th challenge of JS30. Learned basics of SpeechSynthesisUtterance interface.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/8270c481f6a9d1e93b5e7bebeccdcc0b070e1bcf)
### Day 67: November 17

Created a new Rails project for the business logic API of the "Loyalty Area" application that will be used for testing the auth service and finding problems and possible improvements.

[Link to work](https://github.com/maxshend/loyalty-area/commit/0dfac03cde7f6d379e67d797c44d044cb4a3a3d3)
### Day 68: November 18

Finished 24-25th challenges of JS30.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/39c803195b411061010b4bc57c71ead8ecd0e2d4)

[Link to work](https://github.com/maxshend/myJavaScript30/commit/4f9808b24ef2ec148e6d5e9a033dc00ea039a9a5)
### Day 69: November 19

Created User model in the app. Added gem generator's attributes to the generated interactor class that responsible for creating new users.

[Link to work](https://github.com/maxshend/loyalty-area/commit/f55926b0f7a7a655c8c98f5e863be0999d1790bb)

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/45f1e6fbebabca9bc6e9fad9735b356ccd48f597)
### Day 70: November 20

Finished 26th challenge of JS30.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/404b484cfba3a95aedd06c59bc33fe4d75d65e98)
### Day 71: November 21

Dockerized the development environment of the Rails API app.

[Link to work](https://github.com/maxshend/loyalty-area/commit/6ff111b940776368fba1ed8e0a3b96b4e43cf103)
### Day 72: November 22

Finished 27-28th challenges of JS30.

[Link to work](https://github.com/maxshend/myJavaScript30/commit/f903cdb4299d6014676814d42fda335374427ae8)
### Day 73: November 23

Finished 29-30th challenges of JS30. Done!

[Link to work](https://github.com/maxshend/myJavaScript30/commit/ac333bdd05869a078b6324af91d96828286c7c52)

[Link to work](https://github.com/maxshend/myJavaScript30/commit/e9edbbfe4faea870c8c646ed7137d29f727ce1f4)
### Day 74: November 24

Fixed database cleaner Safeguard Error. Changed bundler installation in the Dockerfile. Figuring out how to connect all needed services with docker compose.

[Link to work](https://github.com/maxshend/loyalty-area/commit/c2c24b48df272c40eba7bd8e553e67318467a124)
### Day 75: November 25

Added auth service to the docker compose. Configuring multiapp dev environment with docker compose.

[Link to work](https://github.com/maxshend/loyalty-area/commit/0536ee959db9ce61bc8de5f7084cdc75d8c56a11)
### Day 76: November 26

Added an option to the auth service to run database migrations on start. Created a function that runs sql code from files in migrations directory.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/7f27e9737cd19e5f1f9d90ad3a5f9aa69d6a4380)
### Day 77: November 27

Fixed bug in the auth service that were caused by the uncopied migrations files to the final docker image.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/7956306ea03d3035eddf2e55954cb4119e98540f)
### Day 78: November 28

Fixed problems with interaction of the Rails app and Auth service. Figured out that db hostnames with underscores in Rails are not handled correctly.

[Link to work](https://github.com/maxshend/loyalty-area/commit/8127c829a22e64db7ef519544e165101002d5bae)
### Day 79: November 29

Improving handling of business logic apps HTTP errors in the auth service.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/a3b33030829680926f355160019b2c0291c1476c)
### Day 80: November 30

Unwrap "payload" params from the auth service before passing to the API app interactor that creates a user.
Created an HTTP request handler in the auth service to remove users records from the db.

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/f394a5c5ca18802fab85aa106cd281b030b782db)

[Link to work](https://github.com/maxshend/tiny-goauth/commit/042817f6171ccd1aa2452aea18f1773c9c25b762)
### Day 81: December 1

Added unit tests for DeleteUser HTTP handler.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/70724df98617bdf954c4c8e72e0d019a23b57ed8)
### Day 82: December 2

Adding roles to the user registration process of the auth service.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/1181525ffe4e5848de744ae37e9e45e42ef1e2be)
### Day 83: December 3

Created a custom validation for User roles.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/6e9f1134ecab4599dbe1064d704c70f9aa66e2bc)
### Day 84: December 4

Combined user roles records creation requests into a batch DB request. Add internal HTTP request to create roles.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/4abd6ab4b8b455e38ffbd460b88af173c0af201e)

[Link to work](https://github.com/maxshend/tiny-goauth/commit/f00e6aa2f3c4a94fbd5142172168bbd18e84262c)
### Day 85: December 5

Added to the gem a generator to fill available roles in the auth service.

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/40ef06efacc0213ded668d84a504135f04c91c2a)
### Day 86: December 6

Changed CreateRole handler to allow creating multiple roles with one request. Added an internal handler to delete a specified role. Created corresponding unit tests.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/17c66c3de5d9db9093b23763b0d1d1bed8cfa85d)
### Day 87: December 7

Modify DeleteRole HTTP handler to allow deleting multiple roles in one request.
Added to the gem ability to delete existing roles in the auth service using revoke behaviour of the corresponding generator.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/6a2a5b6c6668881410e32897d1da9f6b1f0b232e)

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/4e5e52bb14a1f2a5ebcdcf80158f478901d1ed92)
### Day 88: December 8

Fixed a bug with request params compability of the rails gem and the auth service.

[Link to work](https://github.com/maxshend/tiny_goauth-rails/commit/a340ca741c11fb4bfaa9b91b75db37ff3ebe0c7a)
### Day 89: December 9

Learning about gRPC and protobuf. Playing around with code examples. Small fixes in the auth service.

[Link to work](https://github.com/maxshend/tiny-goauth/commit/2eba52b770e76991c2397d98213f52f957c44ba6)
### Day 90: December 10

Created a new project for the email sender service that will be used in the auth service for sending confirmation emails. Going through a gRPC tutorial.

[Link to work](https://github.com/maxshend/tiny-gomail/commit/0292c9c7e49e4b774719b30057064eeaa6a91928)
### Day 91: December 11

Created .proto file that defines the data and interface of the mailer service. Generated client- and server-side code from this file.

[Link to work](https://github.com/maxshend/tiny-gomail/commit/bbfecc8bece585f56d2b1a81efb3e9e96f33d303)
### Day 92: December 12

Added to the mailer service method for sending text email messages using SMTP.

[Link to work](https://github.com/maxshend/tiny-gomail/commit/c4576129ce70609ffd60fcd34fe70b3ef1c8beee)
### Day 93: December 13

Added to the mailer service sending HTML email messages. Learning about a Quadtree data structure.

[Link to work](https://github.com/maxshend/tiny-gomail/commit/d8e192992fe28c20765609855ff66c63e6cc1b67)
### Day 94: December 14

Added code responsible for starting gRPC server of the mailer service. Added auto tests.

[Link to work](https://github.com/maxshend/tiny-gomail/commit/abacfb687501a77d4a15d9e1fffaf012784e3223)
### Day 95: December 15

Working on a Quadtree implementation in Go.

[Link to Work](https://github.com/maxshend/quadtree-go/commit/d4c7ea1a58ce408152730b954a5852244e1aac90)
### Day 96: December 16

Implemented Subdivide and Insert methods of a Quadtree. Added auto tests.

[Link to work](https://github.com/maxshend/quadtree-go/commit/6d92a03eb531b1e9dd2d9bf5c69c9379f53c9b26)
### Day 97: December 17

Added methods to query a Quadtree and to check whether two rectangular boundaries are intersect.

[Link to work](https://github.com/maxshend/quadtree-go/commit/7a00c1f70bc979fbad3da60f958271ebd8134935)
### Day 98: December 18

Fixed Subdivide method of a Quadtree. Increased test coverage.

[Link to work](https://github.com/maxshend/quadtree-go/commit/e89e99c72bea9329609f1c61ccac8978e76d0449)
### Day 99: December 19

Created Sender interface in the mailer service that will allow me to use different approaches to send emails and help me to write auto tests without sending real requests. Changed implementation of existing methods.

[Link to work](https://github.com/maxshend/tiny-gomail/commit/a12e91653a2df2880bb5fcb18fe50d9aa12f8712)
### Day 100: December 20

Added to the mailer service Sendgrid integration. Created log wrapper to log responses from senders services.

[Link to work](https://github.com/maxshend/tiny-gomail/commit/73318109437645ef5633d86e755a2418ba8f7973)

[Link to work](https://github.com/maxshend/tiny-gomail/commit/7a391a3de43cd321bd5a42431076d373571cf6bf)
