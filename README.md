# LandsAPI - Integrate Lands into your Plugin
[![](https://jitpack.io/v/Angeschossen/LandsAPI.svg)](https://jitpack.io/#Angeschossen/LandsAPI)


How to include the API with Maven: 
```xml
<repositories>
	<repository>
		<id>jitpack.io</id>
		<url>https://jitpack.io</url>
	</repository>
</repositories>

<dependencies>
    <dependency>
        <groupId>com.github.Angeschossen</groupId>
        <artifactId>LandsAPI</artifactId>
        <version>4.3.3.0</version>
        <scope>provided</scope>
    </dependency>
</dependencies>
```

How to include the API with Gradle:
```groovy
repositories {
	maven { url 'https://jitpack.io' }
}
dependencies {
    compileOnly "com.github.Angeschossen:LandsAPI:4.3.3.0"
}
```


You can also download the jar file from here: https://github.com/Angeschossen/LandsAPI/releases


## Implementing Lands
Examble:

```public class IntegrationExample {

    private final LandsIntegration landsAddon;

    private IntegrationExample(Plugin yourPlugin) {

        /*
        Initialize LandsAddon
        Set isPulic to false, if you want
        to prevent that other developers can
        access your addon.
         */
        landsAddon = new LandsIntegration(yourPlugin, false);
    }

    //Just a test
    private void test(Location location) {
        final LandChunk landChunk = landsAddon.getLandChunk(location);
        //Do some stuff.
    }
}
```
