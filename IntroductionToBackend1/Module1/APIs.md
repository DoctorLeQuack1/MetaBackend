# API Notes

## Introduction

*   We interact with information daily via phones (news, purchases, social media).
*   Websites and apps often use APIs (Application Programming Interfaces).
*   APIs are developer-friendly, accessible, and valuable development tools.

## What is an API?

*   API stands for Application Programming Interface.
*   A set of functions and procedures for creating applications that access features or data of an operating system, application, or other service.
*   The term "API" is intentionally broad to cover many applications and use cases.
*   Web developers frequently work with APIs.

## Types of APIs

*   **Browser/Web APIs:** Built into the browser, extending its functionality.
    *   Examples:
        *   DOM API: Turns HTML into a tree of JavaScript objects.
        *   Geolocation API: Returns browser location coordinates.
        *   Fetch API: For fetching data.
        *   Canvas API: For drawing graphics.
        *   History API: For managing browser history.
        *   Web Storage API: For client-side storage.
*   **RESTful/REST APIs:** Provide data for web and mobile apps (also called web servers).
    *   REST (Representational State Transfer): Principles for building efficient APIs.
    *   Responsibilities: Sending and receiving data to/from a centralized database.
    *   Can query own or third-party REST APIs.
*   **Sensor-Based APIs:** Basis of the Internet of Things (IoT).
    *   Interconnected physical sensors communicating via APIs.
    *   Track and respond to physical data.
    *   Examples: Philips Hue, smart lights, node bots.

## REST API Details

*   Most common data API for web developers.
*   Acts as a data backbone for web clients (web pages, mobile apps).
*   Key operations:
    *   GET (Get data)
    *   POST (Create data)
    *   PUT (Update data)
    *   DELETE (Delete data)
*   Uses REST principles and good design practices for discoverable interfaces.
*   **Endpoints:** Specify how resources are accessed (part of the URL).
*   After hitting an endpoint, the API performs server-side processing to build a response.
*   Common response formats:
    *   Full web pages
    *   JSON (JavaScript Object Notation) data format

## Summary

*   APIs extend system capabilities and act as bridges between components.
*   Web developers frequently work with various types of APIs, especially REST APIs.