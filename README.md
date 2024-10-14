# Micro-Reddit

This project is part of The Odin Project: [Micro-Reddit](https://www.theodinproject.com/lessons/ruby-on-rails-micro-reddit#project-micro-reddit)

## Overview

Micro-Reddit is a simplified version of Reddit, designed to support link submissions and commenting.

## Lesson Objectives

1. Data Modeling
    - Design and implement data models for users, posts, and comments.
    - Understand relationships between models (User, Post, Comment).

2. Rails Setup
    - Generate a new Rails application and set up SQLite3 as the database.
    - Create and run migrations to establish database structure.

3. Validations
    - Implement and test model validations for User, Post, and Comment.
    - Ensure data integrity by preventing invalid records from being saved.

4. Associations
    - Establish associations between models (e.g., User has many Posts, Post has many Comments).
    - Test associations in the Rails console to verify functionality.

5. Console Usage
    - Familiarize with Rails console commands for testing models and relationships.
    - Use console to create, validate, and manipulate records interactively.

6. Commenting System
    - Develop a commenting feature that links users to their comments on posts.
    - Implement necessary validations and associations for comments.
  
## Outcome

- Gain practical experience in building and managing a Rails application with core functionalities, focusing on backend development and data management.

## Getting Started

### Prerequisites

- **Ruby**: 3.3.4
- **Rails**: 7.2.1
- **Database**: SQLite3 (default)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/jambalong/micro-reddit.git
   cd micro-reddit
   ```

2. Install dependencies:
   ```bash
   bundle install
   ```

3. Create and migrate the database:
   ```bash
   rails db:create
   rails db:migrate
   ```

4. Start the Rails server:
   ```bash
   rails server
   ```

### Usage

[Detailed prior setup](https://www.theodinproject.com/lessons/ruby-on-rails-micro-reddit#project-micro-reddit) is described in the project in order to get to this stage.

Add the associations you need between users, posts, and comments. You’ll need to be able to do the following methods successfully from the console (assuming your second user has an ID of 2):

1. `u2 = User.find(2)`
2. `c1 = u2.comments.first` should return that user’s comment. `#comments` returns an array with comments, which is why we need to use `#first` to actually retrieve the comment itself.
3. `c1.user` should return that comment’s author User (`u2`).
4. `p1 = Post.first`
5. `p1.comments.first` should return the comment `c1`.
6. `c1.post` should return the post `p1`.

If any of those don’t work, double check your associations. Sometimes the error messages can be helpful in prompting you for how to set up those associations.
