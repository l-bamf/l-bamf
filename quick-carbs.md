# Quick Carbs Project Documentation

This markdown file is a loose documentation of my experiences working on this project. What I have learnt and accomplished.

## Project Basics

### Goal

In Australia alcoholic drinks are exempt from displaying the nutritional content on the can or bottle unlike other, non-alcoholic, drinks.
This information is accessible online through the manufacturers themselves and third party websites such as [CalorieKing](https://www.calorieking.com/au/en/), but this is a relatively slow process with many irrelevant details the user doesn't need. My goal is to make the user experience quicker, and with less overhead.

### Specs 

| Field | Value(s) |
| ----- | ----- |
| Involved Languages | Kotlin, XML, Groovy |
| Involved Technologies/Toolkits | Android Studio, CameraX, Firebase |
| Version Control | GitHub, TortosieGit |
| Architectures | MVVM, Repositories |
| Android Navigation | State Machine |

# Architectural Decisions

At a very high level, I decided to develop a native mobile application because my main use-case is:

> As a customer, I want to find the nutritional information of a drink while in the store, so I can decide if I want to buy it.

## Navigation

In my last project I developed an Android application using a State Machine architecture. This worked adequately but, as a main goal of this project, I wanted to 
learn different ways of developing and so I investigated the [Android Navigation Component](https://developer.android.com/guide/navigation).
For a reason still unclear, the cameraX library didn't function properly when using Navigation, so I reverted back to a simple state machine architecture.