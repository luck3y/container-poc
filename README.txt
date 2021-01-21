======= EAP 7.3 Docker image Example ========

Instructions: 
=================

- Download EAP 7.3.0 and 7.3.4 patchfile from: https://access.redhat.com/jbossnetwork/restricted/listSoftware.html?product=appplatform&downloadType=distributions

- Add files to cekit cache:
   $ cekit-cache add jboss-eap-7.3.0.zip --md5=3dba80cc1be17b00cb901441111886f3
   $ cekit-cache add jboss-eap-7.3.4-patch.zip --md5=c37fcbbf369647c1904dc061737e866c

- Build the image:
   $ cekit -v build docker

- Alternatively, you can generate a DockerFile which may be modified to suit your end usage:
   $ cekit -v build --dry-run docker
 The DockerFile (and artifacts / modules) are found in target/image, which you may modify and then build with:
   $ cd target/image
   $ docker build .

