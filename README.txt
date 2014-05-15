
An Vaadin Touchkit example project for android.

- Create the unsigned apk
$ mvn clean package

- Generate key
$ keytool -genkey -v -keystore touchkit-demo.ks -alias touchkit-demo -keyalg RSA -keysize 2048 -validity 10000

  Default pass (edit pom.xml)
   <storepass>touchkit-demo</storepass>
   <keypass>touchkit-demo</keypass>

- Create the signed apk, after generating the above key run:
$ mvn clean package -Psign

