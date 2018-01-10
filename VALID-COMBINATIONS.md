# Introduction
There are quiet a few variables and combinations possible. This is an attempt
to explain what combinations are valid. You can also review the options in
vars/main.yml, and all tests are described in molecule/defaults/playbook.yml.

# OpenJDK

distribution = ansible_distribution
release = ansible_distribution_major_version

|distribution|release     |java_version|java_type  |
|------------|------------|------------|-----------|
| CentOS     | 6 & 7      | 6, 7 & 8   | jre & jdk |
| Debian     | 8          | 7          | jre & jdk |
| Debian     | buster/sid | 8 & 9      | jre & jdk |
| Fedora     | 26 & 27    | 8 & 9      | jre & jdk |
| Ubuntu     | 17 & 18    | 8 & 9      | jre & jdk |

# Oracle

distribution = ansible_distribution
release = ansible_distribution_major_version

|distribution     |release     |java_version|java_type  |java_format|
|-----------------|------------|------------|-----------|-----------|
| Any             | Any        | 8 & 9      | jre & jdk | targz     |
| CentOS & Fedora | Any        | 8 & 9      | jre & jdk | rpm       |