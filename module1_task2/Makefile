build:	##Generate the website from the markdown and configuration files in the directory dist/
	@hugo

clean:	##Cleanup the content of the directory dist/
	@rm -rf dist

post:	##Create a new blog post whose filename and title come from the environment variables POST_TITLE and POST_NAME.
	@hugo new posts/$(POST_NAME).md
	@echo "---\
	title: '$(POST_TITLE)'\
	date: $(date +"%Y-%m-%dT%H:%M:%S%z")\
	---" > content/posts/$(POST_NAME).md

help:	##Displays this messages
	@printf "\nusage : make <commands> \n\nthe following commands are available : \n\n"
	@cat Makefile | awk '1;/help:/{exit}' | awk '/##/ { print; getline; print; }' | awk '{ getline x; print x; }1' | awk '{ key=$$0; getline; print key "\t\t\t\t " $$0;}'
	@printf "\n"

