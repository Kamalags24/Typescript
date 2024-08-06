# Typescript

TypeScript est un sur-ensemble typé de JavaScript qui ajoute des types statiques en plus de la vérification des types au moment de la compilation. Il est particulièrement utile pour les projets à grande échelle où la robustesse et la maintenabilité du code sont cruciales. Voici quelques concepts clés et avantages de TypeScript :

### Concepts Clés

1. **Types Statiques** : TypeScript permet de définir des types pour les variables, fonctions, et objets, ce qui aide à attraper les erreurs au moment de la compilation.
   ```typescript
   let isDone: boolean = false;
   let lines: number = 42;
   ```

2. **Interfaces** : Elles permettent de définir des contrats pour les objets.
   ```typescript
   interface User {
     name: string;
     age: number;
   }

   const user: User = { name: "Alice", age: 25 };
   ```

3. **Classes et Héritage** : TypeScript améliore la POO (programmation orientée objet) en JavaScript avec des classes, interfaces et héritages.
   ```typescript
   class Person {
     name: string;

     constructor(name: string) {
       this.name = name;
     }

     greet() {
       console.log(`Hello, my name is ${this.name}`);
     }
   }

   class Employee extends Person {
     employeeId: number;

     constructor(name: string, employeeId: number) {
       super(name);
       this.employeeId = employeeId;
     }
   }
   ```

4. **Modules** : TypeScript utilise des modules pour organiser et réutiliser le code.
   ```typescript
   // math.ts
   export function add(a: number, b: number): number {
     return a + b;
   }

   // main.ts
   import { add } from './math';
   console.log(add(2, 3));
   ```

### Avantages

1. **Typage statique** : Réduction des erreurs à l'exécution en les capturant au moment de la compilation.
2. **Amélioration de l'éditeur** : Auto-complétion, navigation dans le code et refactoring plus efficaces.
3. **Meilleure lisibilité et maintenabilité** : Le code est plus facile à comprendre et à maintenir.
4. **Interopérabilité** : Fonctionne bien avec JavaScript et les bibliothèques JavaScript existantes.

### Mise en Place

Pour commencer avec TypeScript :

1. **Installation** :
   ```bash
   npm install -g typescript
   ```

2. **Initialisation d'un projet** :
   ```bash
   tsc --init
   ```

3. **Compilation** :
   ```bash
   tsc
   ```

4. **Configuration** : Le fichier `tsconfig.json` permet de configurer les options du compilateur TypeScript.
   ```json
   {
     "compilerOptions": {
       "target": "ES6",
       "module": "commonjs",
       "strict": true,
       "esModuleInterop": true
     }
   }
   ```

En utilisant TypeScript, vous pouvez améliorer la qualité et la robustesse de vos projets, en particulier pour les applications de grande envergure.
