FROM golang:1.10.0

# Copy the local package files to the container's workspace.
ADD . /go/src/github.com/minhajuddinkhan/reviewzone/reviewer
WORKDIR /go/src/github.com/minhajuddinkhan/reviewzone/reviewer
# Build the outyet command inside the container.
# (You may fetch or manage dependencies here,
# either manually or with a tool like "godep".)
RUN go get
RUN go install github.com/minhajuddinkhan/reviewzone/reviewer/bin/reviewer


# Run the outyet command by default when the container starts.
#ENTRYPOINT /go/bin/reviewer

# Document that the service listens on port 8080.
EXPOSE 5000

CMD [ "go", "run", "/go/src/github.com/minhajuddinkhan/reviewzone/reviewer/bin/reviewer/main.go" ]