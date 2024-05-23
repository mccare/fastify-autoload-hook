# Example to demonstrate an issue in fastify-autoload 5.8.2

Autoload from 5.8.0 -> 5.8.2 produces an error in the current repository by flagging a route as being already
registered and therefore duplicate.

To reproduce:
* npm install
* npm run dev
=> this will produce an error `FastifyError [Error]: Method 'GET' already declared for route '/backend'`

change autoload to 5.8.0 and run the steps again and the error will disappear