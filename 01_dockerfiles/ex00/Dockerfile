FROM alpine

RUN apk update && \
	apk upgrade && \
	apk add vim

ENTRYPOINT [ "vim" ]

#build it
#docker build --tag ex00 ./

#run it
#docker run --interactive ex00