# QBit Build Parent POM

[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/Kingsrook/qbit-bom)
[![License](https://img.shields.io/badge/license-GNU%20Affero%20GPL%20v3-green.svg)](https://www.gnu.org/licenses/agpl-3.0.en.html)
[![Java](https://img.shields.io/badge/java-17+-blue.svg)](https://adoptium.net/)

> **Parent POM for QRunIO QBit Projects - Central Build Configuration**

This repository contains the **parent POM** that provides centralized build configuration, dependency management, and CI/CD settings for all QRunIO QBit projects.

## 🚀 Overview

QBit Build Parent POM is a **Maven parent POM** that standardizes the build process, dependency versions, and publishing configuration across all QBit projects in the QQQ ecosystem. It ensures consistency and reduces duplication across QBit repositories.

### What This Repository Contains

- **Build Configuration**: Standardized Maven plugin versions and configurations
- **Dependency Management**: Centralized BOM imports (QQQ, JUnit, etc.)
- **Publishing Settings**: Maven Central publishing configuration
- **Release Profile**: GPG signing and artifact publishing setup
- **Java Configuration**: Standardized Java 17+ settings

### What This Repository Does NOT Contain

- **QBit Source Code**: Individual QBit implementations
- **QQQ Core Framework**: The main QQQ framework code
- **Application Logic**: Business logic or application-specific code
- **Runtime Dependencies**: Libraries used at runtime

## 🏗️ Architecture

### Technology Stack

- **Java**: Java 17+ with UTF-8 encoding
- **Maven**: Build system with plugin management
- **GPG**: Artifact signing for Maven Central
- **Sonatype Central**: Publishing to Maven Central

### Core Dependencies Managed

- **QQQ BOM**: `com.kingsrook.qqq:qqq-bom-pom:0.27.9`
- **JUnit BOM**: `org.junit:junit-bom:5.10.0`
- **Maven Plugins**: Compiler, Source, Javadoc, GPG, Central Publishing

## 📁 Project Structure

```
qbit-bom/
├── pom.xml                    # Parent POM configuration
├── README.md                  # This documentation
├── CHANGELOG.md              # Version history
├── LICENSE                   # GNU Affero GPL v3
├── CODE_OF_CONDUCT.md        # Community guidelines
├── CONTRIBUTING.md           # Contribution guidelines
├── SECURITY.md              # Security policy
└── CODE_STYLE.md            # Coding standards
```

## 🎯 Parent POM Functionality

### What This Parent POM Provides

- **Plugin Management**: Standardized Maven plugin versions
- **Dependency Management**: Centralized BOM imports
- **Build Profiles**: Release profile for Maven Central publishing
- **Java Configuration**: Consistent Java 17+ settings
- **Publishing Setup**: GPG signing and artifact publishing
- **Encoding Standards**: UTF-8 for source and reporting

### What This Parent POM Does NOT Do

- **Provide Runtime Dependencies**: Only manages build-time dependencies
- **Include Source Code**: No Java source files
- **Define Business Logic**: No application-specific code
- **Handle Deployment**: Only handles artifact publishing

## 🚀 Getting Started

### Prerequisites

- **Java 17+** (required for QQQ features)
- **Maven 3.8+** (for build system)
- **GPG Key** (for signing artifacts in release profile)

### Using This Parent POM

Add this parent POM to your QBit project's `pom.xml`:

```xml
<parent>
    <groupId>com.kingsrook</groupId>
    <artifactId>qbit-build-parent</artifactId>
    <version>1.0.0</version>
    <relativePath/>
</parent>
```

### Example QBit Project Structure

```xml
<project>
    <parent>
        <groupId>com.kingsrook</groupId>
        <artifactId>qbit-build-parent</artifactId>
        <version>1.0.0</version>
        <relativePath/>
    </parent>
    
    <groupId>com.kingsrook.qbits</groupId>
    <artifactId>qbit-your-component</artifactId>
    <version>${revision}</version>
    
    <properties>
        <revision>0.1.0-SNAPSHOT</revision>
    </properties>
    
    <dependencies>
        <!-- Your QBit dependencies here -->
    </dependencies>
</project>
```

## 📖 Detailed Documentation

For comprehensive development information, see:
- **[QQQ Wiki](https://github.com/Kingsrook/qqq.wiki)** - Complete QQQ framework documentation
- **[QBit Development](https://github.com/Kingsrook/qqq.wiki/QBit-Development)** - QBit development guide

## 🔧 Configuration

### Build Configuration

This parent POM provides:

- **Java 17+**: Source and target Java version
- **UTF-8 Encoding**: Source and reporting encoding
- **Plugin Management**: Standardized plugin versions
- **Release Profile**: Maven Central publishing setup

### Publishing Configuration

The release profile includes:

- **Source JAR**: Automatic source artifact generation
- **Javadoc JAR**: Documentation artifact generation
- **GPG Signing**: Artifact signing for Maven Central
- **Central Publishing**: Direct publishing to Maven Central

## 🧪 Testing

### Running Tests

```bash
# Run all tests
mvn test

# Run tests with coverage
mvn test jacoco:report

# Run specific test class
mvn test -Dtest=YourTestClass
```

### Test Configuration

- **JUnit 5**: Managed via JUnit BOM
- **AssertJ**: Available for fluent assertions
- **H2 Database**: Available for testing

## 📦 Building for Production

### Development Build

```bash
mvn clean install
```

### Release Build

```bash
mvn clean deploy -Prelease
```

The release profile:
- Generates source and javadoc JARs
- Signs artifacts with GPG
- Publishes to Maven Central

## 🔐 Security Considerations

### Artifact Signing

- **GPG Signing**: All release artifacts are signed
- **Maven Central**: Signed artifacts published to Maven Central
- **Key Management**: GPG key configuration required

### Best Practices

- **Dependency Management**: Use BOMs for version consistency
- **Plugin Versions**: Keep plugin versions up to date
- **Security Updates**: Regularly update dependency versions

## 🤝 Contributing

**Important**: This repository is a component of the QQQ framework. All contributions, issues, and discussions should go through the main QQQ repository.

### Development Workflow

1. **Fork the main QQQ repository**: https://github.com/Kingsrook/qqq
2. **Create a feature branch**: `git checkout -b feature/amazing-feature`
3. **Make your changes** (including parent POM changes if applicable)
4. **Run tests**: `mvn test`
5. **Commit your changes**: `git commit -m 'Add amazing feature'`
6. **Push to the branch**: `git push origin feature/amazing-feature`
7. **Open a Pull Request** to the main QQQ repository

### Code Standards

- **Maven**: Follow Maven best practices
- **Documentation**: Update relevant documentation
- **Versioning**: Follow semantic versioning

## 📄 License

This project is licensed under the GNU Affero General Public License v3.0 - see the [LICENSE](LICENSE) file for details.

```
QBit Build Parent POM
Copyright (C) 2021-2024 Kingsrook, LLC
651 N Broad St Ste 205 # 6917 | Middletown DE 19709 | United States
contact@kingsrook.com | https://github.com/Kingsrook/
```

**Note**: This is a component of the QQQ framework. For the complete license and more information, see the main QQQ repository: https://github.com/Kingsrook/qqq

## 🆘 Support & Community

### ⚠️ Important: Use Main QQQ Repository

**All support, issues, discussions, and community interactions should go through the main QQQ repository:**

- **Main Repository**: https://github.com/Kingsrook/qqq
- **Issues**: https://github.com/Kingsrook/qqq/issues
- **Discussions**: https://github.com/Kingsrook/qqq/discussions
- **Wiki**: https://github.com/Kingsrook/qqq.wiki

### Why This Repository Exists

This repository is maintained separately from the main QQQ repository to:
- **Enable independent parent POM development** and versioning
- **Allow QBit-specific CI/CD** and deployment pipelines
- **Provide clear separation** between build configuration and core framework concerns
- **Support different release cycles** for parent POM vs. core framework

### Getting Help

- **Documentation**: Check the [QQQ Wiki](https://github.com/Kingsrook/qqq.wiki)
- **Issues**: Report bugs and feature requests on [Main QQQ Issues](https://github.com/Kingsrook/qqq/issues)
- **Discussions**: Join community discussions on [Main QQQ Discussions](https://github.com/Kingsrook/qqq/discussions)
- **Questions**: Ask questions in the main QQQ repository

### Contact Information

- **Company**: Kingsrook, LLC
- **Email**: contact@kingsrook.com
- **Website**: https://kingsrook.com
- **Main GitHub**: https://github.com/Kingsrook/qqq

## 🙏 Acknowledgments

- **QQQ Framework Team**: For the underlying low-code platform
- **Maven Community**: For the robust build system
- **Open Source Community**: For the tools and libraries that make this possible

---

**Built with ❤️ by the Kingsrook Team**

**This is a parent POM component of the QQQ framework. For complete information, support, and community, visit: https://github.com/Kingsrook/qqq**