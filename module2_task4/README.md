## Prerequisites:

1: A Valid Go-Hugo website is provided
2: There are no Git Submodules
3: The theme ananke is installed
4: No directory dist/ committed
5: Makefile present

## Lifecycle:

build: Generate the website from the markdown and configuration files in the directory dist/.
post: Create a new blog post whose filename and title come from the environment variables POST_TITLE and POST_NAME.
run: Run the application in background by executing the binary awesome-api
stop: Stop the application with the command kill XXXXX where XXXXX is the Process ID of the application.
clean: Stop the application. Delete the binary awesome-api and the log file awesome-api.log
test: Tests it so it becames clear if it works
lint: should fail when the linter catches and error:
help: displays the help messages
unit-tests: Tests the golang
integration-tests: Test the golang integration