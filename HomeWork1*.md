  Преобразовать написанный код в 26-33 пунктах в функцию, принимающую на вход возраст.  
Пример: const checkAge = function(age) {  
Ваши преобразования  
}  
Вывести в консоль результат работы функции с возрастами 17, 18, 61  
  
```
const checkAge = function(age) {
    const age_1 = 10;
    const age_2 = 18;
    const age_3 = 60;
  
    if (age < age_2) {
      return "You don't have access cause your age is " + age + " It's less than " + age_2;
    } else if (age >= age_2 && age < age_3) {
      return "Welcome!";
    } else if (age > age_3) {
      return "Keep calm and look Culture channel";
    } else {
      return "Technical work";
    }
  };
  
  console.log(checkAge(17));
  console.log(checkAge(18));
  console.log(checkAge(61));
```


Преобразовать задание 1 таким образом, чтобы первым делом в функции проверялся тип данных. И если он не Number - кидалась ошибка.  

 
```
const checkAge = function(age) {
    if (typeof age !== "number" || isNaN(age)) {
      throw new Error("Age should be a valid number");
    }
  
    const age_1 = 10;
    const age_2 = 18;
    const age_3 = 60;
  
    if (age < age_2) {
      return "You don't have access cause your age is " + age + " It's less than " + age_2;
    } else if (age >= age_2 && age < age_3) {
      return "Welcome!";
    } else if (age > age_3) {
      return "Keep calm and look Culture channel";
    } else {
      return "Technical work";
    }
  };
  
  try {
    console.log(checkAge(17));
    console.log(checkAge(18));
    console.log(checkAge(61));
    console.log(checkAge("not a number")); 
  } catch (error) {
    console.error(error.message);
  }
```
 
  
Преобразовать 2* таким образом, чтобы значение '2' (строка в которой лежит ТОЛЬКО ЦИФРА) пропускалось, преобразовываясь в number  
  
```
const checkAge = function(age) {
    if (typeof age === "string" && age.trim().length === 1 && !isNaN(parseInt(age))) {
      age = parseInt(age);
    }
  
    if (typeof age !== "number" || isNaN(age)) {
      throw new Error("Age should be a valid number");
    }
  
    const age_1 = 10;
    const age_2 = 18;
    const age_3 = 60;
  
    if (age < age_2) {
      return "You don't have access cause your age is " + age + " It's less than " + age_2;
    } else if (age >= age_2 && age < age_3) {
      return "Welcome!";
    } else if (age > age_3) {
      return "Keep calm and look Culture channel";
    } else {
      return "Technical work";
    }
  };
  
  try {
    console.log(checkAge(17));
    console.log(checkAge(18));
    console.log(checkAge(61));
    console.log(checkAge("not a number"));
    console.log(checkAge("2")); 
  } catch (error) {
    console.error(error.message);
  }
```
