## OpenStack Enabled Fork of SimianArmy

Using code from this fork:
https://github.com/ssbanerje/SimianArmy

I was able to modify NetFlix's SimianArmy Chaos Monkey to work on an OpenStack Cloud.

Ssbanerje tried to get his code merged with the upstream branch but it wasn't acknowledged.

I made these changes to his code

-Updated jclouds for Gradle
-Disabled the other monkeys.  Just disabling them in properties wasn't enough, I had to disable them in the java code
-Took out Cinder 1.0 references because it has been deprecated by jclouds
-Added the ssh lines commented out here src/main/resources/chaos.properties
-Enabled the lines that work for Openstack in all properties files and disabled the ones that don't
-Monkey's are left leashed but I turned up the frequency that they run and enabled MonkeyTime at all hours of the day

## Netflix SimianArmy Description

The Simian Army is a suite of tools for keeping your cloud operating in top form.  Chaos Monkey, the first member, is a resiliency tool that
helps ensure that your applications can tolerate random instance failures

## CloudBees build status
[![Build Status](https://netflixoss.ci.cloudbees.com/job/SimianArmy-master/badge/icon)](https://netflixoss.ci.cloudbees.com/job/SimianArmy-master/)

## DETAILS

Please see the [wiki](https://github.com/Netflix/SimianArmy/wiki).

## SUPPORT

[Simian Army Google group](http://groups.google.com/group/simianarmy-users).

## LICENSE

Copyright 2012 Netflix, Inc.

Licensed under the Apache License, Version 2.0 (the “License”); you may not use this file except in
compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0
Unless required by applicable law or agreed to in writing, software distributed under the License is
distributed on an “AS IS” BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
implied. See the License for the specific language governing permissions and limitations under the
License.
