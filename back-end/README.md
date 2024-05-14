
## How to run locally
- Make sure you have Java 11 or newer, Gradle, Docker, and PostgreSQL
- cd to project root
- run: `docker-compose up -d db`
- run: `./gradlew bootRun`
- Wait approximately 5 minutes for the database to initialize (text "Database has been initialized" will be displayed to the terminal)
- Navigate to `http://localhost:8080/api/stock/{symbol}`

## How to run only with docker

  - cd to project root
    - run: `./gradlew build -x test` (without tests because tests will take a long time to complete)
    - run: `docker image build -t bootdocker:staging .`
    - Finally `docker-compose up -d` : for starting all containers

## How to run tests
- Select the test module and run tests with coverage
- Because we are using an external API and the database has to be initialized, running test takes time (approximately 5 minutes to run all tests)
