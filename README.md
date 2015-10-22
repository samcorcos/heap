# Heap Analytics for Meteor

What is heap? Why would you want to use it? What are some use cases? Give a few examples and probably a picture.

## Getting started

`$ meteor add samcorcos:heap`

Then you will need to create a file in your root directory named `heap.json`. At a minimum, that file will have the following code:

```json
{
  "id": ""
}
```

You will want to add your `id` to the `id` field, which will be a string of about 10 numbers.

And that's it! You now have Heap installed in your app with basic event handling.

## Advanced - Client

You can also add more specific information about your users within your `heap.json` file. 

If you have user accounts and want Heap to have access to all client-side information of your users (username, email, etc), add the following to your 'heap.json` file:

```json
{
  "id": "USER_ID",
  "client": {
    "accounts": true
  }
}
```

This package will check `Meteor.user()` and store information about your user based on the key-value pairs you supplied when you created your users.

## Advanced - Server

And if you want information about your users that is only accessible from the server (admin status, etc), you can add the following to pull in all server-side information about your users:

```json
{
  "id": "USER_ID",
  "server": {
    "accounts": true
  }
}
```
