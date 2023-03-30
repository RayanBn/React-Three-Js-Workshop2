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
Commencons par decouvrir comment debug une application react three !
Commencons par entourer notre code d'un balise permettant de vous avertir de chaque problème que vous allez rencontrer.
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
Maintenant, il est important de pouvoir tester rapidement ce que l'on veut faire. Pour cela, on va utiliser leva !
<br>
Pour cela, il faudra d'abord l'importer :

```js
import { useControls } from 'leva'
```

Une fois le module importer, vous allez pouvoir declarer plusieurs variable avec une valeur par defaut pour ensuite pouvoir les modifier en temps reel sur votre site :
```js
const { color } = useControls({
    color: '#ff0000',
})
```

```js
<meshStandardMaterial color={ color } />
```

<h2>Step 4</h2>
Passons maintenant a la physique ! Pour ca, nous allons utiliser une branche de react three qui s'appel rapier.

```js
import { Physics, RigidBody, Debug } from "@react-three/rapier";
```

Voici un lien vers la documentation de rapier. Ici le but sera de creer des objets simple avec de la physique et de pouvoir modifier leurs hitbox : <br>
https://github.com/pmndrs/react-three-rapier

<h2>Step 5</h2>
Grace a la step 4, vous pourez acceder aux propriétés de chaque objets, pour ensuite les modifier comme vous le souhaitez. Vous permettant ainsi le les faire interagir avec votre scene. Maintenant, apprenons a charger des models 3D grace a react-three/drei.
Voici un lien vers la documentation :<br>
https://github.com/pmndrs/drei#usegltf <br>
Voici un lien ou vous pourrez trouver plusieurs model gratuit dedié a react three js : <br>
https://market.pmnd.rs/
