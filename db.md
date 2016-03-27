## Database Questions

* Design a database schema for Facebook, with at least 4 models, a complete set of attributes for each model, a 1:M association, and a M:M association.

Users
+ User id
+ Password
+ user name
+ M:M relationship with posts

Posts
+ Post id
+ M:M relationship with users

joinedTable: usersposts
+post id
+ user id

Likes
+ Like id
+ 1:M relationship with Posts

Friends
+ Friend id
+ 1:M relationship with users
	-confused here because a user and a friend are basically the same thing becuase a friend is techincally a user, so how can it have a relationship with itself?