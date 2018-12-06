node('master') {
  stage('checkout') {
    checkout scm
  }
  stage('build') {
    sh '/usr/local/bin/composer install';
  }
 stage('create-env-keys') {
	sh 'cp .env.example .env';
	sh 'php artisan key:generate';	
  }

  stage('test') {
    sh './vendor/bin/phpunit';
  }

  stage('xunit') {
	junit 'reports/xunit';	
  }
}
