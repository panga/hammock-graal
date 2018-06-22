# Hammock GraalVM Native

## Build using Weld

`mvn clean package`

`$GRAALVM_HOME/bin/native-image --verbose --no-server --static -H:+ReportUnsupportedElementsAtRuntime -H:ReflectionConfigurationFiles=reflection.json -H:SubstitutionFiles=substitutions.json -H:IncludeResources="META-INF/.*" -cp "target/dependency/*" ws.ament.hammock.Bootstrap`

## Build using OpenWebBeans

`mvn clean package -Powb`

`$GRAALVM_HOME/bin/native-image --verbose --no-server --static -H:+ReportUnsupportedElementsAtRuntime -H:ReflectionConfigurationFiles=reflection-owb.json -H:SubstitutionFiles=substitutions.json -H:IncludeResources="META-INF/.*" -cp "target/dependency/*" ws.ament.hammock.Bootstrap`