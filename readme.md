
# Front-end Assessment

An assessment exam for Filta. Comprises of multiple exercises to test the skills of the applicant.



## Author

- [@mamaoag - Akia Japhet Mamaoag](https://www.github.com/mamaoag)


## Tech Stack

**Client:** NuxtJS, Bootstrap, Vue.js, HTML5, CSS3


## Installation

Clone this repository and run npm install.

```bash
  git clone https://github.com/mamaoag/frontend-assessment
  cd frontend-assessment
  npm install
```
    
## Usage
To run this on the browser. Do the following commands

```bash
npm run dev
```


## FAQ

#### Why did you use NuxtJS instead of just Vue?

While a simple SPA would be suffice, we would have to rely on the client browser to load all our javascript resources then load the site. However we lose SEO and indexing for this. Also NuxtJS handles the abstraction of handling SSR.

#### Why is the result of ('b'+'a'+ + 'a' + 'a').toLowerCase() 'banana'?

The main reason behind lies on `+'a'`. The string is evaluated like this: 
`('b' + 'a' + (+'a'))`. Appending + on a string and evaluating it in an integer convert the said character to a number. Example: `+'1' + 1 = 2`. In this scenario `a` is not a numeric character therefore it expresses the value as `NaN`. and with out function toLowerCase evaluate this as part of the string hence: 'banana'

