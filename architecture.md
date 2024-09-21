layout: page
title: "Use Better Architecture"
permalink: /about

# **Use Better Architecture**

## Mobile App component Diagram

```mermaid
mindmap
    ((Use Better))
    ::icon(fa fa-mobile)
        )AWS Amplify(
        ::icon(fa fa-sync)
            AWS S3
            AWS DynamoDB
            aws_cognito{{AWS Cognito}}
        Account
        ::icon(fa fa-user)
            Email Sign In
            Email Sign Up
            Google SignIn
            Apple SignIn
        User Feed
            Use Cache
        Friends Feed
            Friends Cache
        User Table Model
        Friends Map Table Model
        License Table Model


```

## AWS Backend Component Diagram

```mermaid
mindmap
    ((AWS Backend Services))
        Cognto
            UserPool                
        S3
            Public Folder
                User cognito identifier
                    Image folder
                        item_name.png
                    items.json
        DynamoDB
            User Info Table
            Friends Map Table
            Transaction Table

        Amplify
            interface for cognito
            interface for S3
            interface for DynamoDB
        AppSync
            GraphQL
        Cloudfront
        Cloudformation
            Stacks for S3, Congito, DynamoDB


```

## Firebase Backend Component Diagram

```mermaid
mindmap
    ((FireBase))
        Website Hosting
            usebetter.app
        Notifications
            Apple push notification service (APNS)
            Google push notifications
        Analytics
        Crashlytics

```