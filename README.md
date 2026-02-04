#  BeatHub Backend

## Overview

**BeatHub Backend** is a MongoDB + Mongoose schema design for a music streaming application.
It defines structured, scalable data models for managing users, artists, albums, songs, and playlists, ensuring clean relationships and efficient data handling.

This project focuses on building a **strong database foundation** that can easily scale into a full-fledged backend with APIs and authentication.

---

##  Data Models

The backend includes the following core models:

* **User** – Manages user accounts and liked songs
* **Artist** – Stores artist details, albums, and songs
* **Album** – Represents albums linked to artists
* **Song** – Stores song metadata linked to albums and artists
* **Playlist** – User-created playlists containing songs

All relationships are handled using `mongoose.Schema.Types.ObjectId` and references for easy population.

---

##  Tech Stack

* **Node.js**
* **MongoDB**
* **Mongoose**

---

##  How to Run

1. Install dependencies:

   ```bash
   npm i
   ```

2. Create a `.env` file and add your MongoDB connection string:

   ```env
   MONGO_URI=your_mongodb_connection_string
   ```

3. Seed the database:

   ```bash
   node scripts/seed.js
   ```

---

##  Project Structure

```
├── models/
│   ├── User.js
│   ├── Artist.js
│   ├── Album.js
│   ├── Song.js
│   └── Playlist.js
├── scripts/
│   └── seed.js
├── .env
├── package.json
└── README.md
```

---

##  Key Highlights

* Proper schema normalization
* Clean model relationships
* Timestamps enabled for all schemas
* Ready for `.populate()` queries
* Scalable foundation for REST APIs

---

##  Future Enhancements

* Authentication & authorization
* REST API endpoints
* Search and filtering
* Playlist collaboration
* User activity tracking