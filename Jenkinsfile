node('master') {
  stage('checkout') {
    checkout scm
  }
  stage('build') {
    sh '/usr/local/bin/composer install';
  }
  stage('test') {
    sh './vendor/bin/phpunit';
  }
}
