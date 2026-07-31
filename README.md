<img src="https://elytrium.net/src/img/elytrium.webp" alt="Elytrium" align="right">

# LimboAPI

Library for sending players to virtual servers (called limbo)

## See also

- [LimboAuth-CTD](https://github.com/lis0/LimboAuth-VelocityCTD) - Auth System built in virtual server (Limbo). Uses BCrypt, has TOTP 2FA feature. Supports literally any database due to OrmLite.
- [LimboFilter](https://github.com/Elytrium/LimboFilter) - Most powerful bot filtering solution for Minecraft proxies. Built with LimboAPI. (not sure if it works with Velocity-CTD)

## Features of LimboAPI

- Send to the Limbo server during login process
- Send to the Limbo server during play process
- Send maps, items to player's virtual inventory
- Display player's XP
- Send Title, Chat, ActionBar
- Load world from world files like .schematic
- and more...

## How to

- Include ``limboapi-api`` to your Maven/Gradle project as compile-only
- Subscribe to ``LoginLimboRegisterEvent`` to send players to the Limbo server during login process
- Use ``LimboFactory`` to send players to the Limbo server during play process

## How to include it

#### Setup your project via adding our maven repository to your pom.xml or build.gradle file.

- Maven:

```xml
    <repositories>
        <repository>
            <id>elytrium-repo</id>
            <url>https://maven.elytrium.net/repo/</url>
        </repository>
    </repositories>

    <dependencies>
        <dependency>
            <groupId>net.elytrium.limboapi</groupId>
            <artifactId>api</artifactId>
            <version>1.1.26</version>
            <scope>provided</scope>
        </dependency>
    </dependencies>
```

- Gradle:

```groovy
    repositories {
        maven {
            setName("elytrium-repo")
            setUrl("https://maven.elytrium.net/repo/")
        }
    }

    dependencies {
        compileOnly("net.elytrium.limboapi:api:1.1.26")
    }
```

## Used Open Source projects

- [ProtocolSupport](https://github.com/ProtocolSupport/ProtocolSupport) - for modern->legacy block mappings
- [ViaVersion](https://github.com/ViaVersion/ViaVersion) - for modern string->integer block mappings

## Demo

- [LimboAuth](https://github.com/Elytrium/LimboAuth) - The auth plugin, that uses LimboAPI as a dependency at the basic level.
- [LimboFilter](https://github.com/Elytrium/LimboFilter) - The antibot solution, that uses LimboAPI as a dependency, using almost all available API methods, like Low-level Minecraft packet control.

## License & Attribution
This project is a fork of LimboAPI created by Elytrium.
* Original Work Copyright (c) Elytrium
* Fork Modifications Copyright (c) 2026 lis0

Licensed under the GNU Affero General Public License v3.0 (AGPL-3.0).