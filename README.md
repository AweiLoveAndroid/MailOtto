# MailOtto v1.0.2
A mail box.

[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/drakeet/MailOtto/blob/master/LICENSE)
![SDK](https://img.shields.io/badge/SDK-9%2B-orange.svg)
![maven-central](https://img.shields.io/maven-central/v/me.drakeet.mailotto/mailotto.svg) 

### Usage

```groovy
compile 'me.drakeet.mailotto:mailotto:1.0.2'
```

Mail
----

```java
public class Mail {

    public Class<?> from;
    public Class<?> to;
    public Object content;


    public Mail(Object content, Class<?> to) {
        this(content, to, null);
    }


    public Mail(Object content, Class<?> to, Class<?> from) {
        this.to = to;
        this.from = from;
        this.content = content;
    }
}
```

Post mails
----------

```java
Mailbox.getInstance().post(mail);
```

AtHome, and the postman will give you the mails.
------------------------------------------------

```java
Mailbox.getInstance().atHome(this);
```

When received a mail
--------------------

```java
@OnMailReceived public void onDearMailReceived(Mail mail) {
    Toast.makeText(ConsumerActivity.this, 
                   mail.content.toString(), 
                   Toast.LENGTH_SHORT).show();
}
```

Leave
-----

```java
Mailbox.getInstance().leave(this);
```


Sample
------

There is an example of using MailOtto to do pre loading. It is very suitable for pre loading, nice lol.

这是一个使用 MailOtto 做预加载的示例。它非常适合做预加载，很棒 lol. 相关文章：[使用 MailOtto 做完美预加载](https://drakeet.me/mailotto-sample)

https://github.com/drakeet/MailOtto/tree/master/sample/src/main/java/me/drakeet/mailotto/demo

https://github.com/drakeet/MailOtto/releases


Thanks
------

[square/otto](https://github.com/square/otto)


Changelog
---------

v1.0.2
- Remove the `<application ../>` of `library/src/main/AndroidManifest.xml`.

License
-------

    Copyright 2016 drakeet.
    Copyright 2012 Square, Inc.
    Copyright 2010 Google, Inc.

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.



 [1]: http://square.github.com/otto/
 [2]: http://github.com/square/otto/downloads
 [snap]: https://oss.sonatype.org/content/repositories/snapshots/