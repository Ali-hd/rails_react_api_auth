# Read Me

## Knock Authentication

---

`gem 'knock'`
`gem 'jwt'`

## Knock install

---

`rails generate knock:install`
`rails generate knock:token_controller user`

# create Users

---

`rails g scaffold user`

## Add to application_controller.rb

---

`include Knock::Authenticable`

## Add to user_token_controller.rb

---

`skip_before_action :verify_authenticity_token`

## To post new user

---

```javascript
{
 "user":{
  /* user data here */
 }
}
```

## To Login

---

```javascript
{
 "auth":{
  /* user data here */
 }
}
```
