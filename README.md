[![NPM Version](https://img.shields.io/npm/v/angular-pipes.svg)](https://npmjs.org/package/angular-pipes)

# angular-pipes

angular-pipes is a pipes library for `angular 2`. The project is hosted as `angular-pipes` on `npm`.


## Contribute

Feel free to contribute in any way. Post your own pipes, fix bugs, add options to existing pipes, etc.

## Pipes

You can find the documentations in the [`docs`](./docs) folder.

### Collections (array)

* [`empty`](./docs/array.md#empty)
* [`head`](./docs/array.md#head)
* [`initial`](./docs/array.md#initial)
* [`join`](./docs/array.md#join)
* [`last`](./docs/array.md#last)
* [`tail`](./docs/array.md#tail)
* [`uniq`](./docs/array.md#uniq)
* [`without`](./docs/array.md#without)
* [`range`](./docs/array.md#range) 
* [`map`](./docs/array.md#map) 
* [`pluck`](./docs/array.md#pluck)
* [`where`](./docs/array.md#where)
* [`orderBy`](./docs/array.md#orderBy) 
* [`reverse`](./docs/array.md#reverse)
* [`count`](./docs/array.md#count) 
* [`some`](./docs/array.md#some) 
* [`every`](./docs/array.md#every)


### Boolean

* [`greater`](./docs/boolean.md#greater)
* [`greaterOrEqual`](./docs/boolean.md#greaterOrEqual)
* [`less`](./docs/boolean.md#less)
* [`lessOrEqual`](./docs/boolean.md#lessOrEqual)
* [`equal`](./docs/boolean.md#equal)
* [`notEqual`](./docs/boolean.md#notEqual)
* [`identical`](./docs/boolean.md#identical)
* [`notIdentical`](./docs/boolean.md#notIdentical)
* [`null`](./docs/boolean.md#null)
* [`undefined`](./docs/boolean.md#undefined)
* [`nil`](./docs/boolean.md#nil) 
* [`number`](./docs/boolean.md#number)
* [`string`](./docs/boolean.md#string)
* [`function`](./docs/boolean.md#function)
* [`array`](./docs/boolean.md#array)
* [`object`](./docs/boolean.md#object)
* [`defined`](./docs/boolean.md#defined)

### Math

* [`bytes`](./docs/math.md#bytes)
* [`ceil`](./docs/math.md#ceil)
* [`floor`](./docs/math.md#floor)
* [`round`](./docs/math.md#round)
* [`min`](./docs/math.md#min)
* [`max`](./docs/math.md#max)
* [`mean`](./docs/math.md#mean)
* [`sum`](./docs/math.md#sum)
* [`degrees`](./docs/math.md#degrees)
* [`radians`](./docs/math.md#degrees)

### String

* [`leftpad`](./docs/string.md#leftpad)
* [`rightpad`](./docs/string.md#rightpad)
* [`pad`](./docs/string.md#pad)
* [`trim`](./docs/string.md#trim)
* [`split`](./docs/string.md#split)
* [`replace`](./docs/string.md#replace)
* [`match`](./docs/string.md#match)
* [`test`](./docs/string.md#test)
* [`newlines`](./docs/string.md#newlines)


### Object

* [`keys`](./docs/object.md#keys)
* [`toArray`](./docs/object.md#toArray)


## Install

### npm

```
npm install angular-pipes --save
```

### jspm

```
jspm install angular-pipes=npm:angular-pipes
```

## How to use

```typescript
import { NG2_PIPES } from 'angular-pipes';

@Component({
    // ...
    pipes: [NG2_PIPES]
    // ...
}}

```

You can also import only one category and a string pipe.

```typescript
import { NG2_BOOLEAN_PIPES, SplitPipe } from 'angular-pipes';

@Component({
    // ...
    pipes: [NG2_BOOLEAN_PIPES, SplitPipe]
    // ...
}}
```

But this will import all the files, you can do better by importing
just the boolean files.

```typescript
import { NG2_BOOLEAN_PIPES } from 'angular-pipes/pipes/boolean';
import { SplitPipe } from 'angular-pipes/pipes/string';
```

Same thing for the other categories.

And if you want to only include one file:

```typescript
import { HeadPipe } from 'angular-pipes/pipes/src/array/head.pipe';
```

The boolean pipes are only in two files, the types are in `types.pipe.ts` and the
conditions are in `conditions.pipe.ts`

If you only use one or two pipes, it's better to include only those two files. It will be lighter.
There is no bundle available, this project let you bundle as you wish.


## Tests

```
npm install
npm run lite
```

And navigate to `/unit-tests.html`.
It may take some time for the files to transpile.

`TODO`: Karma


## Contributors

* Florian Knop
