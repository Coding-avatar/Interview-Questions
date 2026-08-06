<h1 id="top">GraphQL Last Minute Questionnaire</h1>
<h2>List of Topics</h2>
<ol type="a">
    <li>
        <details open>
            <summary><h3>GraphQL Basics & Architecture</h3></summary>
            <ol>
                <li><a href="#q1">What is GraphQL and how does it differ from REST?</a></li>
                <li><a href="#q2">Explain the main components of the GraphQL architecture.</a></li>
                <li><a href="#q3">Can you describe the structure of a GraphQL query?</a></li>
                <li><a href="#q4">What are the core features of GraphQL?</a></li>
                <li><a href="#q5">What are the advantages of using GraphQL over other API query languages?</a></li>
                <li><a href="#q6">What problem does GraphQL solve for frontend teams?</a></li>
                <li><a href="#q7">When is REST simpler than GraphQL?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Schema, Types & Directives</h3></summary>
            <ol>
                <li><a href="#q8">What is a GraphQL schema and why is it important?</a></li>
                <li><a href="#q9">What is a GraphQL schema?</a></li>
                <li><a href="#q10">Explain the concept of fields in GraphQL.</a></li>
                <li><a href="#q11">How does GraphQL handle data types?</a></li>
                <li><a href="#q12">What are scalar types in GraphQL?</a></li>
                <li><a href="#q13">What are scalar, object, enum, and input types?</a></li>
                <li><a href="#q14">How do non-null fields and null bubbling work?</a></li>
                <li><a href="#q15">When would you use a custom scalar?</a></li>
                <li><a href="#q16">What is the difference between an interface and a union?</a></li>
                <li><a href="#q17">What are directives in GraphQL?</a></li>
                <li><a href="#q18">How do generated GraphQL types help and where can they hurt?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Queries, Mutations & Resolvers</h3></summary>
            <ol>
                <li><a href="#q19">In GraphQL, what are queries and mutations?</a></li>
                <li><a href="#q20">What is the difference between a query, mutation, and subscription?</a></li>
                <li><a href="#q21">Describe how you would fetch data with a GraphQL query.</a></li>
                <li><a href="#q22">Explain the role of resolvers in GraphQL.</a></li>
                <li><a href="#q23">What is a resolver?</a></li>
                <li><a href="#q24">How do you pass arguments to fields in GraphQL queries?</a></li>
                <li><a href="#q25">Why are variables preferred over string interpolation?</a></li>
                <li><a href="#q26">What are aliases and when would you use them?</a></li>
                <li><a href="#q27">What is a fragment in GraphQL and how are they used?</a></li>
                <li><a href="#q28">How do fragments help?</a></li>
                <li><a href="#q29">What should a mutation return?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Performance, Caching & Subscriptions</h3></summary>
            <ol>
                <li><a href="#q30">How does GraphQL handle caching?</a></li>
                <li><a href="#q31">How does GraphQL caching work on the client?</a></li>
                <li><a href="#q32">How would you handle optimistic UI after a mutation?</a></li>
                <li><a href="#q33">How do you paginate a GraphQL list?</a></li>
                <li><a href="#q34">What is the N+1 problem in GraphQL?</a></li>
                <li><a href="#q35">How do you protect a GraphQL API from expensive operations?</a></li>
                <li><a href="#q36">What are persisted or trusted documents?</a></li>
                <li><a href="#q37">How do subscriptions work and when should you avoid them?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Security, Error Handling & Workflow</h3></summary>
            <ol>
                <li><a href="#q38">How do GraphQL errors differ from REST errors?</a></li>
                <li><a href="#q39">How should auth work in GraphQL?</a></li>
                <li><a href="#q40">What is introspection and should it be disabled?</a></li>
                <li><a href="#q41">How do file uploads work with GraphQL?</a></li>
                <li><a href="#q42">How does GraphQL work over HTTP?</a></li>
                <li><a href="#q43">How do you version a GraphQL API?</a></li>
                <li><a href="#q44">How would you debug a slow GraphQL screen?</a></li>
                <li><a href="#q45">How would you migrate one REST screen to GraphQL?</a></li>
            </ol>
        </details>
    </li>
</ol>

<hr />
<h2>Answers Section</h2>

<!-- GraphQL Basics & Architecture -->
<h3 id="q1">1. What is GraphQL and how does it differ from REST?</h3>
<p><strong>Short Answer:</strong> GraphQL is a highly efficient data query and manipulation language paired with a server runtime. It's designed to optimize data fetching for clients by allowing them to specify the shape and structure of the data they need. In contrast, REST is an architectural style where clients interact with server endpoints (resources) using a standard set of HTTP methods.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

**GraphQL** is a highly efficient data query and manipulation language paired with a server runtime. It's designed to **optimize data fetching for clients** by allowing them to specify the shape and structure of the data they need.

In contrast, **REST** is an architectural style where clients interact with server endpoints (resources) using a standard set of HTTP methods.

<p><b>Key Benefits of GraphQL over REST:</b></p>

- **Efficiency**: GraphQL minimizes data over-fetching and under-fetching, ensuring that clients receive only the necessary data. In contrast, REST endpoints have fixed responses, potentially leading to data redundancy or under-supply.

- **Flexibility**: With GraphQL, clients can specify the exact shape of the data they need. This is beneficial for applications with varying data requirements. REST endpoints deliver a pre-defined data set in their responses.

- **Versioning & Documentation**: GraphQL obviates the need for versioning and keeps documentation centralized. In REST, version management and documentation are typically separate from the API, complicating the process.

- **Data Validation**: GraphQL servers validate and type-check incoming requests. In REST, this is typically the client's responsibility.

- **Network Efficiency**: GraphQL often makes fewer network calls when acquiring related resources, compared to REST, which could necessitate multiple requests for the same resources.

- **Tooling & Ecosystem**: Both approaches enjoy extensive tooling support, but GraphQL's real-time introspection, strong type system, and auto-generation of documentation sets it apart. Additionally, GraphQL clients can benefit from query caching strategies.

- **Cache Control**: REST APIs provide various caching strategies using standard HTTP mechanisms. **Apollo Federation** in GraphQL further refines these strategies, offering finer control over caching across federated services.

- **Performance Optimizations**: Both REST and GraphQL can employ mechanisms like request throttling, but GraphQL's ability to batch multiple data requests into a single query contributes to improved performance.

- **Response Compression**: For reducing data size, GraphQL can utilize techniques like query result compression, while REST APIs can use response compression.

- **Data Consistency**: In a reliable setup, both REST and GraphQL can provide data consistency. However, when using GraphQL with subscriptions, real-time updates can be more straightforward to implement.

<p><b>When to Use GraphQL or REST:</b></p>

- **GraphQL**: Ideal for applications with diverse or changing data requirements, dynamic UIs demanding real-time data, or microservice architectures. Also suitable when the client and server are developed and maintained by the same team, ensuring end-to-end compatibility.

- **REST**: Recommended when the application has straightforward data requirements, relies on well-established data models, or the client's front-end architecture implements one-to-one mapping with the server's resources.

<p><b>Code Example: Basic Schema and Resolver:</b></p>

Here is the GraphQL code:

```graphql
type Query {
  # Retrieves a list of all users
  allUsers: [User]
}

type User {
  id: ID!
  name: String!
  email: String!
}

# Example Query: Fetch all user names and emails
query {
  allUsers {
    name
    email
  }
}
```

Now, the equivalent REST endpoint for reference:

```plaintext
GET /api/users

Response Body:
[
  {
    "id": 1,
    "name": "John Doe",
    "email": "john.doe@gmail.com"
  },
  {
    "id": 2,
    "name": "Jane Smith",
    "email": "jane.smith@gmail.com"
  }
]
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q2">2. Explain the main components of the GraphQL architecture.</h3>
<p><strong>Short Answer:</strong> The GraphQL architecture revolves around several key components, each serving a distinct role in the broader ecosystem.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

The **GraphQL architecture** revolves around several key components, each serving a distinct role in the broader ecosystem.

<p><b>Core Components:</b></p>

1. **Client**: The client initiates data requests, specifying their shape and content through GraphQL queries. This permits more streamlined data access compared to traditional REST operations.

2. **Server**: It's the server's task to process incoming GraphQL queries and deliver the relevant data in response. This paradigm of executing GraphQL queries is defined as "query execution."

3. **Schema**: The schema serves as the contract between the client and the server, establishing the **type system**, namely the types of data available for interaction (e.g., `User`, `Post`) and the **operations** that can be performed (e.g., `Query`, `Mutation`).

4. **Resolver Functions**: These functions are associated with each **field** in a GraphQL type and dictate how that field's data should be retrieved or manipulated. For instance, a resolver for a `user` field within a `Query` type might describe how to fetch a user.

5. **Query Validator and Executor**: After a query is received, the server performs a two-stage process: **validation** (ensuring the query adheres to the schema) and **execution** (fetching data as per the validated query and its resolvers).

<p><b>Supporting Components:</b></p>

  - **Data Source**: Represents the origin of real data, like a database. Each resolver can pull data from different data sources, which can improve modularity and scalability.

  - **Operations**: On the server, these can be of two types: `Query` for reading data and `Mutation` for modifying data. Additionally, one can write `Subscription` operations for real-time data updates.

<p><b>Flow of Operations:</b></p>

  - **Query**: Sent by the client to specify the data requirements. It's validated, and only if successful, the server operates on it.
  
  - **Validation**: The query is verified against the schema to confirm its correctness. If any elements in the query violate the schema, an error is sent back to the client.
  
  - **Execution**: The server employs the resolved functions to retrieve or process the required data, responding with the results in the expected format.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q3">3. Can you describe the structure of a GraphQL query?</h3>
<p><strong>Short Answer:</strong> A GraphQL query specifies the data you seek and the shape you expect it back in. It's composed of fields nested within each other, forming a query tree.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

A **GraphQL query** specifies the data you seek and the shape you expect it back in. It's composed of **fields** nested within each other, forming a **query tree**.

<p><b>Language Elements:</b></p>

- **Fields**: The basic unit of a query, representing a piece of data you want to retrieve.
  
- **Arguments**: Used to customize the result of a field with specific parameters.

- **Aliases**: Enables multiple references to the same field with different configurations.

- **Fragments**: Reusable group of fields, improving the organization of query documents.

- **Directives**: Provide conditional query execution and value manipulation.

- **Operation Types**: Defines whether the query is for fetching data (`query`) or mutating data (`mutation`).

<p><b>Query Example: Fetching a User's Name and Last 5 Posts On Most Recently Used Device:</b></p>

GraphiQL Example:

```graphql
query {
  currentUser {
    name
    posts(last: 5)
  }
}
```

JSON Response that May be Returned:

```json
{
  "user": {
    "name": "John Doe",
    "posts": [
      // Array of post objects
    ]
  }
}
```

<p><b>Query Syntax - Code Example: Firebase API:</b></p>

Here is the **Node.js** code:

  ```javascript
  var query = /* GraphQL */ `{
    currentUser {
      name
      posts(last: 5)
    }
  }`;

  firebaseUserModel.query(query).then(response => {
    console.log("User Data:", response);
  });
  ```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q4">4. What are the core features of GraphQL?</h3>
<p><strong>Short Answer:</strong> Let's look into the core features of GraphQL, a query language and runtime designed by Facebook to enable efficient data communication between the client and server.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Let's look into the core features of **GraphQL**, a query language and runtime designed by Facebook to enable efficient data communication between the client and server.

<p><b>Core Features:</b></p>

- **Declarative Data Fetching**: Empowers clients to request exactly what they need. With REST, developers often over-fetch or under-fetch data, causing inefficiencies in both data transmission and rendering. In contrast, GraphQL allows clients to specify their data requirements, leading to more efficient and specific data retrieval.

    - **Example**: Here is a structural query defined with GraphQL, automatically fetching necessary data.

    ```graphql
    query {
      user(id: "123") {
        name
        posts {
          title
          content
        }
      }
    }
    ```

- **Hierarchical Structure**: Data is structured as a graph. GraphQL directives, which are used to annotate and modify existing schema types, can be coupled with the query language to impose rules on the query execution. For instance, `@include` and `@skip` enable conditional fetching of fields.

    - **Example**: The following query demonstrates conditional fetching using directives.

    ```graphql
    query {
      user(id: "123") {
        name
        posts {
          title
          content
          comments @include(if: $showComments)
        }
      }
    }
    ```

- **Strongly-Typed Schema**: Businesses and developers can benefit from type safety, reducing errors and unexpected behaviors. Every GraphQL API is formed from a set of well-defined object types with precise fields. This type system is backed by a schema that needs to be explicitly declared and shared.

  - **Example**: The schema-first approach uses SDL (Schema Definition Language) to define types and their relationships.

    ```graphql
    type User {
        id: ID!
        name: String!
        age: Int
    }
    ```

- **Single Endpoint for All Operations**: Simplifies the management and orchestration of data, as a single endpoint is utilized for all data interactions. This differs from REST-centric approaches, where endpoints are typically specific to resources or actions, leading to potential confusion in larger systems.

- **Built-in Documentation**: Provides auto-generated and readily-accessible documentation, easing the burden of maintaining external documentation. This "graphiql" in-browser environment, often utilized during the development stage, allows an interactive exploration of the available API and assists in writing precise queries.

- **Introspection**: Enables tools to query the GraphQL server itself for its schema. This meta-level functionality enhances the extensibility and productivity of developers by facilitating functionalities like dynamic query generation and language or platform-specific tooling.

- **Real-time Data**: Through **Subscriptions,** GraphQL offers a method for the server to actively push data to clients, creating remarkable opportunities for real-time interactions in modern apps. Whether it's chat applications or collaborative documents, this feature provides a seamless experience for end-users.

    - **Example**: A GraphQL query incorporating real-time data acquisition.

    ```graphql
    subscription {
      newUser {
        id
        name
      }
    }
    ```

<p><b>Benefits of Using GraphQL:</b></p>

- **Reduction in Over/Under Fetching**: Empowers clients to receive precisely the data they need, eradicating the efficiency challenges associated with over-fetching and under-fetching.

- **Improved Frontend Autonomy**: Fosters frontend independence, allowing teams to evolve their applications without necessitating corresponding backend alterations.

- **Enhanced Tooling and Efficiency**: The robust type system and schema enable advanced tooling and provide developers with comprehensive insights even at the time of query construction.

- **Adaptability and Evolvability**: Facilitates a more streamlined development lifecycle, particularly in contexts featuring rapid evolution or requirements for distinct client applications like web, mobile, and IoT.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q5">5. What are the advantages of using GraphQL over other API query languages?</h3>
<p><strong>Short Answer:</strong> GraphQL offers many advantages over traditional REST APIs, ranging from optimized client-server communication to improved developer experience.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

**GraphQL** offers many advantages over traditional REST APIs, ranging from optimized client-server communication to improved developer experience.

<p><b>Advantages over REST:</b></p>

<p><b>Efficient Data Retrieval:</b></p>

- **Selectivity**: GraphQL allows clients to specify the exact fields they need, reducing data over-fetching.
- **No Multiple Endpoints**: Instead of hitting multiple endpoints for diverse data, clients can make a single request.

<p><b>Data Integrity:</b></p>

- **Strongly Typed Schema**: GraphQL ensures data consistency by defining a schema, a feature not inherent in REST.
- **Structured Endpoints**: REST APIs can alter data formats and required attributes, making assumptions about endpoint responses more error-prone.

<p><b>Client-Specific Data Shaping:</b></p>

- **Client Needs Alignment**: GraphQL aligns server data with client requirements, promoting a more tailored approach for each client.

<p><b>Reduced Chatter:</b></p>

- **Mitigated Under-Fetching**: REST can suffer from under-fetching, prompting multiple requests for comprehensive data.
- **Streamlined Data Collection**: GraphQL, on the other hand, accesses interconnected entities and their data with one consolidated request.

<p><b>Real-Time Flexibility:</b></p>

- **Socket-Like Experience**: Integrated subscriptions in GraphQL allow for real-time updates, a feature often necessitating additional effort in REST.

<p><b>Advantages over Other Query Languages:</b></p>

<p><b>Multiple Data Sources:</b></p>

- **Unified Backend**: With GraphQL, you can amalgamate data from various sources into a single endpoint, a setup that's more challenging with other languages like SQL.

<p><b>Ecosystem Integration:</b></p>

- **Comprehensive API**: GraphQL has a robust toolset, including playgrounds that offer live interaction.
- **Inherent Documentation**: Its introspective nature ensures self-documenting APIs, a feature often less prominent in other query languages.

<p><b>Post-Query Actions:</b></p>

- **Control Over Response**: Clients have unparalleled influence over the response format, something less straightforward in languages like SQL.
- **Data Manipulation**: With GraphQL, you can extrapolate data for specific tasks, going beyond the typical "get" operations.

<p><b>Embedded Domain Solutions:</b></p>

- **Domain-Driven Applications**: GraphQL is effective in presenting the domain model to the user, enhancing user interaction and comprehension.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q6">6. What problem does GraphQL solve for frontend teams?</h3>
<p><strong>Short Answer:</strong> GraphQL gives the frontend a typed schema and lets the client select the fields needed for a view. That can reduce overfetching and underfetching, especially when one screen needs data that would otherwise require several REST endpoints.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

GraphQL gives the frontend a typed schema and lets the client select the fields needed for a view. That can reduce overfetching and underfetching, especially when one screen needs data that would otherwise require several REST endpoints.

The tradeoff is that GraphQL shifts work into schema design, resolvers, caching, authorization, and query cost control. A good answer says GraphQL improves the data contract when the graph is designed well, not that it automatically makes every request faster.

Common mistake: Saying "GraphQL prevents overfetching" without mentioning that resolvers can still fetch too much or do expensive backend work.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q7">7. When is REST simpler than GraphQL?</h3>
<p><strong>Short Answer:</strong> REST can be simpler for file downloads, uploads, public cacheable resources, small CRUD APIs, webhook-style integrations, and teams without schema governance. REST also maps naturally to HTTP caching and resource URLs.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

REST can be simpler for file downloads, uploads, public cacheable resources, small CRUD APIs, webhook-style integrations, and teams without schema governance. REST also maps naturally to HTTP caching and resource URLs.

That does not make GraphQL bad. It shows judgment. Choose GraphQL when the product has multiple clients, nested data needs, strong schema benefits, or frontend screens that suffer from overfetching, underfetching, and endpoint coordination.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Schema, Types & Directives -->
<h3 id="q8">8. What is a GraphQL schema and why is it important?</h3>
<p><strong>Short Answer:</strong> GraphQL Schema serves as the contract between client and server, outlining available data types, their relationships, and the API surface.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

**GraphQL Schema** serves as the contract between client and server, outlining available data types, their relationships, and the API surface.

<p><b>Core Schema Components:</b></p>

<p><b>Object Types:</b></p>

Data in GraphQL is wrapped in object types. Each type comprises a set of fields, which can be other object types or scalar types.

Example:

The `User` type may comprise fields like `id` (a scalar) and `posts` (a list of the `Post` type).

<p><b>Scalar Types:</b></p>

Scalar types are the atomic data types of GraphQL. They include standard types like `String`, `Int`, `Float`, `Boolean`, and `ID`. Custom scalar types allow for tailored behaviors, like `DateTime` for consistent date representation.

<p><b>Query and Mutation Types:</b></p>

Both are **entry points** for the client:

- **Query**: Specifies available read operations clients can invoke.
- **Mutation**: Defines write operations.

Example:

```graphql
type Mutation {
  createUser(name: String!): User
}
```

<p><b>Input Types:</b></p>

These represent data the client sends to the server during mutations. They are similar to object types but exclusively used as input.

Example:

```graphql
input UserInput {
  name: String!
}
```

<p><b>Interfaces and Unions:</b></p>

These facilitate **complex type hierarchies**.

- **Interfaces**: A collection of shared fields which GraphQL types can implement.
- **Unions**: Acts as an "or" statement, allowing multiple types to be returned.

Example:

```graphql
interface Post {
  content: String!
  author: User!
}

type TextPost implements Post {
  content: String!
  author: User!
  wordCount: Int!
}

type ImagePost implements Post {
  content: String!
  author: User!
  imageUrl: String!
}

type Query {
  allPosts: [Post]!
}
```

<p><b>Directives:</b></p>

These are like annotations and can modify the behavior of an operation. While they don't define data types, they are still part of the type system.

Example:

```graphql
directive @auth on FIELD_DEFINITION

type User {
  id: ID
  email: String! @auth
  password: String! @auth
}
```

<p><b>Enumerations:</b></p>

These are custom object types that enumerate a defined set of options.

Example:

```graphql
enum UserRole {
  ADMIN
  USER
}
```

<p><b>Multiple Types:</b></p>

A single GraphQL schema can **consist of various** types, including those mentioned above. Every field in the schema needs to resolve to one of the defined types.

<p><b>Why Are Schemas Important?:</b></p>

- **Clear Communication**: Schemas act as a clear API contract between the client and the server.
- **Structured Data**: They define data types and relationships, ensuring a structured data model.
- **Safety**: The schema helps in error detection and makes sure data types are consistently handled across the application.
- **Ease of Collaboration**: Schemas ensure that a front-end and back-end developer can work independently as long as they adhere to the schema contract.
- **Documentation Generation**: Schemas can be used to auto-generate developer-friendly documentation, promoting clarity and comprehension. 

<p><b>Schema Evolution:</b></p>

A GraphQL schema, like any software, is **subject to change and evolution**. However, changes need to be managed to ensure query compatibility. Visual tools, versioning strategies, and strong communication between teams are vital for seamless schema evolution.

<p><b>Implementing Schemas and Types in Code:</b></p>

Below is the Node.js code:

1. **Define Schema and Types** with GraphQL

   ```javascript
   const { GraphQLObjectType, GraphQLSchema, GraphQLString, GraphQLList, GraphQLNonNull, GraphQLInterfaceType } = require('graphql');

   const UserType = new GraphQLObjectType({
      name: 'User',
      fields: () => ({
         id: { type: GraphQLString },
         name: { type: new GraphQLNonNull(GraphQLString) },
         posts: {
            type: new GraphQLList(PostType),
            resolve: (user) => getUserPosts(user.id),
         },
      }),
   });
   
   const PostType = new GraphQLInterfaceType({
      name: 'Post',
      fields: () => ({
         content: { type: GraphQLString },
         author: { type: UserType },
      }),
      resolveType: (post) => {
         if (typeof post.wordCount !== 'undefined') {
            return 'TextPost';
         }
         return 'ImagePost';
      },
   });
   
   module.exports = new GraphQLSchema({
      types: [UserType, PostType],
      query: new GraphQLObjectType({
         name: 'RootQueryType',
         fields: {
            allPosts: {
               type: new GraphQLList(PostType),
               resolve: getAllPosts,
            },
         },
      }),
   });
   ```

2. **Specify Directives**

   ```javascript
   const { GraphQLDirective, DirectiveLocation, GraphQLString } = require('graphql');
   
   const authDirective = new GraphQLDirective({
      name: 'auth',
      description: 'Directive to control access to secure fields.',
      locations: [DirectiveLocation.FIELD_DEFINITION],
      args: {
         requires: { type: new GraphQLNonNull(GraphQLString) },
      },
      resolve: (next, src, args, context) => {
         // Implement your authentication logic
         return next();
      },
   });
   
   module.exports = new GraphQLSchema({
      directives: [authDirective],
      types: [UserType],
      query: new GraphQLObjectType({
         name: 'RootQueryType',
         fields: {
            user: {
               type: UserType,
               resolve: (root, args, context) => {
                  // Provide field values here
               },
               users: {
                  type: new GraphQLList(UserType),
                  auth: {
                     requires: 'admin',
                  },
                  resolve: (root, args, context) => {
                     // Provide field values here
                  },
               },
            },
         },
      }),
   });
   ```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q9">9. What is a GraphQL schema?</h3>
<p><strong>Short Answer:</strong> A schema is the typed contract exposed by a GraphQL server. It defines which operations are available, which object types exist, which fields can be selected, what arguments are accepted, and which values can be null.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

A schema is the typed contract exposed by a GraphQL server. It defines which operations are available, which object types exist, which fields can be selected, what arguments are accepted, and which values can be null.

For a frontend engineer, the schema is a working client contract. It shapes generated types, component fragments, form input objects, error handling, and the long-term compatibility of old clients.


type Product {
  id: ID!
  name: String!
  price: Money!
  imageUrl: String
}

type Query {
  product(id: ID!): Product
}
Common mistake: Treating the schema as a JSON response shape. The schema is a contract with validation, nullability, field ownership, and evolution rules.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q10">10. Explain the concept of fields in GraphQL.</h3>
<p><strong>Short Answer:</strong> Fields form the basis of GraphQL data retrieval. Whereas REST often necessitates multiple endpoints, GraphQL consolidates this need into a single query. GraphQL representations are akin to objects, with each object possibly possessing numerous fields. This creates a hierarchy, especially useful when interacting with more complex datasets.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

**Fields** form the basis of GraphQL data retrieval. Whereas REST often necessitates multiple endpoints, GraphQL consolidates this need into a single **query**.

GraphQL representations are akin to objects, with each object possibly possessing numerous **fields**. This creates a hierarchy, especially useful when interacting with more complex datasets.

<p><b>Basic Structure:</b></p>

Queries consist of one or more fields. Each field can be an object, a scalar value, or an array of other objects or scalar values.

Structurally, a **field** within a query resembles an object property in JavaScript or a dictionary entry in Python.

<p><b>Self-Referring Objects:</b></p>

Fields can maintain a one-to-one mapping with backend resources. However, they can also **refer to themselves**. This self-reference is invaluable for processing hierarchical data structures.

A simple example is a tree, where each node can potentially have multiple child nodes.

GraphQL exploits self-referential fields to enable powerful data relationships, such as nodes having other nodes as their children. 

<p><b>Code Example: Simple Query:</b></p>

Here is the JSON representation:

```json

{
  "query": {
    "user": {
      "id": 123,
      "name": "John Doe"
    }
  }
}
```

And here is the corresponding algorithm:

```javascript
function fetchData(query) {
  const result = {};
  for (let field in query) {
    if (isValidField(field)) {
      result[field] = fetchData(query[field]);
    }
  }
  return result;
}
```

<p><b>Code Example: Self-Referring Queries:</b></p>

Here are the JSON representation and the corresponding Python algorithm:

```json

{
  "query": {
    "user": {
      "id": 123,
      "posts": {
        "title": "GraphQL Basics"
      }
    }
  }
}
```

```python
def fetch_user_data(user_id, query):
    user_data = fetch_user_from_db(user_id)
    result = {}

    for field, value in user_data.items():
        if field in query:
            if isinstance(value, dict):
                result[field] = fetch_user_data(user_id, query[field])
            else:
                result[field] = value

    return result
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q11">11. How does GraphQL handle data types?</h3>
<p><strong>Short Answer:</strong> GraphQL brings a robust type system that ensures clear data structures and reliable schema enforcement. Let's take a closer look at key concepts like Scalars, Enums, and Input Types.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

**GraphQL** brings a robust **type system** that ensures clear data structures and reliable schema enforcement. Let's take a closer look at key concepts like **Scalars**, **Enums**, and **Input Types**.

<p><b>Types in GraphQL:</b></p>

- **Scalar**: Represents a single value, such as a string or number.
- **Object**: Defines a structured collection of fields, each with its type.
- **List**: Indicates an array of values of the specified type.
- **Enum**: Offers a predefined set of possible values.
- **Union**: Represents a selection of object types, yet only allows querying common fields.
- **Interface**: Guarantees certain fields on all possible implementing types.

<p><b>Code Example: Basic Scalar and Object Types:</b></p>

Here is Schema Definition Language (SDL):

- For a scalar type

```graphql
scalar DateTime
```

- For an object type

```graphql
type Author {
  id: ID!
  name: String
  books: [Book]
}
```

And here is the complete schema with Query and Mutation:

```graphql
type Query {
  author(id: ID!): Author
  allAuthors: [Author]
}

type Mutation {
  addAuthor(name: String!): Author
}

type Book {
  title: String
  author: Author
}
```

<p><b>Code Example: Using Enums and Union Types:</b></p>

Here is schema using Enums:

```graphql
enum Episode {
  NEW_HOPE
  EMPIRE
  JEDI
}

type Character {
  name: String!
  appearsIn: [Episode!]!
}
```

And here is an example using Union Types:

```graphql
type Human {
  name: String!
  height(unit: LengthUnit = METER): Float
}

type Droid {
  id: String!
  name: String!
}

union SearchResult = Human | Droid
```

<p><b>Code Example: Custom Input Types:</b></p>

Here is a code example using **Scalars** and **Input Types**:

- For a scalar input:

```graphql
input DateRange {
  start: DateTime
  end: DateTime
}
```

- For a custom input type:

```graphql
type Query {
  getPosts(publishedAfter: DateRange): [Post]
}
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q12">12. What are scalar types in GraphQL?</h3>
<p><strong>Short Answer:</strong> GraphQL augments traditional data modeling by incorporating its unique concept of scalars, which represent singular, atomic data types.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

**GraphQL** augments traditional data modeling by incorporating its unique concept of **scalars**, which represent singular, atomic data types.

<p><b>Core Scalars:</b></p>

- **Int**: A signed 32-bit integer.
- **Float**: A double-precision floating-point number.
- **String**: A sequence of characters.

The **Boolean** type, representing true or false, is also one of the core scalars.

<p><b>Custom Scalars:</b></p>

Developers can define custom data types using **custom scalars** to match specific requirements. For instance, `Date` might be a developer-defined custom scalar that conforms to date-time values.

GraphQL provides easy extensibility through custom scalars to cater to diverse data types not covered by its core set or to enforce data consistency.

<p><b>Advantages:</b></p>

- **Uniformity**: Scalars ensure consistent data representation across diverse clients.
- **Ease of Extension**: Custom scalars let you unleash flexibility within GraphQL, tailoring data types to your unique needs.
- **Efficiency**: Since each query selects precisely what's needed, reduced data transmission decreases loading time and conserves bandwidth.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q13">13. What are scalar, object, enum, and input types?</h3>
<p><strong>Short Answer:</strong> Scalars are leaf values such as String, Int, Float, Boolean, and ID. Object types contain fields that can be selected. Enums limit a value to a known set of names. Input types describe structured arguments for queries and mutations.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Scalars are leaf values such as String, Int, Float, Boolean, and ID. Object types contain fields that can be selected. Enums limit a value to a known set of names. Input types describe structured arguments for queries and mutations.


enum SortDirection {
  ASC
  DESC
}

input ProductFilterInput {
  query: String
  inStockOnly: Boolean
}
Input types are separate from output object types because output types can contain computed fields, relationships, interfaces, unions, or resolver-only behavior that does not make sense as input.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q14">14. How do non-null fields and null bubbling work?</h3>
<p><strong>Short Answer:</strong> String! means the field must not be null. [Product!]! means the list itself is not null and none of its items are null. Nullability is a product contract because it decides whether the UI can show partial data or must treat the parent object as unavailable.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

String! means the field must not be null. [Product!]! means the list itself is not null and none of its items are null. Nullability is a product contract because it decides whether the UI can show partial data or must treat the parent object as unavailable.

If a non-null field resolves to null during execution, GraphQL adds an error and bubbles the null up to the nearest nullable parent. Overusing ! can make a small resolver failure blank out a larger part of the response.

Good answer shape: Explain the UI consequence. A nullable imageUrl lets the product card render a placeholder. A non-null price says the card is not useful without price, so failure should be more visible.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q15">15. When would you use a custom scalar?</h3>
<p><strong>Short Answer:</strong> Use a custom scalar when a value needs domain-specific serialization or validation, such as DateTime, URL, EmailAddress, or JSON.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Use a custom scalar when a value needs domain-specific serialization or validation, such as DateTime, URL, EmailAddress, or JSON.

The tradeoff is that clients need to know the runtime format. A schema can say DateTime, but frontend code still needs documentation or generated scalar mappings that explain whether the value is an ISO string, number, or custom object.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q16">16. What is the difference between an interface and a union?</h3>
<p><strong>Short Answer:</strong> An interface defines shared fields that multiple object types must implement. A union says a field may return one of several object types without requiring shared fields.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

An interface defines shared fields that multiple object types must implement. A union says a field may return one of several object types without requiring shared fields.

Use an interface when the types share a real contract:


interface Node {
  id: ID!
}
Use a union for heterogeneous results such as search:


union SearchResult = Product | Article | Brand
In frontend code, both usually require checking __typename before rendering type-specific fields.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q17">17. What are directives in GraphQL?</h3>
<p><strong>Short Answer:</strong> Directives annotate parts of a GraphQL document or schema to change behavior. Common built-in directives include @include, @skip, and @deprecated.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Directives annotate parts of a GraphQL document or schema to change behavior. Common built-in directives include @include, @skip, and @deprecated.


query ProductDetails($id: ID!, $showReviews: Boolean!) {
  product(id: $id) {
    id
    name
    reviews @include(if: $showReviews) {
      rating
      body
    }
  }
}
For frontend interviews, explain directives as part of the data contract. @include can conditionally fetch a field, while @deprecated tells clients a schema field is being phased out.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q18">18. How do generated GraphQL types help and where can they hurt?</h3>
<p><strong>Short Answer:</strong> Generated types catch mismatches between operations and frontend code. They help when a selected field can be null, when a union needs narrowing, or when a mutation input changes.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Generated types catch mismatches between operations and frontend code. They help when a selected field can be null, when a union needs narrowing, or when a mutation input changes.

They can hurt if teams treat generated types as architecture. Codegen cannot fix a vague schema, unstable IDs, unsafe nullability, or a mutation that returns too little data. It is a guardrail, not a replacement for schema ownership.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Queries, Mutations & Resolvers -->
<h3 id="q19">19. In GraphQL, what are queries and mutations?</h3>
<p><strong>Short Answer:</strong> In GraphQL, developers use two main types of operations to interact with data, known as Queries and Mutations.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

In **GraphQL**, developers use two main types of operations to interact with data, known as **Queries** and **Mutations**.

<p><b>Queries:</b></p>

- **Purpose**: Read data from the server.
- **HTTP Equivalent**: Usually `GET`.
- **Immutability**: Queries are **Immutable**; they don't change server data.
- **Requesting Specific Fields**: Allows clients to fetch only the data they need, increasing efficiency.
- **Caching**: Results can be cached since queries remain consistent unless modified by the client.
- **Errors**: Fails if the server cannot fulfill the data request.

<p><b>Mutations:</b></p>

- **Purpose**: Modify data on the server.
- **HTTP Equivalent**: Typically `POST` or `PUT`.
- **Immutability**: Mutations are **Mutable**; they trigger data changes.
- **Requesting Specific Fields**: Can include a return payload of specific fields for client updates post-mutation.
- **Caching**: Results are typically not cacheable.
- **Errors**: Can indicate both successes and failures, and usually carry specific feedback.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q20">20. What is the difference between a query, mutation, and subscription?</h3>
<p><strong>Short Answer:</strong> A query reads data. A mutation represents a write or state-changing operation. A subscription streams updates over a long-lived connection such as WebSocket or server-sent events.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

A query reads data. A mutation represents a write or state-changing operation. A subscription streams updates over a long-lived connection such as WebSocket or server-sent events.

For frontend work, the distinction matters because each operation drives different UI states. A query needs loading, empty, success, partial-error, and retry states. A mutation needs pending, optimistic, success, rollback, validation-error, and duplicate-submit handling. A subscription needs connection, reconnect, stale-event, and auth-expiry behavior.

Interview-ready add-on: A mutation should usually return the changed object or payload the UI needs to update the cache. Returning only success: true often forces a refetch or leaves the client guessing.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q21">21. Describe how you would fetch data with a GraphQL query.</h3>
<p><strong>Short Answer:</strong> When integrating GraphQL, data retrieval is performed through a query.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

When integrating **GraphQL**, data retrieval is performed through a query.

<p><b>Steps for Fetching Data with a GraphQL Query:</b></p>

1. **Define the Query**:
    GraphQL queries specify the exact shape and structure of the expected response using the same dataset as the server schema.

2. **Execute the Query**:
    Queries are typically triggered via an HTTP POST request to the server's endpoint.

3. **Handle the Response**:
    Expect the exact data structure that you requested, with no need for subsequent requests or data manipulation.	errors, and then receive the data in the precise shape you requested.

<p><b>Example GraphQL Query:</b></p>

```graphql
query {
  bookById(id: "4") {
    title
    author {
      name
      age
    }
  }
}
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q22">22. Explain the role of resolvers in GraphQL.</h3>
<p><strong>Short Answer:</strong> Resolvers in GraphQL tie specific fields of a schema to the actual functions that resolve these fields. They are critical for data fetching and manipulation.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

**Resolvers** in GraphQL tie specific fields of a schema to the actual functions that resolve these fields. They are critical for data fetching and manipulation.

<p><b>Core Functions of Resolvers:</b></p>

- **Data Fetching**: The primary role of resolvers is to fetch the data for the fields they are responsible for.
- **Data Transformation**: Resolvers can perform any necessary transformations on the data before returning it to the client.
- **Data Source Specification**: Resolvers detail where to retrieve the data from (such as a database or an API).

<p><b>Resolver Structure:</b></p>

- **Single Responsibility**: A resolver is responsible for a specific field in the schema.
- **Parent-Child Relationships**: Resolvers can "pass" data between related fields, e.g., a user resolver can return details about a user's posts.

<p><b>Resolver Types:</b></p>

- **Root Resolvers**: Deal with top-level query and mutation fields.
- **Nested Resolvers**: Handle specific fields on related types.

<p><b>Code Example: Resolvers in GraphQL:</b></p>

Here is the GraphQL Schema:

```graphql
type Query {
  user(id: Int!): User
}

type User {
  id: Int!
  name: String!
  posts: [Post]
}

type Post {
  id: Int!
  title: String!
  content: String!
}
```

And here is the resolver code in JavaScript:

```javascript
const resolvers = {
  Query: {
    user: (parent, { id }, context, info) => fetchUser(id),
  },
  User: {
    posts: (parent, args, context, info) => fetchPostsForUser(parent.id),
  },
};

// Sample data for illustration
const sampleData = {
  users: [
    { id: 1, name: "John" },
    { id: 2, name: "Jane" },
  ],
  posts: [
    { id: 1, title: "First Post", content: "Hello, first post!", userId: 1 },
  ],
};

function fetchUser(id) {
  return sampleData.users.find((user) => user.id === id);
}

function fetchPostsForUser(userId) {
  return sampleData.posts.filter((post) => post.userId === userId);
}
```

In this example, when a client sends a query for a user's posts, the `posts` resolver is invoked and calls `fetchPostsForUser` to retrieve the posts associated with that user.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q23">23. What is a resolver?</h3>
<p><strong>Short Answer:</strong> A resolver is the server-side function that returns the value for a schema field. It may read from a database, call another API, compute a value, or delegate to another service.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

A resolver is the server-side function that returns the value for a schema field. It may read from a database, call another API, compute a value, or delegate to another service.

Frontend engineers are not always expected to implement resolvers, but they should understand the cost boundary. One GraphQL request can trigger many resolver calls behind the scenes, so a harmless-looking nested query can be expensive.


const resolvers = {
  Query: {
    product: (_parent, args, context) => {
      return context.productService.findById(args.id);
    },
  },
};
Good answer shape: Mention the usual resolver inputs: parent value, field arguments, request context, and execution info. Then connect that to auth, batching, and observability.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q24">24. How do you pass arguments to fields in GraphQL queries?</h3>
<p><strong>Short Answer:</strong> In GraphQL, queries represent requests for specific data fields. To refine these requests, you can use arguments with fields.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

In GraphQL, **queries** represent requests for specific data fields. To refine these requests, you can use **arguments** with fields. 

<p><b>Syntax for Passing Arguments:</b></p>

To **pass arguments**, include them within the parentheses next to the field name. Each argument is defined using its unique name followed by the colon `:` and the intended value.

<p><b>Example: Retrieve a Specific User:</b></p>

```graphql
{
  user(id: "XYZ_123") {
    name
    email
  }
}
```

<p><b>Code Example: Passing Arguments:</b></p>

Here is the GraphQL schema:

```graphql
type Query {
  booksByAuthor(author: String, count: Int): [Book]
}
```

And here is the query:

```graphql
{
  booksByAuthor(author: "JK Rowling", count: 3) {
    title
  }
}
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q25">25. Why are variables preferred over string interpolation?</h3>
<p><strong>Short Answer:</strong> Variables keep the GraphQL document stable while passing dynamic values separately. They are validated by type, easier to reuse, safer than string-building, and friendlier to operation caching or persisted documents.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Variables keep the GraphQL document stable while passing dynamic values separately. They are validated by type, easier to reuse, safer than string-building, and friendlier to operation caching or persisted documents.


query ProductDetails($id: ID!) {
  product(id: $id) {
    id
    name
    price {
      amount
      currency
    }
  }
}
Variables:


{ "id": "product_123" }
Common mistake: Building query strings with template literals and user input. That makes validation, caching, escaping, and operation tracking harder.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q26">26. What are aliases and when would you use them?</h3>
<p><strong>Short Answer:</strong> Aliases rename response keys. They are useful when querying the same field more than once with different arguments, or when the UI needs two differently named versions of the same schema field.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Aliases rename response keys. They are useful when querying the same field more than once with different arguments, or when the UI needs two differently named versions of the same schema field.


query CompareProducts {
  left: product(id: "product_1") {
    id
    name
  }
  right: product(id: "product_2") {
    id
    name
  }
}
Without aliases, both selections would produce the same product key and conflict.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q27">27. What is a fragment in GraphQL and how are they used?</h3>
<p><strong>Short Answer:</strong> In GraphQL, a fragment enables describing a set of fields that can be repeatedly used across multiple queries.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

In **GraphQL**, a **fragment** enables describing a set of fields that can be repeatedly used across multiple queries.

<p><b>Benefits of Fragments:</b></p>

- **Reusability**: Easily reuse identical fields in various queries.
- **Modularity**: Enhance code organization by separating logical groupings.
- **Clarity**: Increase readability by outlining expected data needs in one place.

<p><b>Fragment Definition and Reference:</b></p>

<p><b>Definition:</b></p>

Fragments are crafted using the `fragment` keyword and must specify a **name** along with the desired fields. They are scoped to a particular type.

```graphql
fragment UserInfo on User {
  id
  name
  email
}
```

<p><b>Reference:</b></p>

To incorporate a fragment into a query, you utilize the `...` (spread) syntax followed by the fragment name.

```graphql
query GetUserAndTheirPost {
  user(id: "123") {
    ...UserInfo
  }
  postsForUser(id: "123") {
    ...PostInfo
  }
}
```

<p><b>Handling Duplicates:</b></p>

While fragments help with code modularity and repeated field lists, GraphQL servers are smart enough to **deduplicate** and combine fields from all sources, ensuring minimal overhead in the underlying data fetch.

<p><b>Multiple Fragments:</b></p>

Queries can reference multiple fragments, and the fields from all fragments get composed in the query, streamlining data handling.

```graphql
query GetMyData {
  myself {
    ...BasicUserInfo
    ...ExtendedUserInfo
    ...UserAddressInfo
  }
}
```

<p><b>Client-Specific Fragments:</b></p>

Sometimes, clients might have unique field requirements that the server's general schema doesn't cover. For this, client-specific fragments offer an avenue to define custom fields tailored to the client's needs.

```graphql
fragment DisplayUserInfo on User {
  ... on RegularUser {
    subscriptionStatus
    lastLogin
    securityQuestions
  }
  ... on AdminUser {
    permissions
    staffSince
  }
}
```

In contrast to globally defined fragments, client-specific fragments cater to the specific needs of the query or operation where they're referenced.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q28">28. How do fragments help?</h3>
<p><strong>Short Answer:</strong> Fragments define reusable field selections. They are most useful when components own their data needs, because the fragment can live near the component that renders those fields.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Fragments define reusable field selections. They are most useful when components own their data needs, because the fragment can live near the component that renders those fields.


fragment ProductCardFields on Product {
  id
  name
  imageUrl
  price {
    amount
    currency
  }
}
Fragments improve consistency, but they can also hide overfetching if teams create one large shared fragment for every screen. A useful fragment represents what a component actually renders.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q29">29. What should a mutation return?</h3>
<p><strong>Short Answer:</strong> A mutation should return enough data for the client to update the UI safely. That might be the changed entity, affected list metadata, aggregate counts, or a domain-specific payload with validation errors.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

A mutation should return enough data for the client to update the UI safely. That might be the changed entity, affected list metadata, aggregate counts, or a domain-specific payload with validation errors.


mutation UpdateCartLine($input: UpdateCartLineInput!) {
  updateCartLine(input: $input) {
    cart {
      id
      totalItems
      subtotal {
        amount
        currency
      }
    }
    line {
      id
      quantity
    }
    userErrors {
      field
      message
    }
  }
}
Returning only success: true is weak because the frontend still needs to refetch, guess, or manually patch state without enough information.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Performance, Caching & Subscriptions -->
<h3 id="q30">30. How does GraphQL handle caching?</h3>
<p><strong>Short Answer:</strong> Data Federation in GraphQL, achieved through resolvers, instigates caching at multiple levels to heighten efficiency and optimize data handling.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

**Data Federation** in GraphQL, achieved through resolvers, instigates caching at multiple levels to heighten efficiency and optimize data handling.

<p><b>Caching Strategies:</b></p>

<p><b>Level 1: Client-Side Caching:</b></p>

- **Purpose**: Minimize network traffic and local state management.
- **Mechanism**: `Apollo Client` offers automatic in-memory caching. This ensures that redundant requests such as querying the same data multiple times don't hit the server.

<p><b>Level 2: Cloud-Controlled Caching:</b></p>

- **Purpose**: Amplify efficiency by using explicitly stated HTTP caching directives.
- **Mechanism**: The caching mechanism of the server is dependent on the HTTP cache-control headers. If data is cacheable, these headers specify how long it should be kept in the cache.

<p><b>Level 3: Persistent Caching:</b></p>

- **Purpose**: Establish a global and persistent cache for recurrent data requests.
- **Mechanism**: Beyond the scope of GraphQL per se, several solutions like Redis for in-memory caching or Apache Ignite as a distributed cache facilitate data storage, minimizing the need for repeated remote calls.

<p><b>Multi-Level Cache Coherency:</b></p>

GraphQL employs strategies to ensure coherence across the various cache levels:

- **Real-Time Feed**: With subscriptions, a server can alert the client about new data, prompting cache updates.
- **Partial Updates**: Through `GraphQL` subscriptions, you can tailor the response to only include changed or updated information, preventing a full cache refresh.
- **Optimistic UI and cache updates**: `Apollo Client` manages client-side cache updates, providing immediate UI feedback. Updates are subsequently synched with the server, ensuring coherence.

<p><b>Code Example: Caching Directives:</b></p>

Here is the `GraphQL SDL` schema definitions:

```graphql
type Query {
  # Utilizes defaults from server config
  getUser(id: ID!): User @cacheControl

  # A specific request with an assigned cache time
  getPost(id: ID!): Post @cacheControl(maxAge: 60)

  # Bypasses cache directives
  getMessage(id: ID!): Message @cacheControl(maxAge: 0)
}

type User {
  id: ID!
  name: String!
  email: String!
}

type Post {
  id: ID!
  title: String!
  content: String!
}

type Message {
  id: ID!
  text: String!
}

directive @cacheControl(
  maxAge: Int
  scope: CacheScope
  inheritMaxAge: Boolean
) on FIELD_DEFINITION | OBJECT | INTERFACE
```
16. What are enums in GraphQL, and when would you use them?
17. Describe the concept of "schema-first" development in GraphQL.
18. How would you handle errors in a GraphQL API?
19. Explain the purpose of introspection in GraphQL.
20. What is the difference between an operation and a field in GraphQL?

## GraphQL Schema and Types
21. What are enums in GraphQL, and when would you use them?
22. Describe the concept of "schema-first" development in GraphQL.
23. How would you handle errors in a GraphQL API?
24. Explain the purpose of introspection in GraphQL.
25. What is the difference between an operation and a field in GraphQL?
26. How do you define object types in GraphQL?
27. What is the difference between an Interface and a Union in GraphQL?
28. Can you illustrate how GraphQL implements polymorphism?
29. What is the significance of the "!" mark in GraphQL types?
25. How do you perform validation in GraphQL?
26. Describe the role of input types in GraphQL.
27. How do you extend a GraphQL schema?
28. What are custom scalar types and when might you use them?
29. Explain the use of directives in GraphQL.
30. How does GraphQL support pagination and how is it implemented?

## GraphQL Operations and Performance
31. How do you optimize query performance in GraphQL?
32. Describe how GraphQL handles batch operations.
33. Explain how you might manage large lists of data in a GraphQL response.
34. How do subscriptions work in GraphQL?
35. What is the N+1 problem and how can it be solved in GraphQL?
36. How do you handle file uploads with GraphQL?
37. Describe how you would use GraphQL with microservices.
38. How are real-time updates managed in GraphQL?
39. What is a query planner and optimizer in the context of GraphQL?
40. How can you limit the depth or complexity of queries in GraphQL?

## Advanced GraphQL Concepts
41. What is Apollo Client and how does it interact with GraphQL?
42. Describe schema stitching and when it is useful.
43. How do you handle authentication and authorization in GraphQL?
44. What are the best practices for securing a GraphQL API?
45. How do you implement server-side caching in GraphQL?
46. Explain how to use GraphQL over HTTP.
47. What are persisted queries, and why would you use them in GraphQL?
48. How do you handle state management with GraphQL on the client side?
49. Explain the concept of optimistic Ul with GraphQL.
50. How does GraphQL integrate with existing code and APls?

## GraphQL Clients and Server Integration
51. How would you set up a GraphQL server?
52. What are the popular GraphQL client libraries?
53. How can you cache GraphQL queries on the client side?
54. Describe the process of linking a GraphQL client with a React application.
55. What are the options for hosting a GraphQL server?
56. How do you test a GraphQL API?
57. Explain how you might handle offline functionality with GraphQL.
58. What are the considerations for scaling a GraphQL backend?
59. Discuss how a GraphQL proxy layer works and its use cases.
60. How do you monitor and log GraphQL queries?

## GraphQL Tools and Ecosystem
61. Name some GraphQL IDEs and their features.
62. What is GraphQL Code Generator and how can it be used?
63. Explain how the GraphiQL tool is used.
64. What is Orchestra and how does it pertain to GraphQL?
65. Describe the role of DataLoader in GraphQL.
66. Discuss the use cases for AST (Abstract Syntax Tree) in GraphQL.
67. What are mock functions in GraphQL, and when might you use them?
68. How do you manage database migrations with GraphQL-centric development?
69. Explain how you might organize GraphQL schema in a large project.
70. What is Relay and how does it compare to Apollo Client?

## GraphQL Best Practices
71. How do you version a GraphQL API?
72. What are some common anti-patterns in GraphQL and how would you avoid them?
73. Explain the significance of field deprecation in GraphQL.
74. Discuss how you would manage access control with GraphQL.
75. What are the guidelines for effective error handling in a GraphQL API?
76. How do you organize the file structure for a GraphQL project?
77. What is the significance of naming conventions in GraphQL?
78. When should you use variables in GraphQL and how are they implemented?
79. What do you need to consider when documenting your GraphQL API?
80. How would you design mutations for complex write operations?

## GraphQL Specification and Advanced Topics
81. What is the GraphQL specification and how does it impact API development?
82. How do you extend the GraphQL spec with custom directives?
83. Explain the process of contributing to the GraphQL spec.
84. Describe how GraphQL can be used for schema federation.
85. What are possible considerations for internationalization in GraphQL APIs?
86. How does GraphQL manage de-duplication of client requests?
87. Discuss how custom middleware can be used in GraphQL.
88. Explain the concept of incremental delivery in the context of GraphQL.
89. What is the relationship between GraphQL and service workers?
90. How can GraphQL be used in conjunction with server-sent events?

## GraphQL Industry Use Cases
91. How have large-scale applications implemented GraphQL, and what can be learned from them?
92. Explain how GraphQL can be leveraged in e-commerce platforms.
93. Describe the use of GraphQL in content management systems.
94. How can GraphQL streamline workflows in enterprise applications?
95. Discuss how GraphQL has transformed frontend development practices.

## GraphQL and Modern Development Workflows
96. How does GraphQL fit into a CI/CD pipeline?
97. What role does GraphQL play in serverless architectures?
98. How do you manage database access and ORM tooling with GraphQL?
99. What's the role of GraphQL in edge computing and loT applications?
100. Describe the future prospects of GraphQL-what new developments and patterns are emerging?
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q31">31. How does GraphQL caching work on the client?</h3>
<p><strong>Short Answer:</strong> GraphQL does not define client caching by itself. Many clients normalize objects by type name and ID, then store fields separately so different queries can reuse the same entity.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

GraphQL does not define client caching by itself. Many clients normalize objects by type name and ID, then store fields separately so different queries can reuse the same entity.

For example, Apollo Client can identify an object using __typename plus id by default. That means a product returned by a list query and a product returned by a detail query can point to the same cache entity.

Cache correctness depends on stable IDs, selected fields, field arguments, pagination merge policy, and mutation responses. If a mutation response omits the changed object's ID, the client may not know which cached entity to update.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q32">32. How would you handle optimistic UI after a mutation?</h3>
<p><strong>Short Answer:</strong> Optimistic UI updates the interface before the server confirms the mutation. It works well when the operation is likely to succeed and the rollback behavior is clear.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Optimistic UI updates the interface before the server confirms the mutation. It works well when the operation is likely to succeed and the rollback behavior is clear.

For a cart quantity change, the frontend can show the new quantity immediately, disable repeated clicks while the mutation is pending, and roll back if the server rejects the change because of stock, price, or permission rules.

What to say in interviews: Name the visible states: optimistic value, pending indicator, duplicate-submit protection, rollback, validation error, and final cache consistency.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q33">33. How do you paginate a GraphQL list?</h3>
<p><strong>Short Answer:</strong> Use cursor-based pagination for feeds and changing lists when possible. The connection pattern returns edges, node, cursor, and pageInfo, which lets the UI request the next page without relying on unstable offsets.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Use cursor-based pagination for feeds and changing lists when possible. The connection pattern returns edges, node, cursor, and pageInfo, which lets the UI request the next page without relying on unstable offsets.


query ProductList($first: Int!, $after: String) {
  products(first: $first, after: $after) {
    edges {
      cursor
      node {
        id
        name
      }
    }
    pageInfo {
      hasNextPage
      endCursor
    }
  }
}
The frontend still needs to dedupe by stable ID, preserve scroll position, handle empty states, and avoid appending stale pages after filters change.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q34">34. What is the N+1 problem in GraphQL?</h3>
<p><strong>Short Answer:</strong> N+1 happens when resolving a list triggers one extra backend call per item. The frontend sees one GraphQL request, but the server may perform many database or service calls.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

N+1 happens when resolving a list triggers one extra backend call per item. The frontend sees one GraphQL request, but the server may perform many database or service calls.

Example: a products query returns 40 products, and each product's seller field calls the seller service separately. That becomes one call for the list plus 40 calls for sellers.

Common fixes include batching, request-scoped caching, joining data earlier, or using loader patterns. A frontend engineer should know enough to ask whether expensive fields are batched and whether resolver timing is observable.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q35">35. How do you protect a GraphQL API from expensive operations?</h3>
<p><strong>Short Answer:</strong> Use layered demand control. For first-party clients, trusted documents can allow only known operations in production. For broader APIs, use pagination, depth limits, breadth or alias limits, batch limits, query complexity analysis, rate limits, timeouts, and monitoring.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Use layered demand control. For first-party clients, trusted documents can allow only known operations in production. For broader APIs, use pagination, depth limits, breadth or alias limits, batch limits, query complexity analysis, rate limits, timeouts, and monitoring.

Turning off introspection is not enough. It can reduce schema discoverability in non-development environments, but it does not replace authorization, input validation, trusted documents, or operation limits.

Interview-ready answer: "I would control both who can call the API and how expensive each operation can be."
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q36">36. What are persisted or trusted documents?</h3>
<p><strong>Short Answer:</strong> Persisted documents store approved GraphQL operations on the server and let clients send an operation ID, often a hash, instead of the full document. Trusted documents go further by treating those stored operations as an allowlist for first-party production clients.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Persisted documents store approved GraphQL operations on the server and let clients send an operation ID, often a hash, instead of the full document. Trusted documents go further by treating those stored operations as an allowlist for first-party production clients.

They can improve security and operations because the server can reject unknown arbitrary documents, track known operation names, and reason about query cost ahead of time.

They do not remove authorization. A known operation can still request data the current user should not see unless the server checks permissions during execution.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q37">37. How do subscriptions work and when should you avoid them?</h3>
<p><strong>Short Answer:</strong> Subscriptions keep a long-lived connection open and push updates when server-side events happen. They are useful for chat, notifications, live dashboards, collaborative editing signals, and other flows where the user benefits from immediate updates.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Subscriptions keep a long-lived connection open and push updates when server-side events happen. They are useful for chat, notifications, live dashboards, collaborative editing signals, and other flows where the user benefits from immediate updates.

Avoid subscriptions for data that can be refreshed on navigation, loaded on demand, or polled cheaply. Subscriptions add connection state, auth renewal, reconnect logic, ordering concerns, and server resource cost.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Security, Error Handling & Workflow -->
<h3 id="q38">38. How do GraphQL errors differ from REST errors?</h3>
<p><strong>Short Answer:</strong> A GraphQL response can contain data and errors together. Request errors, such as syntax, validation, or variable-coercion errors, stop execution and do not include data. Execution errors happen at a response position and may produce partial data; older GraphQL material often calls these field errors.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

A GraphQL response can contain data and errors together. Request errors, such as syntax, validation, or variable-coercion errors, stop execution and do not include data. Execution errors happen at a response position and may produce partial data; older GraphQL material often calls these field errors.


{
  "data": {
    "product": {
      "id": "product_123",
      "name": "Everyday Backpack",
      "inventory": null
    }
  },
  "errors": [
    {
      "message": "Inventory service unavailable",
      "path": ["product", "inventory"]
    }
  ]
}
The UI should not automatically turn every GraphQL error into a full-page failure. If the missing field is non-critical, render the safe data and show a local fallback. If the failed field is essential, show a stronger error state.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q39">39. How should auth work in GraphQL?</h3>
<p><strong>Short Answer:</strong> Authentication identifies the caller. Authorization decides whether that caller can read or mutate a resource or field. Both must be enforced on the server side, usually in resolvers or the service layer behind them.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Authentication identifies the caller. Authorization decides whether that caller can read or mutate a resource or field. Both must be enforced on the server side, usually in resolvers or the service layer behind them.

Do not rely on hiding fields or buttons in the UI. A user can still send a GraphQL operation manually. The frontend can improve UX by hiding unavailable actions, but the server must remain the source of truth.

Good answer shape: Mention authentication headers or cookies, per-resource authorization, consistent error behavior, and audit logging for sensitive mutations.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q40">40. What is introspection and should it be disabled?</h3>
<p><strong>Short Answer:</strong> Introspection lets clients query the schema itself. It powers tools, autocomplete, documentation, and code generation.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Introspection lets clients query the schema itself. It powers tools, autocomplete, documentation, and code generation.

Disabling introspection can reduce schema discoverability for a private first-party API, but it also removes standard tooling and is not a security boundary. Public GraphQL APIs often leave it enabled. In either case, production security must rely on authorization, trusted documents where appropriate, demand control, and safe error messages.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q41">41. How do file uploads work with GraphQL?</h3>
<p><strong>Short Answer:</strong> GraphQL can support file uploads through conventions, but uploads often fit better as direct-to-storage or REST-style flows. The frontend concern is not only "can GraphQL upload a file?" It is progress, cancellation, retry, size limits, auth, virus scanning, and what happens if metadata succeeds but upload fails.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

GraphQL can support file uploads through conventions, but uploads often fit better as direct-to-storage or REST-style flows. The frontend concern is not only "can GraphQL upload a file?" It is progress, cancellation, retry, size limits, auth, virus scanning, and what happens if metadata succeeds but upload fails.

A practical answer says: use GraphQL for metadata and signed upload coordination when that keeps the API clean, but do not force large binary transfer through GraphQL just to be consistent.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q42">42. How does GraphQL work over HTTP?</h3>
<p><strong>Short Answer:</strong> GraphQL is not tied to one transport, but HTTP is commonly used for queries and mutations. Many GraphQL APIs send operations to a single endpoint such as /graphql. Servers commonly support POST, and some support GET for queries when it is safe and useful for caching.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

GraphQL is not tied to one transport, but HTTP is commonly used for queries and mutations. Many GraphQL APIs send operations to a single endpoint such as /graphql. Servers commonly support POST, and some support GET for queries when it is safe and useful for caching.

Do not assume HTTP status codes carry every application outcome. A well-formed operation that executes can return HTTP 200 and still contain GraphQL execution errors alongside partial data. Parse or validation failures and transport failures use different status handling, so the client must inspect both the HTTP result and the GraphQL response body.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q43">43. How do you version a GraphQL API?</h3>
<p><strong>Short Answer:</strong> Prefer additive schema evolution. Add new fields, deprecate old fields, track operation usage, migrate clients, and remove fields only after the compatibility window.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Prefer additive schema evolution. Add new fields, deprecate old fields, track operation usage, migrate clients, and remove fields only after the compatibility window.

Avoid changing a field's meaning in place. That is worse than removing it because old clients may keep working syntactically while showing wrong data.

Whole endpoint versioning can exist, but it is usually a last resort for major compatibility breaks. The normal GraphQL path is schema evolution through additive changes and deprecation.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q44">44. How would you debug a slow GraphQL screen?</h3>
<p><strong>Short Answer:</strong> Start at the user-visible symptom, then split the problem:</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Start at the user-visible symptom, then split the problem:

Inspect which operation ran and which variables changed.
Check response size and whether the query selected expensive fields.
Check client cache hit/miss behavior.
Look for duplicate requests or stale refetch loops.
Ask for resolver timing, N+1 traces, backend indexes, and service-call counts.
Measure render cost if the data arrives quickly but the screen still feels slow.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q45">45. How would you migrate one REST screen to GraphQL?</h3>
<p><strong>Short Answer:</strong> Choose one screen with clear ownership and measurable behavior. Keep the existing REST flow as a reference, design the GraphQL query around the fields the screen actually renders, generate types, handle loading and error states, compare response size and latency, and verify analytics or logs before removing the old path.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

Choose one screen with clear ownership and measurable behavior. Keep the existing REST flow as a reference, design the GraphQL query around the fields the screen actually renders, generate types, handle loading and error states, compare response size and latency, and verify analytics or logs before removing the old path.

Do not migrate every endpoint just because GraphQL is available. A safe migration proves that the schema, cache, authorization, and observability work for one product flow first.
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />
