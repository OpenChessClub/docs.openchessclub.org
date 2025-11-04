---
title: Getting Started
nav_order: 2
---

To run OpenChessClub locally or self-host your own instance, you’ll need a few dependencies installed and a MongoDB connection string for your database.

## Installations

Before you begin, make sure you have:

- [Git](https://git-scm.com/install/windows)
- [Node.js](https://nodejs.org/en) v18 or higher installed
- [MongoDB connection URI](https://www.mongodb.com/lp/cloud/atlas)

OpenChessClub uses MongoDB to store players, games, and club data. You can: 1. Use a local MongoDB instance (`mongodb://127.0.0.1:27017/openchessclub`) 2. Or use a hosted MongoDB service such as [MongoDB Atlas](https://www.mongodb.com/lp/cloud/atlas) (recommended).

If you've got the required software installed, setting up is easy.

## Setting Environment Variables

Currently, there are only three environment variables needed, which hopefully makes the setup process easy.

```
MONGO_URI=
SESSION_SECRET=
NODE_ENV=
```

As the project grows, I'm sure that list will become rather large, but for now, this is all.

## Running The Project

After you've set your environment variables, the next step is to get the project up and running. To do that, it's as simple as running `npm i`, waiting for the dependencies to install and then `npm run dev`. You should now be able to navigate to `localhost:3000` to see the dashboard.

## Creating a user

Since this software should only ever have 1 or 2 users, there's no need for a signup page. However, setting up a user account is incredibly easy. In the root of the project, you'll find a `scripts` folder. Therein, you'll find `createUser.js`. Simply run this script when you're ready to create your user account: `node createUser.js`. Follow the prompts, and that's it. You'll now have an admin account that you can now login with.