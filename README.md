# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...


* usersテーブル

  | Column             | Type                | Option                |
  | -----------------  | ------------------- | --------------------- |
  | email              | string              | NOt NULL   unique     |
  | encrypted_password | string              | NOT NULL              |
  | name               | string              | NOT NULL              |
  | profile            | text                | NOT NULL              |
  | occupation         | text                | NOT NULL              |
  | position           | text                | NOT NULL              |

  *prototypeテーブル

  | Column             | Type                | Option                |
  | -----------------  | ------------------- | --------------------- |
  | title              | string              | NOt NULL              |
  | catch_copy         | text                | NOT NULL              |
  | concept            | text                | NOT NULL              |
  | user               | references          | NOT NULL  foreign_key |

 *commentsテーブル

  | Column             | Type                | Option                |
  | -----------------  | ------------------- | --------------------- |
  | content            | text                | NOt NULL              |
  | prototype          | references          | NOT NULL foreign_key  |
  | user               | references          | NOT NULL foreign_key  |