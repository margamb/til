### Form React

![](imgages/input_form_explanation.png)

```jsx
import React, { useEffect, useState } from 'react';

function App() {

    const [nameTeam, setNameTeam] = useState('');
    const [nameTeam2, setNameTeam2] = useState('');

    function addNameTeam(ev) {
        ev.preventDefault();
        console.debug(ev.target)
        setNameTeam(ev.target.teamName.value)
        setNameTeam2(ev.target.teamName2.value)
    }

    return (
        <>
        <h1>Form React<h1>
        <p>The NAME of input match with setNameTeam(ev.target.NAME.value)</p>
        <form onSubmit={addNameTeam}>
            <input type="text" placeholder="Write team name" name="teamName" />
            <input type="text" placeholder="Write team name" name="teamName2" />
            <input type="submit" value="submit" />
        </form>
        <p>{nameTeam}</p>
        <p>{nameTeam2}</p>  
        </>
    )

}

```

### Form Javascript
#### STEPS
- 1 -> 👆 Seleccionar elementos del DOM (querySelector)
    - const valueName = document.querySelector('#name');  
- 2 -> 👂🏻 Haciendo que escuchen (addEventListener)
- 3 -> Cogiendo los valores del DOM (.value)
    -const inputName = document.querySelector('.js-input-name').value;
- 4 -> Cambiar valores del DOM (innerHTML)

``` html
    <form>
        <input type="text" placeholder="Write name" name="name" class="js-input-name"/>
        <input type="text" placeholder="Write job" name="job" class="js-input-job"/>
        <input type="submit" value="submit" class="js-submit"/>
    </form>
    <div id="name"></div>
    <div id="job"></div>

```

``` js
    // Seleccionar elementos del DOM (querySelector)
    const submit = document.querySelector('.js-submit')
    const valueName = document.querySelector('#name');  
    const valueJob = document.querySelector('#job');  

    //Cogiendo los valores del DOM (.value)
    const inputName = document.querySelector('.js-input-name').value;
    const inputJob = document.querySelector('.js-input-job').value;


    function onSubmit(ev) {
        ev.preventDefault();
        valueName.innerHTML = inputName;
        valueJob.innerHTML = inputJob;
    }

    submit.addEventListener('click', onSubmit);
```
 