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


### LINKS
https://cloud.spring.io/spring-cloud-contract/single/spring-cloud-contract.html#_producer_side_fraud_detection_server

http://cloud-samples.spring.io/spring-cloud-contract-samples/tutorials/contracts_external.html

https://github.com/spring-cloud/spring-cloud-contract/blob/master/docs/src/main/asciidoc/verifier_setup.adoc#gradle-project

https://github.com/spring-cloud/spring-cloud-contract/blob/ea65ae355369d37b1fe56fd118a0e1ceef67eba4/docs/src/main/asciidoc/verifier_faq.adoc
