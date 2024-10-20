# IBM GraphQL Workshop

## Use and build GraphQL APIs with ease
<p align="center">
<img src="https://d7umqicpi7263.cloudfront.net/img/product/404ac0a4-b577-41f3-94cb-8440d23f414b.png" width="300">
</p>

Welcome! In this workshop, you'll learn how to use and create GraphQL APIs based on the most popular data sources (REST, MySQL, Postgres, GraphQL) and how to manage and share those APIs using [IBM API Connect](https://www.ibm.com/products/api-connect?utm_content=SRCWW&p1=Search&p4=43700074867184569&p5=p&p9=58700008241632940&gad_source=1&gclid=EAIaIQobChMIytGqp5aCiQMVBJCDBx3juy2BEAAYASAAEgKVoPD_BwE&gclsrc=aw.ds).

## Part 1 - Using GraphQL APIs

### Getting Started:

Go to the [API Connect Essentials Explorer](https://dashboard.ibm.stepzen.com/explorer?endpoint=https%3A%2F%2Fswapi-graphql.netlify.app%2F.netlify%2Ffunctions%2Findex). Using the dashboard, you should be able to navigate a GraphQL API that contains a lot of information about the original Star Wars movies (e.g. about the characters, planets and starships). To make sure the API works, paste the following query into the Explorer:

```graphql
query {
  allFilms {
    films {
      title
    }
  }
}
```

As a result, all of the movie titles should be displayed. It should look like this:

```graphql
{
  "data": {
    "allFilms": {
      "films": [
        {
          "title": "A New Hope"
        },
        {
          "title": "The Empire Strikes Back"
        },
        {
          "title": "Return of the Jedi"
        },
        {
          "title": "The Phantom Menace"
        },
        {
          "title": "Attack of the Clones"
        },
        {
          "title": "Revenge of the Sith"
        }
      ]
    }
  }
}
```

Feel free to try other queries if you want to!

### Assignments

1. From the first two movies ("A New Hope" & "The Empire Strikes Back"), select all the characters and the character's corresponding id. Hint: Use the "first:" argument in your query.

    <details>
    <summary>Your result should look like this:</summary>

    ```graphql
        {
          "data": {
            "allFilms": {
              "films": [
                {
                  "title": "A New Hope",
                  "characterConnection": {
                    "characters": [
                      {
                        "id": "cGVvcGxlOjE=",
                        "name": "Luke Skywalker"
                      },
                      {
                        "id": "cGVvcGxlOjI=",
                        "name": "C-3PO"
                      },
                      {
                        "id": "cGVvcGxlOjM=",
                        "name": "R2-D2"
                      },
                      {
                        "id": "cGVvcGxlOjQ=",
                        "name": "Darth Vader"
                      },
                      {
                        "id": "cGVvcGxlOjU=",
                        "name": "Leia Organa"
                      },
                      {
                        "id": "cGVvcGxlOjY=",
                        "name": "Owen Lars"
                      },
                      {
                        "id": "cGVvcGxlOjc=",
                        "name": "Beru Whitesun lars"
                      },
                      {
                        "id": "cGVvcGxlOjg=",
                        "name": "R5-D4"
                      },
                      {
                        "id": "cGVvcGxlOjk=",
                        "name": "Biggs Darklighter"
                      },
                      {
                        "id": "cGVvcGxlOjEw",
                        "name": "Obi-Wan Kenobi"
                      },
                      {
                        "id": "cGVvcGxlOjEy",
                        "name": "Wilhuff Tarkin"
                      },
                      {
                        "id": "cGVvcGxlOjEz",
                        "name": "Chewbacca"
                      },
                      {
                        "id": "cGVvcGxlOjE0",
                        "name": "Han Solo"
                      },
                      {
                        "id": "cGVvcGxlOjE1",
                        "name": "Greedo"
                      },
                      {
                        "id": "cGVvcGxlOjE2",
                        "name": "Jabba Desilijic Tiure"
                      },
                      {
                        "id": "cGVvcGxlOjE4",
                        "name": "Wedge Antilles"
                      },
                      {
                        "id": "cGVvcGxlOjE5",
                        "name": "Jek Tono Porkins"
                      },
                      {
                        "id": "cGVvcGxlOjgx",
                        "name": "Raymus Antilles"
                      }
                    ]
                  }
                },
                {
                  "title": "The Empire Strikes Back",
                  "characterConnection": {
                    "characters": [
                      {
                        "id": "cGVvcGxlOjE=",
                        "name": "Luke Skywalker"
                      },
                      {
                        "id": "cGVvcGxlOjI=",
                        "name": "C-3PO"
                      },
                      {
                        "id": "cGVvcGxlOjM=",
                        "name": "R2-D2"
                      },
                      {
                        "id": "cGVvcGxlOjQ=",
                        "name": "Darth Vader"
                      },
                      {
                        "id": "cGVvcGxlOjU=",
                        "name": "Leia Organa"
                      },
                      {
                        "id": "cGVvcGxlOjEw",
                        "name": "Obi-Wan Kenobi"
                      },
                      {
                        "id": "cGVvcGxlOjEz",
                        "name": "Chewbacca"
                      },
                      {
                        "id": "cGVvcGxlOjE0",
                        "name": "Han Solo"
                      },
                      {
                        "id": "cGVvcGxlOjE4",
                        "name": "Wedge Antilles"
                      },
                      {
                        "id": "cGVvcGxlOjIw",
                        "name": "Yoda"
                      },
                      {
                        "id": "cGVvcGxlOjIx",
                        "name": "Palpatine"
                      },
                      {
                        "id": "cGVvcGxlOjIy",
                        "name": "Boba Fett"
                      },
                      {
                        "id": "cGVvcGxlOjIz",
                        "name": "IG-88"
                      },
                      {
                        "id": "cGVvcGxlOjI0",
                        "name": "Bossk"
                      },
                      {
                        "id": "cGVvcGxlOjI1",
                        "name": "Lando Calrissian"
                      },
                      {
                        "id": "cGVvcGxlOjI2",
                        "name": "Lobot"
                      }
                    ]
                  }
                }
              ]
            }
          }
        }
    ```
    </details>
    
    <details>
    <summary>Solution:</summary>

    ```graphql
        query {
          allFilms(first: 2) {
            films {
              title
              characterConnection {
                characters {
                  id
                  name
                }
              }
            }
          }
        }
    ```
    </details>
    
2. Copy the id of your favorite character. Use the id to get the name, birth year, gender as well as the name and population of it's home planet.


    <details>
    <summary>Your result should look like this:</summary>

    ```graphql
        {
          "data": {
            "person": {
              "name": "Luke Skywalker",
              "birthYear": "19BBY",
              "gender": "male",
              "homeworld": {
                "name": "Tatooine",
                "population": 200000
              }
            }
          }
        }
    ```
    </details>
    
    
    
    <details>
    <summary>Solution:</summary>

    ```graphql
        query {
          person(id: "cGVvcGxlOjE=") {
            name
            birthYear
            gender
            homeworld {
              name
              population
            }
          }
        }
    ```
    </details>
    
    
3. Get a list of all the characters which have piloted the Millennium Falcon.


    <details>
    <summary>Your result should look like this:</summary>

    ```graphql
        {
          "data": {
            "starship": {
              "name": "Millennium Falcon",
              "pilotConnection": {
                "pilots": [
                  {
                    "name": "Chewbacca"
                  },
                  {
                    "name": "Han Solo"
                  },
                  {
                    "name": "Lando Calrissian"
                  },
                  {
                    "name": "Nien Nunb"
                  }
                ]
              }
            }
          }
        }
    ```
    </details>
    
    
    
    <details>
    <summary>Solution:</summary>
    Get the starship id of the Millennium Falcon first:
  

    ```graphql
        query {
          allStarships {
            starships {
              id
              name
            }
          }
        }
    ```
  
  
    Then, use the id to get a list of all pilots:
    ```graphql
        query {
          starship(id: "c3RhcnNoaXBzOjEw") {
            name
            pilotConnection {
              pilots {
                name
              }
            }
          }
        }
    ```
    </details>
    
    
4. Get the average height of the Wookie species. Also, get the names of the members of this species as well as their height.<br>Hint: the id of the wookie species is ```c3BlY2llczoz```.


    <details>
    <summary>Your result should look like this:</summary>

    ```graphql
        {
          "data": {
            "species": {
              "averageHeight": 210,
              "personConnection": {
                "people": [
                  {
                    "name": "Chewbacca",
                    "height": 228
                  },
                  {
                    "name": "Tarfful",
                    "height": 234
                  }
                ]
              }
            }
          }
        }
    ```
    </details>
    
    
    
    <details>
    <summary>Solution:</summary>

    ```graphql
        query {
          species(id: "c3BlY2llczoz") {
            averageHeight
            personConnection {
              people {
                name
                height
              }
            }
          }
        }
    ```
    </details>
 
 
4. Send a query of your choice to the GraphQL server using curl or a programming language of your choice.<br>Hint: Clicking on "Export" in the menu on the top will give you some code snippets to make this task easier.

## Part 2 - Creating GraphQL APIs

### Getting Started:

You need to install the [StepZen CLI](https://www.npmjs.com/package/stepzen), for which you need Node.js and NPM installed (https://docs.npmjs.com/downloading-and-installing-node-js-and-npm).

After installing the CLI, you need to create a _free_ account [here](https://dashboard.ibm.stepzen.com/) (no credit card required).

### Assignments

1. Log in to your [IBM API Connect Essentials Instance](https://dashboard.ibm.stepzen.com/). Then, select "Getting started" and "Try an example project". You can now create GraphQL APIs using various data sources as a backend, try to connect some of them. You will be led through the various commands which you will need to execute in your local CLI to create and deploy the endpoint. Note that by using the introspection service ("stepzen import"), a schema for data sources like databases, REST endpoints or GraphQL endpoints will automatically be generated without having to explicitly specify it.

    Afterwards, you can test the APIs you created by selecting "Explorer" in the menu on the left. On the top, you can now select your endpoint and specify which data you want to request from it using the Schema on the left (to make this easier, you can select the "Builder" item on the top if it is not yet selected). The Explorer will then automatically create the needed Query. By clicking on the symbol which looks like a Play button, the Query will be executed and the result will be shown on the right.

2. Leave your current directory and create/enter a new one. Clone this GitHub repository using ```git clone https://github.com/benediktaugenstein/graphql-workshop``` or download it as a zip file. After that, switch to the git repository using ```cd graphql-workshop``` and deploy the endpoint defined in this repository. You can deploy it by running ```stepzen start```, which does the same as ```stepzen deploy``` but monitors your local directory for changes and automatically deploys them to the endpoint.

3. Check the connection to your data source by running the query to get a list of books and their names.

    <details>
    <summary>Solution:</summary>

    ```graphql
    query {
      books {
        name
      }
    }
    ```

    </details>
    

4. With StepZen, you can use custom directives, like `@materializer`, to combine data retrieved by different queries. The schema for your selected data sources has queries to get `authors` and `books`, which return the types `Author` and `Book`. Connect the field `authorID` on type `Book` using the `@materializer` directive so that you can query the GraphQL API with the following operation:

    ```graphql
    query {
      book(id: 1) {
        name
        author {
          name
        }
      }
    }
    ```

    This query should return the book with `id` equal to `1`, including its author ("Agatha Christie").

    <details>
    <summary>Solution:</summary>

    Add the `author` field to type `Book` in the GraphQL schema in the `rest` directory. The `@materializer` will be configured to use the `author` query when the `books` query requests the `author` field. If so, it will take the field `authorID` and pass it to the `author` query as an argument.

    ```graphql
    ## ../rest/books.graphql

    type Book {
      id: ID!
      name: String!
      originalPublishingDate: Date!
      authorID: ID!
      author: Author
        @materializer(
          query: "author"
          arguments: [{ name: "id", field: "authorID" }]
        )
      isbn: String
    }
    ```

    </details>

4.  Let's connect another data source to the data you've explored in the first questions. We can enrich the data from our existing data source with data from a third party, like [Google Books](https://developers.google.com/books/docs/v1/using). The Google Books API is a REST API that returns meta-data about almost every book. You can send a request to the following endpoint to get data for a book with the ISBN 9781407021102: [https://www.googleapis.com/books/v1/volumes?q=9788726586343&country=US](https://www.googleapis.com/books/v1/volumes?q=9781407021102&country=US).

    This request can also be added as a query to your GraphQL API. This directive will change the response of the REST API into a GraphQL response. All nested relationships in the returned JSON by the REST API are respected. Therefore you can use the directive `@rest` to connect a REST data source to a new file. You need to create a new `.graphql` file to make this connection, and make sure to add it to `index.graphql` as well.

    After connecting the endpoint, you should be able to use the following query to retrieve a title, thumbnail, and description for a book based on the ISBN:

    ```graphql
    query {
      googleBooks(isbn: "9788726586343") {
        items {
          volumeInfo {
            title
            description
            imageLinks {
              thumbnail
            }
          }
        }
      }
    }
    ```

    Tip: Open the Google Books API response in [this online tool](https://transform.tools/json-to-graphql) to automatically create GraphQL type definitions for the response of the Google Books API. Look at the directory `./rest` in this project to see more examples of how the `@rest` directive should be configured.

    <details>
    <summary>Solution:</summary>

    Create a new file (in the root directory) called `googleBooks.graphql`. In this file, you need to add a query to get the results from the Google Books API, and you need to define the return types of the data. The response of this API is heavily nested, so you need to create multiple types to define all the fields that you want to be returned by this new query.

    ```graphql
    ## googleBooks.graphql

    type ImageLinks {
      thumbnail: String
    }

    type VolumeInfo {
      title: String
      description: String
      imageLinks: ImageLinks
    }

    type GoogleBook {
      id: ID!
      volumeInfo: VolumeInfo
    }

    type GoogleBookResult {
      items: [GoogleBook]
    }

    type Query {
      googleBooks(isbn: String!): GoogleBookResult
        @rest(
          endpoint: "https://www.googleapis.com/books/v1/volumes?q=isbn:$isbn&country=US"
        )
    }
    ```

    </details>

5.  The query's response that gets the book information from the Google Books API with GraphQL is a bit hard to read. Let's refactor the GraphQL schema for this API to flatten the response. After the refactor, you should be able to use the following query on the GraphQL API:

    ```graphql
    query {
      googleBooks(isbn: "9788726586343") {
        title
        description
        thumbnail
      }
    }
    ```

    You can use the helpers `resultroot` and `setters` that are available on the `@rest` directive for this.

    Tip: You can append `[]` to the field for `resultroot` to use a field that is returning an array.

    <details>
    <summary>Solution:</summary>

    The helper `resultroot` will take the field `volumeInfo` for every iteration of the `items` array. That way, all the fields in `volumeInfo` become top-level fields for this query. With `setters` the information for the field `thumbnail` inside the `imageLinks` path can be flattened.

    ```graphql
    ## googleBooks.graphql

    type GoogleBook {
      title: String
      description: String
      thumbnail: String
    }

    type Query {
      googleBooks(isbn: String!): [GoogleBook]
        @rest(
          endpoint: "https://www.googleapis.com/books/v1/volumes?q=isbn:$isbn&country=US"
          resultroot: "items[].volumeInfo"
          setters: [{ field: "thumbnail", path: "imageLinks.thumbnail" }]
        )
    }
    ```

    </details>

6.  With the Google Books API added to the GraphQL API; the next step will be to connect the information from the `books` and `googleBooks` queries. The `Book` type returned from the prepopulated data source has a field called `isbn` which can be used to find meta-data for this book using the Google Books API. Combining types using queries can be done in two ways: with the `@materializer` directive that you used in question 3 or with the directive `@sequence` that lets you chain the results of multiple queries. Use this `@sequence` directive to add the following query to your schema:

    ```graphql
    query {
      getBooks {
        name
        description
        thumbnail
        isbn
      }
    }
    ```

    This new query called `getBooks` gets the fields `name` and `isbn` from the query `books`, and the fields `description` and `thumbnail` from `googleBooks`. The result comes from both the prepopulated data source and the Google Books API. You can create this query in a new file (in example) called `collections.graphql` or in any of the `.graphql` files you worked in before.

    Tip: `@sequence` only returns the response of the last query in the sequence. Therefore the directive `@collect` needs to be used to collect the responses from all the queries that are listed in the sequence. You need to create a new type that will be the response type of the collection and the `getBooks` query.

    <details>
    <summary>Solution:</summary>

    The directive `@sequence` needs to call the query `books` first, followed by `googleBooks`. The query `books` returns a field called `isbn` which is also the name of the argument that is needed by the `googleBooks` query. This value will automatically be passed to this query. The `collect` query uses the `@collect` directive to get the fields `name` and `description` from the `books` query, and the fields `description` and `thumbnail` from the `googleBooks` query. The response type of the `collect` query is the same as for the `getBooks` query but singular as the results for every response is collected individually.

    ```graphql
    ## collections.graphql

    type BookResult {
      name: String
      description: String
      thumbnail: String
      isbn: String
    }

    type Query {
      collect(
        name: String
        description: String
        isbn: String
        thumbnail: String
      ): BookResult @connector(type: "echo")
      getBooks: [BookResult]
        @sequence(
          steps: [
            { query: "books" }
            { query: "googleBooks" }
            { query: "collect" }
          ]
        )
    }
    ```

    </details>
    
    
## Part 3 - Manage your API

In this part, you will use an API Management solution to administer the complete lifecycle of your API. Using such a tool, you can easily create, manage, secure, socialize and monetize APIs. 

1. Go to the following link and sign in as either user1 or user3 and the password "passw0rd" using the "API Manager user registry":
  https://small-mgmt-api-manager-integration.apps.670915d2dd88d89307362840.ocp.techzone.ibm.com/manager/

2. Click on "Develop APIs and products". Click "Add"->"API" to create a new API. Import your newly created API as a GraphQL proxy by providing the needed information. Leave the configurations as they are except for "Secure using Cliend ID", which you can unselect.

3. When the API has been created, go back to "Develop APIs and products". You will see your API being listed under "APIs". By clicking on the three dots, you can manage various aspects of your API. Click on "publish" and follow the various steps to share your API in a portal, making it available in your enterprise. 

4. Go to your developer portal. The specific url depends on which user you have chosen (replace <user_number> with the number of your user):
  https://small-ptl-portal-web-integration.apps.670915d2dd88d89307362840.ocp.techzone.ibm.com/org-<user_number>/sandbox/product
  Sign in by using your user and the password "passw0rd1!,f". Your product should be displayed in the portal. Within the portal, developers can browse, explore, test and subscribe to API products like the product you have created. If you want to, you can further edit your API and product, adding more detailed information which will be displayed in the portal, facilitating the usage of your products/APIs.


### Support

If you have further questions after the workshop is over or would like to conduct a follow-up, please feel free to contact us:

benedikt.augenstein@ibm.com <br>
michael.hamann@de.ibm.com
