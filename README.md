# bs-typing

BuckleScript bindings for the [Typed.js](https://github.com/mattboldt/typed.js/) library.

## Install

First, install dependencies.

```shell
yarn add bs-typing typed.js
```

Lastly, add `bs-typing` to `bsconfig.json`.

```json
"bs-dependencies": [ "bs-typing" ]
```

## Usage

First, create an instance of the function and bind it to a variable. You do this by utilizing the `Type.make` and `Type.options` functions. The only required values for `Typed.make` is the `selector`, i.e. `"#typing-example`, which relates to an element in the DOM, and a `Typing.options` function which requires a `~typeSpeed` value.

```reason
let example =
  Typing.make(
    "#typing-example",
    Typing.options(
      ~strings=[|
        {j|Typing animation in ReasonML with the help of Typed.js|j},
      |],
      ~typeSpeed=50,
      ~typeDelay=30,
      ~loop=true,
      ~loopCount=5.0,
      (),
    ),
  );
```

Take a look at the [Example.re file](./example/Example.re) for more examples.
