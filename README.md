![CF](https://camo.githubusercontent.com/70edab54bba80edb7493cad3135e9606781cbb6b/687474703a2f2f692e696d6775722e636f6d2f377635415363382e706e67) 14: Mongo/Express 2 Resource API
===


## Links -
* Github - https://github.com/khalahm253/14-relationship-modeling
* Heroku - https://lab-14-khalil.herokuapp.com/
* Travis -  https://travis-ci.com/khalahm253/14-relationship-modeling


## Server Endpoints
### `/api/resource-name`
* `POST` request
  * should pass data as stringifed JSON in the body of a post request to create a new resource

### `/api/resource-name/:id`
* `GET` request
  * should pass the id of a resource through the url endpoint to get a resource
    * **this should use `req.params`, not querystring parameters**
* `PUT` request
  * should pass data as stringifed JSON in the body of a put request to update a pre-existing resource
* `DELETE` request
  * should pass the id of a resource though the url endpoint to delete a resource
    

#### Feature Tasks
  * continue working on the `express` and `mongoDB` REST API that you started yesterday
  * include an additional resource that contains a "relationship" to the single resource that has already been created
  * create `GET`, `POST`, `PUT`, and `DELETE` routes for your newly added resource
  * test your application to ensure that it meets the standard criteria of a working **full CRUD** REST API
  * use `populate` in the `get()` route logic your  `/api/new-resource-name/:id` route to populate the associated property used to house related resources **(ex: `List.findById(req.params.id).populate('notes')`)**
### Tests

 * `GET` - test 200, returns a resource with a valid body
 * `GET` - test 404, respond with 'not found' for valid requests made with an id that was not found
 * `PUT` - test 200, returns a resource with an updated body
 * `PUT` - test 400, responds with 'bad request' if no request body was provided
 * `PUT` - test 404, responds with 'not found' for valid requests made with an id that was not found
 * `POST` - test 400, responds with 'bad request' if no request body was provided
 * `POST` - test 200, returns a resource for requests made with a valid body



