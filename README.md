yum install git -y
yum install docker -y
systemctl start docker
systemctl status docker

vim Student.java

# Dockerfile with java file
vim Dockerfile
+++++++++++++++++++++++
FROM amazoncorretto:21-al2023
LABEL maintainer="krishna"
WORKDIR /app
COPY Student.java .
RUN javac Student.java
CMD ["java", "Student"]
+++++++++++++++++++++++++++
docker build -t my-student-app .

[root@ip-172-31-19-80 PROJECT1_Student_java_Docker]# docker run -it my-student-app
OUTPUT:
++++++++++++++++
LEARN HERE AND LEAD ANYWHERE!!!
My Name is: KRISHNA
My Course is: PYTHON
My Roll Number is: 1596
=======================
JENKINS-WEBHHOK-TRIIGER
JENKINS-WEBHHOK-TRIIGER
