pipeline{
agent any
tools{
maven'Maven'
jdk'jdk'
}
stages{
stage('Checkout'){
steps{
git branch:'master',url:'https://github.com/Prajna1101/MavenDevops.git'
}
}
stage('Build'){
steps{
sh'mvn clean install'
}
}
stage('Test'){
steps{
sh'mvn test'
}
}
stage('Run Application'){
steps{
sh 'java -jar target/MavenDevops-1.0-SNAPSHOT.jar'
}
}
}
post{
success{
echo'build and deployed successfully'
}
failure{
echo'build failed'
}
}
