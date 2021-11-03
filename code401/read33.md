# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 33 -->

[comment]: <> (https://docs.amplify.aws/cli/graphql-transformer/connection/)
##GraphQL @connection
The @connection directive enables you to specify relationships between @model types. Currently, this supports one-to-one, one-to-many, and many-to-one relationships. You may implement many-to-many relationships using two one-to-many connections and a joining @model type. See the usage section for details.

Relationships between types are specified by annotating fields on an @model object type with the @connection directive.

###Defining a @connection:
`directive @connection(keyName: String, fields: [String!]) on FIELD_DEFINITION`

### Example One-To-One
In the simplest case, you can define a one-to-one connection where a project has one team:
```aidl
type Project @model {
id: ID!
name: String
team: Team @connection
}

type Team @model {
id: ID!
name: String!
}
```

### Example One to Many
The following schema defines a Post that can have many comments:
```aidl

type Post @model {
id: ID!
title: String!
comments: [Comment] @connection(keyName: "byPost", fields: ["id"])
}

type Comment @model
@key(name: "byPost", fields: ["postID", "content"]) {
id: ID!
postID: ID!
content: String!
}
```

Note how a one-to-many connection needs an @key that allows comments to be queried by the postID and the connection uses this key to get all comments whose postID is the id of the post was called on. After it's transformed, you can create comments and query the connected Post as follows:

### Queries
After it's transformed, you can create comments and query the connected Post as follows:
```aidl
mutation CreatePost {
    createPost(input: { id: "a-post-id", title: "Post Title" } ) {
        id
        title
    }
}

mutation CreateCommentOnPost {
    createComment(input: { id: "a-comment-id", content: "A comment", postID: "a-post-id"}) {
        id
        content
    }
}
```

[BACK TO HOME](../README.md)