
An Vaadin Touchkit example project for android including the widgetset and 
the code necesary for loading it from the device.

- Copy your widgetset to assets/www/VAADIN

- Set your widgetset name in assets/www/index.html

- Set the url of your app in assets/www/index.html

- Create the unsigned apk
$ mvn clean package

- Generate key (you have to do this once)
$ keytool -genkey -v -keystore touchkit-demo.ks -alias touchkit-demo -keyalg RSA -keysize 2048 -validity 10000

  Default pass (edit pom.xml)
   <storepass>touchkit-demo</storepass>
   <keypass>touchkit-demo</keypass>

- Create the signed apk, after generating the above key run:
$ mvn clean package -Psign

