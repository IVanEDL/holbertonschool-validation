build:	##- Generate the website from the markdown and configuration files in the directory dist/
	@hugo
	@go build -o awesome-api

run:	##- Run the application in background by executing the binary awesome-api
	@./awesome-api >./awesome-api.log 2>&1 &

post:	##- Create a new blog post whose filename and title come from the environment variables POST_TITLE and POST_NAME.
	@hugo new posts/$(POST_NAME).md
	@echo "---\
	title: '$(POST_TITLE)'\
	date: $(date +"%Y-%m-%dT%H:%M:%S%z")\
	---" > content/posts/$(POST_NAME).md

stop:	##- Stop the application with the command kill XXXXX where XXXXX is the Process ID of the application.
	@kill "$(pgrep awesome-api)"

clean:	##- Stop the application. Delete the binary awesome-api and the log file awesome-api.log
	@kill "$(pgrep awesome-api)"
	@rm -rf awesome-api.log awesome-api

test:	##- Tests it so it becames clear if it works
	@curl http://localhost:9999
	@curl http://localhost:9999/health

help:	##- Displays this messages
	@sed -e '/#\{2\}-/!d; s/\\$$//; s/:[^#\t]*/:/; s/#\{2\}- *//' $(MAKEFILE_LIST)

