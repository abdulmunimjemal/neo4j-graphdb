# SocialNetworkApp - GraphDB

## Overview
`SocialNetworkApp` is a Python class for managing a social network via a Neo4j graph database, supporting user registration, friendships, group interactions, and social engagements like posts and comments.

## Features
- **User Management**: Register, update, and manage users.
- **Relationships**: Handle friend requests, acceptances, and group memberships.
- **Posts**: Users can create, like, and comment on posts.
- **Recommendations & Searching**: Suggest friends and search for users by name.

## Installation
Ensure Neo4j is installed. Set up the Python environment with required packages:
```bash
pip install neo4j python-dotenv
```

## Usage
Initialize and use the class to manage users and interactions:

```python
app = SocialNetworkApp(os.getenv("NEO_URI"), os.getenv("NEO_USERNAME"), os.getenv("NEO_PASSWORD"))
app.register_user("1", "Abeba", 30, "Jimma", ["Reading"])
app.send_friend_request("1", "2")
app.create_post("1", "Enjoying the sunny weather!", "2024-06-05T14:00:00")
app.close()
```
