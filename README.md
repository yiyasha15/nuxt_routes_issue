# route_testing

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

BACKEND json server
1. cd json-server-lib
2. json-server --watch user.json --p 3001
For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).

ISSUE!!
1. Navigate to the user card.
2. The _id page is the parent component and I'm sending the 'user' object to the 'work' component.
3. Go to work page, the _id page will render below it.
How do I stop rendering the parent component below the child component? 
