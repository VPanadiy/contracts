# Build project
1. Move to project folder
2. Build a Docker Image with Maven: `mvnw install dockerfile:build`
3. To start project run (from docker daemon): `docker-compose up` 
4. Open project in browser `http://127.0.0.1:8080`.
    * Get ip address from docker toolbox run: `docker-machine ip` 
    
##### Swagger
To open swagger doc open url: `http://localhost:8080/swagger-ui.html`

Springfox Reference Documentation: `https://springfox.github.io/springfox/docs/current/`

Use mapping annotations closer to the method declaration. For example:

--- For controllers ---
```
@Api(tags="Person Controller", description = "Operation with entity person")
@RestController
@RequestMapping(path = URL_API)
public class PersonController { }
```

--- For methods ---
```
@ApiOperation(value = "Get person by id",
		notes = "If a person exist, it will be returned")
@GetMapping(URL_PERSON + "/{id}")
public Optional<Person> findPersonById(@PathVariable("id") Long id) { }
```


Annotation examples: 

- To change name and set description to controller use:
`@Api(tags="Person Controller", description = "Operation with entity person")`,
where `tags` - change name, `description` - set description

- Set short and full description to method: 
`	@ApiOperation(value = "Get person by id", 
 			notes = "If a person exist, it will be returned")`,
 where `value` - set short description, `notes` - full description