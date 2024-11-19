# ChatRooms

## Table of Contents

1. [Overview](#Overview)
2. [Product Spec](#Product-Spec)
3. [Wireframes](#Wireframes)
4. [Schema](#Schema)

## Overview

### Description

Chatrooms is a text based chatting app that allows users to interact with one another using chatrooms. Each chatroom is identified by its topic, chats will be saved to a history relating to that specific topic.

### App Evaluation

- **Category:** Social
- **Mobile:** Mobile only, has the potential to be extended to other devices.
- **Story:**  The story my app tells is one relating to society itself. Humans build upon one another to grow and become stronger, and with common interests to talk about and bond over their collaboration unites them even further, which raises opportunities for innovation and progress.
- **Market:** Users who enjoy discussing their interests
- **Habit:** Occasional use. Whenever you have time to chat with others.
- **Scope:** Narrow, the extent of functionality is chatting, database and api integration, and the UI built around it.

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* User can set their username
* User can set their active chatroom, and fetch the recently sent messges in that chatroom
* User can send and recieve messages

**Optional Nice-to-have Stories**

* User can set their prefered language
* Any messages recieved by the user that are not in the user's prefered language will be translated to the prefered language
* User may view a list of popular existing chatrooms to choose from and enter

### 2. Screen Archetypes

- [ ] **Login Screen**
* User can log in
* User can register a new account
- [ ] **Chatroom Screen**
* User can view messages sent to that chat room
* User can send messages to the active chatroom
* User can change their active chatroom
* User can logout

### 3. Navigation

**Tab Navigation** (Tab to Screen)

- [ ] Active ChatRoom
- [ ] Recent ChatRooms

**Flow Navigation** (Screen to Screen)

- [ ] **Login Screen**
  * Leads to **Chatroom Screen** on login
- [ ] **Chatroom Screen**
  * Leads to **Login Screen** ong logout


## Wireframes

Login Screen Wireframe:
![Login Screen Wireframe Image](https://github.com/user-attachments/assets/96cf0607-1fb8-49b8-8232-96ae46af19ef)
Chatroom Screen Wireframe:
![Chatroom Screen Wireframe Image](https://github.com/user-attachments/assets/1b6b566c-3356-493a-9fe6-3af98555286a)

## Schema 

### Models

| Property | Type   | Description                                  |
|----------|--------|----------------------------------------------|
| username | String | unique id for the user post (default field) |
| password | String | user's password for login authentication |
| topic | String | key for chatroom messages database |


### Networking

- **Login Screen**
    - [GET] /user - to retrieve user data
    - [POST] /user - to add a new user
- **ChatRoom Screen**
    - [Get] /room/messages - to get the recent messages from the room
    - [POST] /room/messages - to add a message to the room from the user
