FROM golang:1.12.0-alpine3.9 As build
WORKDIR /app
COPY example.go /app
RUN cd /app && go build example.go

FROM scratch
COPY --from=build /app/example /app/
CMD [ "/app/example" ]