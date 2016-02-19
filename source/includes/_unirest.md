# Unirest

```shell
  # Unix comes with cURL - nothing to do here!
```

```ruby
# For ruby, simply install the gem with
gem install unirest
# or in Gemfile
gem 'unirest'

# and require
require 'unirest'
```

```php
<?php
  // You can install with composer by adding the following to your composer.json:
  {
    "require-dev": {
      "mashape/unirest-php": "2.*"
    }
  }

  // Or by running
  composer require mashape/unirest-php

  // And require the autoloader
  require_once 'vendor/autoload.php';

  // If you don't have composer, you can clone the git repo:
  git clone git@github.com:Mashape/unirest-php.git

  // And require Unirest.php
  require_once "/path/to/unirest-php/src/Unirest.php";
?>
```

```python
# Install unirest using pip
pip install unirest

# And import the library
import unirest
```

```javascript
// Install unirest using npm
$ npm install unirest

// Then use unirest to start making requests:
var unirest = require('unirest');
```

```objective_c
// If you use CocoaPods, just add the following to your podfile, and then run
// pod install
platform :ios, '5.0'
pod 'Unirest', '~> 1.1.4'

// Now import the dependencies
#import <UNIRest.h>
```

```java
// You can install unirest with maven by including the library:
<dependency>
  <groupId>com.mashape.unirest</groupId>
  <artifactId>unirest-java</artifactId>
  <version>1.4.7</version>
</dependency>

// Alternatively, you can directly include the JAR file in the classpath:
// http://oss.sonatype.org/content/repositories/releases/com/mashape/unirest/unirest-java/1.4.7/unirest-java-1.4.7.jar
// You'll also have to install the dependencies in the classpath: (org.json, httpclient 4.3.6, httpmime 4.3.6, httpasyncclient 4.0.2)
```

> You can now start sending requests!

We recommend using Unirest to make sending http requests easier. It's the best library that we've found, but of course you can use whatever that suits you best.
