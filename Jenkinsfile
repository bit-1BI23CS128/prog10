pipline{
agent any
tools{
maven'Maven'
}
stages{
stage('checkout'){
steps{
git branch:'master',url:'https://github.com/bit-1BI23CS128/prog10.git'
}
}
stage('build'){
steps{
sh'mvn clean package'
}}
stage('test'){
steps{
sh'mvn test'
}}
stage('run'){
steps{
sh'java -jar targat/MyMavenApp0010'
}}
post{
success{
echo'build successfull'
}
failure{
echo'build failed'
}}}
