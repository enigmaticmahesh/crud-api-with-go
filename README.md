# CRUD with Golang

---

- `go mod init crud-with-go `
  - This will create a go module with the name as **go.mod** in the proejct folder
- `go get "github.com/gorilla/mux"`
  - We have used this **gorilla/mux** package to handle the routing in this application
  - We have installed the package using this command
  - We have 2 ways to install a package in command
    - `go get <package_name>`
    - `go install <package_name>`
  - But, the second one is deprecated and the first one is being used now. We can stil use the second one.
  - The only difference between them as far as I know is that **get** will check if the package is available, if not then it will download and then compile
  - Whereas **install** will directly compile, and will throw error if the package is not available
  - The **get** command will install the package in the **GO_HOME**
- It has 5 routes/endpoints for the following:
  - **/movies**: will provide list of all the movies(Request: **GET**)
  - **/movies**: will create a movie(Request: **POST**). The request body should have the following structure
    ```
    {
      "isbn": "1193453248",
      "title": "Baahubali 2",
      "director": {
        "firstname": "S.S.",
        "lastname": "Rajamouli"
      }
    }
    ```
  - **/movies/1**: will provide movie with **id = 1**(Request: **GET**)
  - **/movies/1**: will delete movie with **id = 1**(Request: **DELETE**)
  - **/movies/1**: will update movie with **id = 1**(Request: **PUT**). The request body should be same as that of the Create Request
