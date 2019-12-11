# Read Me

=====================
Knock Authentication
=====================
gem 'knock'
gem 'jwt'

============================
Knock install
============================
rails generate knock:install
rails generate knock:token_controller user

============================
User
============================
rails g scaffold user

============================
Add to Application controller
============================
include Knock::Authenticable

============================
Add to user_token_controller
============================
skip_before_action :verify_authenticity_token

To post new user

```javascript
{
 "user":{
  /* user data here */
 }
}
```

To Login

```javascript
{
 "auth":{
  /* user data here */
 }
}
```
