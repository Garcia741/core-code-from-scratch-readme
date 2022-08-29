# Week 6.
# Lunes

Modulo01

    Creación de modulo completo, desde el .ts, js, tsconfig.json.html desde el
    cmd conectando con VSCode.


Typescript. Laboratorio1 (Corrección de código)

    let firstName : string;
    let lastName : String;
    let fullName : String;
    let age : number;
    let ukCitizen :boolean;

    firstName = 'Rebecca';
    lastName = 'Smith';
    age = 42;
    ukCitizen = false;
    fullName = firstName + " " + lastName;

    if (ukCitizen) {
        console.log("My name is " + fullName + ", I'm " + age + ", and I'm a citizen of the United Kingdom.");
    } else {
        console.log("My name is " + fullName + ", I'm " + age + ", and I'm not a citizen of the United Kingdom.");
    }

    /* EXERCISE 2
    TODO: You can use types to ensure operation outcomes. Run the code as is and then modify 
    it to have strongly typed variables. Then, address any errors you find so that the result 
    returned to a is 12. */

    let x : number;
    let y : number;
    let a : number;

    x = 5;
    y = 7;
    a = x + y;

    console.log(a);

    /* EXERCISE 3
    TODO: In the following code, implement an enum type called Season that represents 
    the constants "Fall", "Winter", "Spring", and "Summer". Then, update the function so 
    you can pass in the season by referencing an item in the enum, for example 
    Season.Fall, instead of the literal string "Fall". */
    enum Seasons {
        FALL = 'Fall',
        WINTER = 'Winter',
        SPRING = 'Spring',
        SUMMER = 'Summer'   
    }

    function whichMonths(season: Seasons) {

        let monthsInSeason: string ='';

        switch (season) {
            case "Fall":
                monthsInSeason = "September to November";
                break;
            case "Winter":
                monthsInSeason = "December to February";
                break;
            case "Spring":
                monthsInSeason = "March to May";
                break;
            case "Summer":
                monthsInSeason = "June to August";
        }

        return monthsInSeason;
    }

    console.log(whichMonths(Seasons.FALL));

    /* EXERCISE 4
    TODO: Declare the array as the type to match the type of the items in the array. */

    let randomNumbers : number [] = [];
    let nextNumber : number;
    
    for (let i = 0; i < 10; i++) {
        nextNumber = Math.floor(Math.random() * (100 - 1)) + 1;
        randomNumbers.push(nextNumber);
    }
    
    console.log(randomNumbers);

 
# 2

                export type User = {
        name: string;
        age: number;
        occupation: string;
        }

        export const users: User[] = [
            {
                name: 'Max Mustermann',
                age: 25,
                occupation: 'Chimney sweep'
            },
            {
                name: 'Kate Müller',
                age: 23,
                occupation: 'Astronaut'
            }
        ];

        export function logPerson(user: User) {
            console.log(` - ${user.name}, ${user.age}`);
        }

        console.log('Users:');
        users.forEach(logPerson);