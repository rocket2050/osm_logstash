osm_lagstash
=========

An Ansible Role that installs Logstash 5.x on RedHat/CentOS Debian/Ubuntu.

Requirements
------------
Java8 must be installed on the systems. JAVA_HOME must be defined either implicitely or explicitely.
Selinux must be disabled on the centOS/Redhat base systems.

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):

  clear_logstash_config: false
  java_tmp_storage: /tmp/java_install
  java_oracle_rpm: java8u131
  java_oracle_download: http://download.oracle.com/otn-pub/java/jdk/8u131-b11/d54c1d3a095b4ff2b6607d096fa80163/jdk-8u131-   linux-x64.rpm
  java_oracle_download_checksum: md5:9024d13ec651d07de450d465f14065a6

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

It depends on java8 role and will fail if java is not found in the system

Example Playbook
----------------

Including an example of how to use osm_logstash role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: default
      roles:
         - { role: osm_logstash }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
