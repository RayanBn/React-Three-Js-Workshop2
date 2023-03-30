# React-Three-Js-Workshop2

<h2>Introduction</h2>
In this second workshop session, you will discover the physics with React Three JS.

<h2>Step 1</h1>
Clone the repo !<br>

```
git clone git@github.com:RayanBn/React-Three-Js-Workshop2.git
```

Steps to follow for compiling :

```
npm install
npm run dev
```

<h2>Step 2</h2>
Let's start by discovering how to debug a react three application!
Let's start by surrounding our code with a tag to warn you of any problem you may encounter.
<br>
<br>

```javascript
root.render(
    <StrictMode>
        <Canvas
            camera={ {
                fov: 45,
                near: 0.1,
                far: 200,
                position: [ - 4, 3, 6 ]
            } }
        >
            <Experience />
        </Canvas>
    </StrictMode>
)
```

<h2>Step 3</h2>
Now, it is important to be able to quickly test what we want to do. For this, we will use leva!
<br>
To do this, you must first import it:

```js
import { useControls } from 'leva'
```

Once the module is imported, you will be able to declare several variables with a default value and then modify them in real time on your site:
```js
const { color } = useControls({
    color: '#ff0000',
})
```

```js
<meshStandardMaterial color={ color } />
```

<h2>Step 4</h2>
Now let's go to the physics! For this, we will use a branch of react three called rapier.

```js
import { Physics, RigidBody, Debug } from "@react-three/rapier";
```

Here is a link to the documentation of rapier. Here the goal will be to create simple objects with physics and to be able to modify their hitbox: <br>
https://github.com/pmndrs/react-three-rapier

<h2>Step 5</h2>
Thanks to step 4, you will be able to access the properties of each object, to then modify them as you wish. This allows you to make them interact with your scene. Now, let's learn how to load 3D models with react-three/drei.
Here is a link to the documentation: <br>
https://github.com/pmndrs/drei#usegltf <br>
Here is a link where you can find several free model dedicated to react three js: <br>
https://market.pmnd.rs/
