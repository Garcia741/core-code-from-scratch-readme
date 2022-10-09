# Week 10.
# Lunes.

React.

    Libreria front end.
    para genera el aspecto de los programas asiendolo más llamativo para con el usuario y el uso
    de la interacción con el usuario, desarrolla una buena precentación.
    Puede ser un conjunto de programas que ayudan a crear la interface en uno solo, ya que 
    comunmente se realizaba individualmente.
    Es una de las librerias de javascript.

# Miercoles.

Más de React.

    Se conforma por componentes del programa que ayudan a mejorar la calidad de la interación entre
    el uso de los clientes con sus apps, como un ejemplo se puede observar a facebook, ya que 
    es una app que usa de los componentes que react ofrece y que le a ayuda a mejorar su entorno
    conbirtiendose en una app, usada por varios de nosotros en estos tiempos. 

# Jueves.

Kata React.

    import React from 'react';

    export const EggList = ({nombre, edad}) => {
    return (
        <ul>
        {eggs.map((egg, index) => {
            return <EasterEgg name={egg} key={index}/>
        })}
        </ul>
    )
    };

    export const EasterEgg = ({name}) => {
        return <li>{name}</li>
    };