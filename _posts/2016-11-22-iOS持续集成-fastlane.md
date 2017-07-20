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

<h3>查看fastlane版本</h3>

{% highlight ruby %}

fastlane --version

{% endhighlight %}


<h3>Match</h3>

{% highlight ruby %}

fastlane match adhoc

{% endhighlight %}

<p>+-----------------------+---------------------------------------------------+</p>
<p>|                          Summary for match 2.1.3                          |</p>
<p>+-----------------------+---------------------------------------------------+</p>
<p>| git_url               | git@gitlab.****.me:*****.**/ioscertificates.git |</p>
<p>| type                  | adhoc                                             |</p>
<p>| git_branch            | master                                            |</p>
<p>| keychain_name         | login.keychain                                    |</p>
<p>| readonly              | false                                             |</p>
<p>| verbose               | false                                             |</p>
<p>| force                 | false                                             |</p>
<p>| skip_confirmation     | false                                             |</p>
<p>| shallow_clone         | false                                             |</p>
<p>| force_for_new_devices | false                                             |</p>
<p>| skip_docs             | false                                             |</p>
<p>+-----------------------+---------------------------------------------------+</p>


<p>[10:45:30]: Cloning remote git repo...</p>
<p>[10:45:31]: 🔓  Successfully decrypted certificates repo</p>
<p>[10:45:31]: To not be asked about this value, you can specify it using 'username'</p>
<p>Your Apple ID Username: ****@****.com</p>
<p>[10:45:34]: Verifying that the certificate and profile are still valid on the Dev Portal...</p>
<p>[10:45:40]: To not be asked about this value, you can specify it using 'app_identifier'</p>
<p>The bundle identifier(s) of your app (comma-separated): com.***.*****</p>
<p>[10:46:21]: Couldn't find a valid code signing identity in the git repo for distribution... creating one for you now</p>


<p>+-------------------------------------+-----------------------------------+</p>
<p>|                         Summary for sigh 2.1.3                          |</p>
<p>+-------------------------------------+-----------------------------------+</p>
<p>| app_identifier                      | ***.***.****             |</p>
<p>| username                            | *****@****.com                   |</p>
<p>| force                               | true                              |</p>
<p>| cert_id                             | Z7PUV2FBS2                        |</p>
<p>| provisioning_name                   | match AdHoc ***.***.**            |</p>
<p>| ignore_profiles_with_different_name | true                              |</p>
<p>| adhoc                               | true                              |</p>
<p>| development                         | false                             |</p>
<p>| skip_install                        | false                             |</p>
<p>| skip_fetch_profiles                 | false                             |</p>
<p>| skip_certificate_verification       | false                             |</p>
<p>+-------------------------------------+-----------------------------------+</p>
<p>[10:50:50]: All required keys, certificates and provisioning profiles are installed 🙌</p>
