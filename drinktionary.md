# Quick Carbs Project Documentation

This markdown file is a loose documentation of my experiences working on this project. What I have learnt and accomplished.

## Project Basics

### Goal

In Australia alcoholic drinks are exempt from displaying the nutritional content on the can or bottle unlike other, non-alcoholic, drinks.
This information is accessible online through the manufacturers themselves and third party websites such as [CalorieKing](https://www.calorieking.com/au/en/), but this is a relatively slow process with many irrelevant details the user doesn't need. My goal is to make the user experience quicker, and with less overhead.

A secondary and equally important goal for me in this project is upskilling and learning different technologies. I have gone out of my way to try things I haven't done before such as developing in Kotlin
and using Firestore as an external database.

### Specs 

| Field | Value(s) |
| ----- | ----- |
| Involved Languages | Kotlin, XML, Groovy |
| Involved Technologies/Toolkits | Android Studio, CameraX, Firebase |
| Version Control | GitHub, TortosieGit |
| Architectures | MVVM, Repository |
| Android Navigation | State Machine |

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

