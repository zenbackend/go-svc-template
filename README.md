# service name 

Explain what service does 

## Dev Notes
The following steps are to be followed to run/test the service locally.
- Repository Setup:
    * After cloning the repository set these environment variables:
       
    * Get all the dependencies by using:
        ```
        go get -v -d ./...
        ```
  - To setup the DB:
      - Initialize docker container
        ```shell
          docker command to setup the db
        ```

      - Create Table in YSQL
        ```shell
         command to create table
        ```
      
      - Create the following environment variables and add them to a file called .local.env inside the configs directory:
          ```shell
          DB_HOST="localhost"
          DB_PORT="5433"
          DB_USER="yugabyte"
          DB_PASS="yugabyte"
          DB_NAME="dbname"
          DB_SSL="disable"
          DB_DIALECT=postgres
          ```
      
      * To run the migrations use:
         ```
         command to run the migrations
        ```

- To start the service:
     ```
    go run main.go
    ```

## Testing
- For test coverage:

    * To run tests execute command:
         ```
        go test `go list ./... ` -p 1 -v -coverprofile coverage.out -coverpkg=./...
        ```

    * To generate the coverage report, run the following command after running the above command:
         ```
        go tool cover -func coverage.out
        ```


