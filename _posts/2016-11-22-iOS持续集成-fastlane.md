---
layout: post
title: fastlane
categories: [工具]
tags: [工具]
description: ios持续集成
---
<h3>安装Homebrew</h3>

{% highlight ruby %}

ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

{% endhighlight %}

<h3>安装Ruby</h3>

{% highlight ruby %}

rvm list known

sudo rvm install ruby-2.1.4

{% endhighlight %}


<h3>gem源更换</h3>
<h6>显示当前源</h6>

{% highlight ruby %}

gem sources -l

{% endhighlight %}

<h6>移除当前源</h6>

{% highlight ruby %}

gem sources --remove https://rubygems.org/

{% endhighlight %}

<h6>增加当前源</h6>

{% highlight ruby %}

gem sources -a http://ruby.taobao.org/

{% endhighlight %}


<h6>更新缓存</h6>

{% highlight ruby %}

gem sources -u 

{% endhighlight %}



<h3>安装</h3>

{% highlight ruby %}

sudo gem install -n /usr/local/bin fastlane

{% endhighlight %}

<h3>Match</h3>

{% highlight ruby %}

fastlane match adhoc

{% endhighlight %}


+-----------------------+---------------------------------------------------+
|                          Summary for match 2.1.3                          |
+-----------------------+---------------------------------------------------+
| git_url               | git@gitlab.****.me:*****.**/ioscertificates.git |
| type                  | adhoc                                             |
| git_branch            | master                                            |
| keychain_name         | login.keychain                                    |
| readonly              | false                                             |
| verbose               | false                                             |
| force                 | false                                             |
| skip_confirmation     | false                                             |
| shallow_clone         | false                                             |
| force_for_new_devices | false                                             |
| skip_docs             | false                                             |
+-----------------------+---------------------------------------------------+


[10:45:30]: Cloning remote git repo...
[10:45:31]: 🔓  Successfully decrypted certificates repo
[10:45:31]: To not be asked about this value, you can specify it using 'username'
Your Apple ID Username: ****@****.com
[10:45:34]: Verifying that the certificate and profile are still valid on the Dev Portal...
[10:45:40]: To not be asked about this value, you can specify it using 'app_identifier'
The bundle identifier(s) of your app (comma-separated): com.***.*****
[10:46:21]: Couldn't find a valid code signing identity in the git repo for distribution... creating one for you now


+-------------------------------------+-----------------------------------+
|                         Summary for sigh 2.1.3                          |
+-------------------------------------+-----------------------------------+
| app_identifier                      | ***.***.****             |
| username                            | *****@****.com                   |
| force                               | true                              |
| cert_id                             | Z7PUV2FBS2                        |
| provisioning_name                   | match AdHoc ***.***.**            |
| ignore_profiles_with_different_name | true                              |
| adhoc                               | true                              |
| development                         | false                             |
| skip_install                        | false                             |
| skip_fetch_profiles                 | false                             |
| skip_certificate_verification       | false                             |
+-------------------------------------+-----------------------------------+
[10:50:50]: All required keys, certificates and provisioning profiles are installed 🙌




