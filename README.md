Role Name
=========

A brief description of the role goes here.

Requirements
------------
Java8 must be installed on the systems. JAVA_HOME must be defined either implicitely or explicitely.
selinux must be disabled on the centOS/Redhat base systems.

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):

# defaults file for ansible-logstash
# Defines if logstash_config_dir should be cleared out
clear_logstash_config: false

# Defines if logstash should be configured
  java_tmp_storage: /tmp/java_install
__java_oracle_rpm: java8u131
__java_oracle_download: http://download.oracle.com/otn-pub/java/jdk/8u131-b11/d54c1d3a095b4ff2b6607d096fa80163/jdk-8u131-linux-x64.rpm
#__java_oracle_download_checksum: md5:9024d13ec651d07de450d465f14065a6
path_to_data:
oracle_java_dir_source: '/usr/local/src'
oracle_java_set_as_default: yes
oracle_java_version: "8"
oracle_java_version_string: "1.{{ oracle_java_version }}.0_{{ oracle_java_version_update }}"
oracle_java_ansible_arch_mappings:
  x86_64: x64
  i386: i586
oracle_java_cache_valid_time: 3600
oracle_java_home: "/usr/lib/jvm/java-{{ oracle_java_version }}-oracle"
oracle_java_os_supported: yes
oracle_java_state: latest

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
