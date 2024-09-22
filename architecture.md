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
        Data Models
            User Feed
                Use Cache
            Friends Feed
                Friends Cache
        Database Models
            User Table Model
            Friends Map Table Model
            Transaction Table Model
            License Table Model

        Screens
            Login Page
            Home Page
            Add item
            Your Items
            Profile
            Manage Friends

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
            Event Table
            License Table

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

## DynamoDB Table map
```mermaid
mindmap
    ((AWS DynamoDB))
        UserInfo Table
            Email
            UserId
            IdentityId
            DisplayName
            FCMToken                
        FriendsMap Table
            user Id
            Friend Id
            Circle Name
        Event Table
            Item Id
            Owner Id
            Receiver Id
            State
        License Table
            user Id
            License state
            License type
            startedOn
            expiredOn
            OS_Type
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
            Page Visits
            Button Clicks
            Sign In
            Sign up
            Custom Events
        Crashlytics

```