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

 
# 1

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

# 2
        interface User {
            name: string;
            age: number;
            occupation: string;
        }

        interface Admin {
            name: string;
            age: number;
            role: string;
        }

        export type Person = User | Admin;

        export const persons: Person[] /* <- Person[] */ = [
            {
                name: 'Max Mustermann',
                age: 25,
                occupation: 'Chimney sweep'
            },
            {
                name: 'Jane Doe',
                age: 32,
                role: 'Administrator'
            },
            {
                name: 'Kate Müller',
                age: 23,
                occupation: 'Astronaut'
            },
            {
                name: 'Bruce Willis',
                age: 64,
                role: 'World saver'
            }
        ];

        export function logPerson(user: Person) {
            console.log(` - ${user.name}, ${user.age}`);
        }

        persons.forEach(logPerson);

# 3

        interface User {
            name: string;
            age: number;
            occupation: string;
        }

        interface Admin {
            name: string;
            age: number;
            role: string;
        }

        export type Person = User | Admin;

        export const persons: Person[] = [
            {
                name: 'Max Mustermann',
                age: 25,
                occupation: 'Chimney sweep'
            },
            {
                name: 'Jane Doe',
                age: 32,
                role: 'Administrator'
            },
            {
                name: 'Kate Müller',
                age: 23,
                occupation: 'Astronaut'
            },
            {
                name: 'Bruce Willis',
                age: 64,
                role: 'World saver'
            }
        ];

        export function logPerson(person: Person) {
            let additionalInformation: string;
            if ('role' in person) {
                additionalInformation = person.role;
            } else {
                additionalInformation = person.occupation;
            }
            console.log(` - ${person.name}, ${person.age}, ${additionalInformation}`);
        }

        persons.forEach(logPerson);

# 4
        interface User {
            type: 'user';
            name: string;
            age: number;
            occupation: string;
        }

        interface Admin {
            type: 'admin';
            name: string;
            age: number;
            role: string;
        }

        export type Person = User | Admin;

        export const persons: Person[] = [
            { type: 'user', name: 'Max Mustermann', age: 25, occupation: 'Chimney sweep' },
            { type: 'admin', name: 'Jane Doe', age: 32, role: 'Administrator' },
            { type: 'user', name: 'Kate Müller', age: 23, occupation: 'Astronaut' },
            { type: 'admin', name: 'Bruce Willis', age: 64, role: 'World saver' }
        ];

        export function isAdmin(person: Person):person is Admin {
            return person.type === 'admin';
        }

        export function isUser(person: Person): person is User {
            return person.type === 'user';
        }

        export function logPerson(person: Person) {
            let additionalInformation: string = '';
            if (isAdmin(person)) {
                additionalInformation = person.role;
            }
            if (isUser(person)) {
                additionalInformation = person.occupation;
            }
            console.log(` - ${person.name}, ${person.age}, ${additionalInformation}`);
        }

        console.log('Admins:');
        persons.filter(isAdmin).forEach(logPerson);

        console.log();

        console.log('Users:');
        persons.filter(isUser).forEach(logPerson);

# 5

        interface User {
            type: 'user';
            name: string;
            age: number;
            occupation: string;
        }

        interface Admin {
            type: 'admin';
            name: string;
            age: number;
            role: string;
        }

        export type Person = User | Admin;

        export const persons: Person[] = [
            { type: 'user', name: 'Max Mustermann', age: 25, occupation: 'Chimney sweep' },
            {
                type: 'admin',
                name: 'Jane Doe',
                age: 32,
                role: 'Administrator'
            },
            {
                type: 'user',
                name: 'Kate Müller',
                age: 23,
                occupation: 'Astronaut'
            },
            {
                type: 'admin',
                name: 'Bruce Willis',
                age: 64,
                role: 'World saver'
            },
            {
                type: 'user',
                name: 'Wilson',
                age: 23,
                occupation: 'Ball'
            },
            {
                type: 'admin',
                name: 'Agent Smith',
                age: 23,
                role: 'Administrator'
            }
        ];

        export const isAdmin = (person: Person): person is Admin => person.type === 'admin';
        export const isUser = (person: Person): person is User => person.type === 'user';

        export function logPerson(person: Person) {
            let additionalInformation = '';
            if (isAdmin(person)) {
                additionalInformation = person.role;
            }
            if (isUser(person)) {
                additionalInformation = person.occupation;
            }
            console.log(` - ${person.name}, ${person.age}, ${additionalInformation}`);
        }

        export function filterUsers(persons: Person[], criteria: Partial<Omit<User, 'type'>>): User[] {
            return persons.filter(isUser).filter((user) => {
                const criteriaKeys = Object.keys(criteria) as (keyof Partial<Omit<User, 'type'>>)[];
                return criteriaKeys.every((fieldName) => {
                    return user[fieldName] === criteria[fieldName];
                });
            });
        }

        console.log('Users of age 23:');

        filterUsers(
            persons,
            {
                age: 23
            }
        ).forEach(logPerson);