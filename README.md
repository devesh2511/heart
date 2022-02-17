# Project Name
> Outline a brief description of your project.

> [Live demo here](https://www.example.com).

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Screenshots](#screenshots)
* [Usage](#usage)
* [Contact](#contact)

## General Information
- Provide general information about your project here.
- What problem does it (intend to) solve?
- What is the purpose of your project?
- Why did you undertake it?

## Technologies Used
- HTML5
- CSS3
- Javascript
- healthAPI
- collect.chat
- GoogleMapsAPI

## Screenshots
![hp1](./img/ss1.png)
![hp2](./img/ss2.png)

![hd1](./img/ss3.png)
![hd2](./img/ss4.png)

![bmi](./img/ss5.png)
![bmr](./img/ss6.png)

## Usage
How does one go about using it?
Provide various use cases and code examples here.

```
setTimeout(() => {
        fetch(`https://heartapi.herokuapp.com/predict?age=${age}&sex=${sex}&cigs=${cigs}&chol=${cholestrol}&sBP=${sBP}&dia=${diabetes}&dBP=${dBP}&gluc=${glucose}&hRate=${heartRate}`)
        .then(res => res.json())
        .then(data => {
          prediction = parseFloat(data['probability'][0][1]).toFixed(5);
          console.log(prediction)
          document.querySelector('.loader').style.display = 'none';
          if (cigs > 0 & prediction > 0.07) {
            document.querySelector('.clearfix').innerHTML = `
            <p class="nl-form">Quit Smoking Today<br>Predicted probability of having a coronary heart disease (Heart Attack)is ${prediction*100} % <br>Please Consult Cardiologist</p>`;

          }
          else if (cigs > 1 & prediction < 0.07){
            document.querySelector('.clearfix').innerHTML = `
            <p class="nl-form">Quit Smoking Today<br>Predicted probability of having a coronary heart disease (Heart Attack) is ${prediction*100} %</p>`;
          }
            else{
              document.querySelector('.clearfix').innerHTML = `
              <p class="nl-form">Predicted probability of having a coronary heart disease (Heart Attack) is ${prediction*100} %</p>`;} 
        })
   ```
        
## Contact
Created by [@deveshjain](https://github.com/devesh2511) - feel free to contact me!