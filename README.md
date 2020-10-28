# kra-pin-scrapper-doc
Documentation for kra-pin-scrapper
# kra-pin-scraper

### How to build with gradle
> This project will run with ```java 11``` or later.
<br/>Build Commands: 
<br/> Windows: ```gradlew clean build```
<br/> Linux/Unix ```./gradlew clean build```

### How to Build Docker Image:
>```docker build . -f Dockerfile-Firefox -t ckeidev/kra-pin-scraper:latest```

### How to run Docker image:
> ``` docker run -it --shm-size=512m --name kra-pin-checker -p 8080:8080 ckeidev/kra-pin-scraper:latest ```
### How to call the API
> ```http://localhost:8080/pin-checker/{KRA_PIN_NUMBER}```

*Response Object*
```
{
    "error": Int,
    "errorMessage": String,
    "pinNumber": String,
    "taxPayerName": String,
    "pinStatus": String,
    "obligationName": String,
    "currentStatus": String,
    "effectiveFrom": String,
    "effectiveTo": String
}
```
