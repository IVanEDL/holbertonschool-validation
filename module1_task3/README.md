## Prerequisites:

1: A Valid Go-Hugo website is provided
2: There are no Git Submodules
3: The theme ananke is installed
4: No directory dist/ committed
5: Makefile present

## Lifecycle:

build: Generate the website from the markdown and configuration files in the directory dist/.
clean: Cleanup the content of the directory dist/
post: Create a new blog post whose filename and title come from the environment variables POST_TITLE and POST_NAME.
help: displays the help messages
