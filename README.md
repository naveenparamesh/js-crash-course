# JavaScript Crash Course

This repository is meant to teach the essential language features of JavaScript by developing a mock chat application from scratch - no libraries, except Jasmine (assuming your browser supports all ES2015 features).

### How does this crash course work?

1. Clone the directory
2. Navigate to the `/src` directory and copy the full path of the `src/index.html` file into your browser
3. Notice that Jasmine unit tests are being run, but they're all failing
4. Fill out the code in `/src/js` so that the unit tests pass
5. Reference the `/ref/js` directory if you get stuck

### Major concepts include:

* Object oriented features (classes, inheritance, etc.)

```javascript
    class Sedan extends Vehicle {
        constructor(color) {
            this.color = color;
        }

        drive() {

        }
    }
```
        
* Variable declarations (let and const)

        const numWheels = 4; // Cannot be reassigned
        let color = "Blue" // May be reassigned

* Arrow functions

        cars.forEach(car => car.drive());

* Template strings

        const description = `The car is ${this.color} and has ${this.numWheels} wheels.`;

* Promises

        function waitAndGo() {
            return new Promise((resolve, reject) => {
                setTimeout(() => resolve("Done"), 1000);
            });
        }
        
        waitAndGo().then(message => {
            console.log(message);
        });

* Maps and sets

        let s = new Set();
        s.add("Sedan");
        s.add("Sedan");
        console.log(s); // Set {"Sedan"}

* Default, rest, and spread

        // Default
        function(name = "Anonymous") {
            const output = `Hello ${name}`;
        }

        // Rest
        function manyArgs(...args) {
            console.log(args.length);
        }
        
        // Spread
        function addToArray(anArray) {
            someOtherArray.push(...anArray);
        }

* Destructuring

        function multipleReturns() {
            const result1 = 3.14;
            const result2 = 2.72;
            return [result1, result2];
        }
        
        let a, b;
        [a, b] = multipleReturns(); // a = 3.14, b = 2.72
