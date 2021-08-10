# Architecture

## Why does architecture matter?

A poorly architected app may have all of its logic contained within a single method that consists of many lines; or it may have one large class with too many responsibilities. Both of these scenarios make it impossible to test groups or units of logic independently.

Apps that are architected for testing separate their code into groups of logic using multiple methods and classes to collaborate. With this type of architecture, developers can test each public method and class in isolation.