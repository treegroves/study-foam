Navigating larger code bases

Start by drawing a picture of the code base
 - Ask yourself what all the files do

- index:
	- launches express
	- boot file
	- execution code - test manually 

### Express Code
- server.js(express code):
	- add middleware
	- configure server
	- plumbing
	- automated testing 

- routes.js(express code):
	- configure routes
	- control flow 
	- user input in
	- user output = rendering
	- templates 


### Database Code
- db.js(database code):


Testing Routes which use databases

### Unit testing:
Isolate a function from dependencies and test just it
Mock out route and test it in isolation
don't use real function, use fake function

### integration testing:
Testing a large piece of the system , with no mocking


use jest.mock('./db) to convert actual functions into mock functions for testing
why you put functions in seperate file from route


socially-related thing that

ministry for disabled people
