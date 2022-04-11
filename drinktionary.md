# Drinktionary Project Documentation

This markdown file is a loose documentation of my experiences working on this project.

# Project Basics

## Current App State

The current app allows the user to successfully scan a barcode using the phone's camera, and then displays this string on another page. Firestore integration is the next goal.

## Goal

In Australia alcoholic drinks are exempt from displaying the nutritional content on the can or bottle unlike other, non-alcoholic, drinks.
This information is accessible online through the manufacturers themselves and third party websites such as [CalorieKing](https://www.calorieking.com/au/en/), but this is a relatively slow process with many irrelevant details the user doesn't need. Usability for this use-case is more important than usual, because it is likely the user will be in a social setting and a quick user experience is essential. 
My goal is to make the user experience more efficient, and with less overhead, by allowing the user to scan the barcode on a drink, to more quickly find the information.
This project is of personal importance to me because I have Type 1 Diabetes, and knowing the carbohydrate content of food and drink is essential to my short and long-term health.
The regulations let me down, so I am filling the gap myself.

A secondary and equally important goal for me in this project is upskilling and learning different technologies. I have gone out of my way to try things I haven't done before such as developing in Kotlin
and using Firestore as an external database.

## Specs 

| Field | Value(s) |
| ----- | ----- |
| Involved Languages | Kotlin, XML, Groovy |
| Involved Technologies/Toolkits | Android Studio, CameraX, Firebase |
| Version Control | GitHub, TortosieGit |
| Architectures | MVVM, Repository |
| Android Navigation | State Machine |

### Why is the repo private?

I am not as idealogical about open-source code as many people I know, so for now, for security, I'm keeping the repo private.


# Architectural Decisions

At a very high level, I decided to develop a native mobile application because my main use-case is:

> As a customer, I want to find the nutritional information of a drink while in the store, so I can decide if I want to buy it.

## AndroidOS

I decided to develop the app as an Android native because it suits my available tools. My regular phone is an iPhone but I don't have a Mac and so developing in a virtual machine is unappealing.
I chose native over a web-based app like React-native because I feel native apps lead to the best usability, and since I don't indend much UI complexity the speed of development is a lower priority.

## Navigation

In my last project I developed an Android application using a State Machine architecture. This worked adequately but, as a main goal of this project, I wanted to 
learn different ways of developing and so I investigated the [Android Navigation Component](https://developer.android.com/guide/navigation).
For a reason still unclear, the cameraX library didn't function properly when using Navigation, so I reverted back to a simple state machine architecture.

## Firestore

I have chosen to use Firestore as the external database because I have been in teams using it before, and keeping both distribution (Firebase) and storage on the same platform is appropriate.
I chose a No-SQL database type because it is simpler to get running earlier, and I don't know the final structure of my data. 
I will build the front-end of the application in such a way that changing backend implementations shouldn't be difficult if I choose to do so.
