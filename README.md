# General
This repo can be used to verify Kafka certificates without consuming any messages as such. It can also help identifying which all topics these certificates can access.

In order to run the example after importing it in Anypoint Studio, you will need to :
1. Update the global.xml for the global properties "mule.env" and "mule.encryptionKey" as applicable.
2. Add Kafka truststore and keystore in the "certs" folder under src\main\resources. Naming conventions to match as in the tls-context global element.
3. Update keystore and trustore password in the secureConfig folder's files.
4. Test the configuration by using "Test Connection" button on the kafka-consumer global element. If the configuration was correct, you will see a success message.
5. Additionally, if you want to check which all topics these certificates have access to , you can start this application and in the logs search for the string "topicId". There will be multiple occurrences of this string in only one of the logs. Before the "topicId", it will display "name" of the topic.