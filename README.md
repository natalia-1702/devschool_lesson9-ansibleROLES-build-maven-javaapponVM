Во 2 роли можно использовать:

  - name: Synchronization of src on the inventory host to the dest on the localhost in pull mode
    synchronize:
      mode: push
      src: /home/boxfuse-sample-java-war-hello/target/hello-1.0.war
      dest: /var/lib/tomcat8/webapps/hello-1.0.war
    delegate_to: "{{groups['build'][0]}}"
    
    Но для этого нужно ключи сгенерить на 1 и пробросить на 2-ю(руками или ансиблом).
