echo " --- Start Build & rRun Container ---"
pwd
echo "this is build number: $BUILD_ID - " >> index.html
date >> index.html
cat index.html
docker run -d --rm --name my-apache-app -p 81:80 -v "$PWD":usr/local/apache2/htdocs/ httpd
echo " ---Finish Build And Run Container--- "
