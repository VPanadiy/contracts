# contracts
An isolated SCM repository for SCC Contracts

##### To test Consumer Driven Contracts in the Open API 3.0 Specification for Spring Cloud Contract run: 
- maven: `mvn clean install -DcontractsRepositoryUsername=yourGitName -DcontractsRepositoryPassword=yourGitPassword`
- gradle: `gradle build`


##### How to update stubs?
- maven: `mvn clean package -DskipTests -Dstubrunner.properties.git.username=USER -Dstubrunner.properties.git
.password=PASSWORD`
-gradle: `gradlew pushStubsToScm`

#### Push contracts to Git repository wit Gradle
1.In contract-rest-service add username and password to the git account

2.Create jar archive of the project
- run: `gradle build -x test`

3.Publish to local maven storage
- run: `gradle install`

4.Push to git
- run: `gradle publishStubsToScm`
