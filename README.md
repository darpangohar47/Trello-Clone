# Trello Clone

A Trello-inspired task management application built using **Node.js**, **Express.js**, and **React**.

## Features

- **Authentication**: Secure login and registration.
- **Boards**: Create, edit, and delete project boards.
- **Lists**: Add multiple lists to organize tasks.
- **Cards**: Create, move, and delete cards within lists.
- **Drag-and-Drop**: Intuitive drag-and-drop interface for managing tasks.
- **Responsive Design**: Fully optimized for desktop and mobile devices.

---

## Tech Stack

### Frontend
- React.js
- CSS/SCSS 
- Drag-and-Drop library (e.g., react-beautiful-dnd)

### Backend
- Node.js
- Express.js

### Database
- MongoDB (or any other database of choice)

### Authentication
- JSON Web Tokens (JWT)

---

## Installation and Setup

   ```bash
   git clone https://github.com/darpangohar47/Trello-Clone.git
   cd trello-clone
   npm i 
   npm run dev 
   ```

Remember to setup an .env file with following variables
```
MONGO_URI
JWT_SECRET

```

## API Endpoints:

### User Registration:

Endpoint: POST /api/users/register

Description: Registers a new user.

Request Body:
{
  "name": "User Name",
  "email": "user@example.com",
  "password": "userpassword"
}

### User Login:

Endpoint: POST /api/users/login

Description: Authenticates a user and returns a JWT token.

Request Body:
{
  "email": "user@example.com",
  "password": "userpassword"
}

### Create Board:

Endpoint: POST /api/boards

Description: Creates a new board.

Request Body:
{
  "title": "Board Title",
  "description": "Board Description"
}

### Get Boards:

Endpoint: GET /api/boards

Description: Retrieves all boards for the authenticated user.


### Create List:

Endpoint: POST /api/lists

Description: Adds a new list to a board.

Request Body:
{
  "boardId": "board_id",
  "title": "List Title"
}
### Create Card:

Endpoint: POST /api/cards

Description: Adds a new card to a list.

Request Body:
{
  "listId": "list_id",
  "title": "Card Title",
  "description": "Card Description"
}
### Move Card:

Endpoint: PUT /api/cards/move

Description: Moves a card to a different list or position.

Request Body:
{
  "cardId": "card_id",
  "targetListId": "target_list_id",
  "position": new_position
}
### Delete Card:

Endpoint: DELETE /api/cards/:id

Description: Deletes a card by its ID.



**Note**: Ensure that all API requests include the appropriate authentication headers with the JWT token obtained during login.
