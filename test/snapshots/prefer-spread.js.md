# Snapshot report for `test/prefer-spread.js`

The actual snapshot is saved in `prefer-spread.js.snap`.

Generated by [AVA](https://avajs.dev).

## Invalid #1
      1 | const x = Array.from(set);

> Output

    `␊
      1 | const x = [...set];␊
    `

> Error 1/1

    `␊
    > 1 | const x = Array.from(set);␊
        |           ^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #2
      1 | Array.from(set).map(() => {});

> Output

    `␊
      1 | [...set].map(() => {});␊
    `

> Error 1/1

    `␊
    > 1 | Array.from(set).map(() => {});␊
        | ^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #3
      1 | Array.from(set, mapFn).reduce(() => {});

> Output

    `␊
      1 | [...set].map(mapFn).reduce(() => {});␊
    `

> Error 1/1

    `␊
    > 1 | Array.from(set, mapFn).reduce(() => {});␊
        | ^^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #4
      1 | Array.from(set, mapFn, thisArg).reduce(() => {});

> Output

    `␊
      1 | [...set].map(mapFn, thisArg).reduce(() => {});␊
    `

> Error 1/1

    `␊
    > 1 | Array.from(set, mapFn, thisArg).reduce(() => {});␊
        | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #5
      1 | Array.from(set, () => {}, thisArg).reduce(() => {});

> Output

    `␊
      1 | [...set].map(() => {}, thisArg).reduce(() => {});␊
    `

> Error 1/1

    `␊
    > 1 | Array.from(set, () => {}, thisArg).reduce(() => {});␊
        | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #6
      1 | Array.from(new Set([1, 2])).map(() => {});

> Output

    `␊
      1 | [...new Set([1, 2])].map(() => {});␊
    `

> Error 1/1

    `␊
    > 1 | Array.from(new Set([1, 2])).map(() => {});␊
        | ^^^^^^^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #7
      1 | Array.from(document.querySelectorAll("*")).map(() => {});

> Output

    `␊
      1 | [...document.querySelectorAll("*")].map(() => {});␊
    `

> Error 1/1

    `␊
    > 1 | Array.from(document.querySelectorAll("*")).map(() => {});␊
        | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #8
      1 | const foo = []
      2 | Array.from(arrayLike).forEach(doSomething)

> Output

    `␊
      1 | const foo = []␊
      2 | ;[...arrayLike].forEach(doSomething)␊
    `

> Error 1/1

    `␊
      1 | const foo = []␊
    > 2 | Array.from(arrayLike).forEach(doSomething)␊
        | ^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #9
      1 | const foo = "1"
      2 | Array.from(arrayLike).forEach(doSomething)

> Output

    `␊
      1 | const foo = "1"␊
      2 | ;[...arrayLike].forEach(doSomething)␊
    `

> Error 1/1

    `␊
      1 | const foo = "1"␊
    > 2 | Array.from(arrayLike).forEach(doSomething)␊
        | ^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #10
      1 | const foo = null
      2 | Array.from(arrayLike).forEach(doSomething)

> Output

    `␊
      1 | const foo = null␊
      2 | ;[...arrayLike].forEach(doSomething)␊
    `

> Error 1/1

    `␊
      1 | const foo = null␊
    > 2 | Array.from(arrayLike).forEach(doSomething)␊
        | ^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #11
      1 | const foo = true
      2 | Array.from(arrayLike).forEach(doSomething)

> Output

    `␊
      1 | const foo = true␊
      2 | ;[...arrayLike].forEach(doSomething)␊
    `

> Error 1/1

    `␊
      1 | const foo = true␊
    > 2 | Array.from(arrayLike).forEach(doSomething)␊
        | ^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #12
      1 | const foo = 1
      2 | Array.from(arrayLike).forEach(doSomething)

> Output

    `␊
      1 | const foo = 1␊
      2 | ;[...arrayLike].forEach(doSomething)␊
    `

> Error 1/1

    `␊
      1 | const foo = 1␊
    > 2 | Array.from(arrayLike).forEach(doSomething)␊
        | ^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #13
      1 | const foo = /./
      2 | Array.from(arrayLike).forEach(doSomething)

> Output

    `␊
      1 | const foo = /./␊
      2 | ;[...arrayLike].forEach(doSomething)␊
    `

> Error 1/1

    `␊
      1 | const foo = /./␊
    > 2 | Array.from(arrayLike).forEach(doSomething)␊
        | ^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #14
      1 | const foo = /./g
      2 | Array.from(arrayLike).forEach(doSomething)

> Output

    `␊
      1 | const foo = /./g␊
      2 | ;[...arrayLike].forEach(doSomething)␊
    `

> Error 1/1

    `␊
      1 | const foo = /./g␊
    > 2 | Array.from(arrayLike).forEach(doSomething)␊
        | ^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #15
      1 | const foo = bar
      2 | Array.from(arrayLike).forEach(doSomething)

> Output

    `␊
      1 | const foo = bar␊
      2 | ;[...arrayLike].forEach(doSomething)␊
    `

> Error 1/1

    `␊
      1 | const foo = bar␊
    > 2 | Array.from(arrayLike).forEach(doSomething)␊
        | ^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #16
      1 | const foo = bar.baz
      2 | Array.from(arrayLike).forEach(doSomething)

> Output

    `␊
      1 | const foo = bar.baz␊
      2 | ;[...arrayLike].forEach(doSomething)␊
    `

> Error 1/1

    `␊
      1 | const foo = bar.baz␊
    > 2 | Array.from(arrayLike).forEach(doSomething)␊
        | ^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #17
      1 | function* foo() {
      2 | 	yield Array.from(arrayLike).forEach(doSomething)
      3 | }

> Output

    `␊
      1 | function* foo() {␊
      2 | 	yield [...arrayLike].forEach(doSomething)␊
      3 | }␊
    `

> Error 1/1

    `␊
      1 | function* foo() {␊
    > 2 | 	yield Array.from(arrayLike).forEach(doSomething)␊
        | 	      ^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
      3 | }␊
    `

## Invalid #18
      1 | const foo = `bar`
      2 | Array.from(arrayLike).forEach(doSomething)

> Output

    `␊
      1 | const foo = `bar`␊
      2 | ;[...arrayLike].forEach(doSomething)␊
    `

> Error 1/1

    `␊
      1 | const foo = `bar`␊
    > 2 | Array.from(arrayLike).forEach(doSomething)␊
        | ^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #19
      1 | const foo = [];
      2 | Array.from(arrayLike).forEach(doSomething)

> Output

    `␊
      1 | const foo = [];␊
      2 | [...arrayLike].forEach(doSomething)␊
    `

> Error 1/1

    `␊
      1 | const foo = [];␊
    > 2 | Array.from(arrayLike).forEach(doSomething)␊
        | ^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #20
      1 | for (const key of Array.from(arrayLike)) {
      2 | }

> Output

    `␊
      1 | for (const key of [...arrayLike]) {␊
      2 | }␊
    `

> Error 1/1

    `␊
    > 1 | for (const key of Array.from(arrayLike)) {␊
        |                   ^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
      2 | }␊
    `

## Invalid #21
      1 | for (const key in Array.from(arrayLike)) {
      2 | }

> Output

    `␊
      1 | for (const key in [...arrayLike]) {␊
      2 | }␊
    `

> Error 1/1

    `␊
    > 1 | for (const key in Array.from(arrayLike)) {␊
        |                   ^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
      2 | }␊
    `

## Invalid #22
      1 | const foo = `${Array.from(arrayLike)}`

> Output

    `␊
      1 | const foo = `${[...arrayLike]}`␊
    `

> Error 1/1

    `␊
    > 1 | const foo = `${Array.from(arrayLike)}`␊
        |                ^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #23
      1 | async function foo(){
      2 | 	return await Array.from(arrayLike)
      3 | }

> Output

    `␊
      1 | async function foo(){␊
      2 | 	return await [...arrayLike]␊
      3 | }␊
    `

> Error 1/1

    `␊
      1 | async function foo(){␊
    > 2 | 	return await Array.from(arrayLike)␊
        | 	             ^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
      3 | }␊
    `

## Invalid #24
      1 | foo()
      2 | Array.from(arrayLike).forEach(doSomething)

> Output

    `␊
      1 | foo()␊
      2 | ;[...arrayLike].forEach(doSomething)␊
    `

> Error 1/1

    `␊
      1 | foo()␊
    > 2 | Array.from(arrayLike).forEach(doSomething)␊
        | ^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #25
      1 | const foo = {}
      2 | Array.from(arrayLike).forEach(doSomething)

> Output

    `␊
      1 | const foo = {}␊
      2 | ;[...arrayLike].forEach(doSomething)␊
    `

> Error 1/1

    `␊
      1 | const foo = {}␊
    > 2 | Array.from(arrayLike).forEach(doSomething)␊
        | ^^^^^^^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

## Invalid #1
      1 | [1].concat(2)

> Output

    `␊
      1 | [1, 2]␊
    `

> Error 1/1

    `␊
    > 1 | [1].concat(2)␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #2
      1 | [1].concat([2, 3])

> Output

    `␊
      1 | [1, 2, 3]␊
    `

> Error 1/1

    `␊
    > 1 | [1].concat([2, 3])␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #3
      1 | [1].concat(2,)

> Output

    `␊
      1 | [1, 2]␊
    `

> Error 1/1

    `␊
    > 1 | [1].concat(2,)␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #4
      1 | [1].concat([2, ...bar],)

> Output

    `␊
      1 | [1, 2, ...bar]␊
    `

> Error 1/1

    `␊
    > 1 | [1].concat([2, ...bar],)␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #5
      1 | [1,].concat(2)

> Output

    `␊
      1 | [1, 2,]␊
    `

> Error 1/1

    `␊
    > 1 | [1,].concat(2)␊
        |      ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #6
      1 | [1,].concat([2, 3])

> Output

    `␊
      1 | [1, 2, 3,]␊
    `

> Error 1/1

    `␊
    > 1 | [1,].concat([2, 3])␊
        |      ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #7
      1 | [1,].concat(2,)

> Output

    `␊
      1 | [1, 2,]␊
    `

> Error 1/1

    `␊
    > 1 | [1,].concat(2,)␊
        |      ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #8
      1 | [1,].concat([2, 3],)

> Output

    `␊
      1 | [1, 2, 3,]␊
    `

> Error 1/1

    `␊
    > 1 | [1,].concat([2, 3],)␊
        |      ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #9
      1 | (( (([1,])).concat( (([2, 3])) ,) ))

> Output

    `␊
      1 | (( (([1, 2, 3,])) ))␊
    `

> Error 1/1

    `␊
    > 1 | (( (([1,])).concat( (([2, 3])) ,) ))␊
        |             ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #10
      1 | (( (([1,])).concat( (([2, 3])) , bar ) ))

> Output

    `␊
      1 | (( (([1, 2, 3,])).concat( bar ) ))␊
    `

> Error 1/1

    `␊
    > 1 | (( (([1,])).concat( (([2, 3])) , bar ) ))␊
        |             ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #11
      1 | foo.concat(2)

> Output

    `␊
      1 | [...foo, 2]␊
    `

> Error 1/1

    `␊
    > 1 | foo.concat(2)␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #12
      1 | foo.concat([2, 3])

> Output

    `␊
      1 | [...foo, 2, 3]␊
    `

> Error 1/1

    `␊
    > 1 | foo.concat([2, 3])␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #13
      1 | foo.concat(2,)

> Output

    `␊
      1 | [...foo, 2]␊
    `

> Error 1/1

    `␊
    > 1 | foo.concat(2,)␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #14
      1 | foo.concat([2, 3],)

> Output

    `␊
      1 | [...foo, 2, 3]␊
    `

> Error 1/1

    `␊
    > 1 | foo.concat([2, 3],)␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #15
      1 | (( ((foo)).concat( (([2, 3])) ,) ))

> Output

    `␊
      1 | (( [...((foo)), 2, 3] ))␊
    `

> Error 1/1

    `␊
    > 1 | (( ((foo)).concat( (([2, 3])) ,) ))␊
        |            ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #16
      1 | (( ((foo)).concat( (([2, 3])) , bar ) ))

> Output

    `␊
      1 | (( [...((foo)), 2, 3].concat( bar ) ))␊
    `

> Error 1/1

    `␊
    > 1 | (( ((foo)).concat( (([2, 3])) , bar ) ))␊
        |            ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #17
      1 | bar()
      2 | foo.concat(2)

> Output

    `␊
      1 | bar()␊
      2 | ;[...foo, 2]␊
    `

> Error 1/1

    `␊
      1 | bar()␊
    > 2 | foo.concat(2)␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #18
      1 | const foo = foo.concat(2)

> Output

    `␊
      1 | const foo = [...foo, 2]␊
    `

> Error 1/1

    `␊
    > 1 | const foo = foo.concat(2)␊
        |                 ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #19
      1 | const foo = () => foo.concat(2)

> Output

    `␊
      1 | const foo = () => [...foo, 2]␊
    `

> Error 1/1

    `␊
    > 1 | const foo = () => foo.concat(2)␊
        |                       ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #20
      1 | const five = 2 + 3;
      2 | foo.concat(five);

> Output

    `␊
      1 | const five = 2 + 3;␊
      2 | [...foo, five];␊
    `

> Error 1/1

    `␊
      1 | const five = 2 + 3;␊
    > 2 | foo.concat(five);␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #21
      1 | const array = [2 + 3];
      2 | foo.concat(array);

> Output

    `␊
      1 | const array = [2 + 3];␊
      2 | [...foo, ...array];␊
    `

> Error 1/1

    `␊
      1 | const array = [2 + 3];␊
    > 2 | foo.concat(array);␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #22
      1 | foo.concat([bar])

> Output

    `␊
      1 | [...foo, bar]␊
    `

> Error 1/1

    `␊
    > 1 | foo.concat([bar])␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #23
      1 | foo.concat(bar)

> Error 1/1

    `␊
    > 1 | foo.concat(bar)␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    ␊
    --------------------------------------------------------------------------------␊
    Suggestion 1/2: First argument is an `array`.␊
      1 | [...foo, ...bar]␊
    ␊
    --------------------------------------------------------------------------------␊
    Suggestion 2/2: First argument is not an `array`.␊
      1 | [...foo, bar]␊
    `

## Invalid #24
      1 | Array.from(set).concat([2, 3])

> Output

    `␊
      1 | [...set, 2, 3]␊
    `

> Error 1/2

    `␊
    > 1 | Array.from(set).concat([2, 3])␊
        | ^^^^^^^^^^^^^^^ Prefer the spread operator over `Array.from(…)`.␊
    `

> Error 2/2

    `␊
    > 1 | Array.from(set).concat([2, 3])␊
        |                 ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #25
      1 | foo.concat([2, 3]).concat(4)

> Output

    `␊
      1 | [...foo, 2, 3, 4]␊
    `

> Error 1/2

    `␊
    > 1 | foo.concat([2, 3]).concat(4)␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

> Error 2/2

    `␊
    > 1 | foo.concat([2, 3]).concat(4)␊
        |                    ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #26
      1 | string.concat("bar")

> Output

    `␊
      1 | [...string, "bar"]␊
    `

> Error 1/1

    `␊
    > 1 | string.concat("bar")␊
        |        ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #27
      1 | foo.concat(2, 3)

> Output

    `␊
      1 | [...foo, 2, 3]␊
    `

> Error 1/1

    `␊
    > 1 | foo.concat(2, 3)␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #28
      1 | foo.concat(2, bar)

> Output

    `␊
      1 | [...foo, 2].concat(bar)␊
    `

> Error 1/1

    `␊
    > 1 | foo.concat(2, bar)␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #29
      1 | [...foo, 2].concat(bar)

> Error 1/1

    `␊
    > 1 | [...foo, 2].concat(bar)␊
        |             ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    ␊
    --------------------------------------------------------------------------------␊
    Suggestion 1/2: First argument is an `array`.␊
      1 | [...foo, 2, ...bar]␊
    ␊
    --------------------------------------------------------------------------------␊
    Suggestion 2/2: First argument is not an `array`.␊
      1 | [...foo, 2, bar]␊
    `

## Invalid #30
      1 | let sortedScores = scores.concat().sort((a, b) => b[0] - a[0]);

> Output

    `␊
      1 | let sortedScores = [...scores].sort((a, b) => b[0] - a[0]);␊
    `

> Error 1/1

    `␊
    > 1 | let sortedScores = scores.concat().sort((a, b) => b[0] - a[0]);␊
        |                           ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #31
      1 | foo.concat(bar, 2, 3)

> Error 1/1

    `␊
    > 1 | foo.concat(bar, 2, 3)␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    ␊
    --------------------------------------------------------------------------------␊
    Suggestion 1/2: First argument is an `array`.␊
      1 | [...foo, ...bar, 2, 3]␊
    ␊
    --------------------------------------------------------------------------------␊
    Suggestion 2/2: First argument is not an `array`.␊
      1 | [...foo, bar, 2, 3]␊
    `

## Invalid #32
      1 | foo.concat(bar, 2, 3, baz)

> Error 1/1

    `␊
    > 1 | foo.concat(bar, 2, 3, baz)␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    ␊
    --------------------------------------------------------------------------------␊
    Suggestion 1/2: First argument is an `array`.␊
      1 | [...foo, ...bar, 2, 3].concat(baz)␊
    ␊
    --------------------------------------------------------------------------------␊
    Suggestion 2/2: First argument is not an `array`.␊
      1 | [...foo, bar, 2, 3].concat(baz)␊
    `

## Invalid #33
      1 | async function a() {return [].concat(await bar)}

> Error 1/1

    `␊
    > 1 | async function a() {return [].concat(await bar)}␊
        |                               ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    ␊
    --------------------------------------------------------------------------------␊
    Suggestion 1/2: First argument is an `array`.␊
      1 | async function a() {return [...(await bar)]}␊
    ␊
    --------------------------------------------------------------------------------␊
    Suggestion 2/2: First argument is not an `array`.␊
      1 | async function a() {return [await bar]}␊
    `

## Invalid #34
      1 | async function a() {return [].concat(((await bar)))}

> Error 1/1

    `␊
    > 1 | async function a() {return [].concat(((await bar)))}␊
        |                               ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    ␊
    --------------------------------------------------------------------------------␊
    Suggestion 1/2: First argument is an `array`.␊
      1 | async function a() {return [...((await bar))]}␊
    ␊
    --------------------------------------------------------------------------------␊
    Suggestion 2/2: First argument is not an `array`.␊
      1 | async function a() {return [((await bar))]}␊
    `

## Invalid #35
      1 | foo.concat((0, 1))

> Output

    `␊
      1 | [...foo, (0, 1)]␊
    `

> Error 1/1

    `␊
    > 1 | foo.concat((0, 1))␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #36
      1 | async function a() {return (await bar).concat(1)}

> Output

    `␊
      1 | async function a() {return [...(await bar), 1]}␊
    `

> Error 1/1

    `␊
    > 1 | async function a() {return (await bar).concat(1)}␊
        |                                        ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #37
      1 | [].concat(...bar)

> Error 1/1

    `␊
    > 1 | [].concat(...bar)␊
        |    ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #38
      1 | [].concat([,], [])

> Output

    `␊
      1 | [,]␊
    `

> Error 1/1

    `␊
    > 1 | [].concat([,], [])␊
        |    ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #39
      1 | [,].concat([,], [,])

> Output

    `␊
      1 | [, , ,]␊
    `

> Error 1/1

    `␊
    > 1 | [,].concat([,], [,])␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #40
      1 | [,].concat([,,], [,])

> Output

    `␊
      1 | [, ,, ,]␊
    `

> Error 1/1

    `␊
    > 1 | [,].concat([,,], [,])␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #41
      1 | [,].concat([,], [,,])

> Output

    `␊
      1 | [, , ,,]␊
    `

> Error 1/1

    `␊
    > 1 | [,].concat([,], [,,])␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #42
      1 | [1].concat([2,], [3,])

> Output

    `␊
      1 | [1, 2, 3,]␊
    `

> Error 1/1

    `␊
    > 1 | [1].concat([2,], [3,])␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #43
      1 | [1].concat([2,,], [3,,])

> Output

    `␊
      1 | [1, 2,, 3,,]␊
    `

> Error 1/1

    `␊
    > 1 | [1].concat([2,,], [3,,])␊
        |     ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #44
      1 | [1,].concat([2,], [3,])

> Output

    `␊
      1 | [1, 2, 3,]␊
    `

> Error 1/1

    `␊
    > 1 | [1,].concat([2,], [3,])␊
        |      ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #45
      1 | [1,].concat([2,,], [3,,])

> Output

    `␊
      1 | [1, 2,, 3,,]␊
    `

> Error 1/1

    `␊
    > 1 | [1,].concat([2,,], [3,,])␊
        |      ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #46
      1 | [].concat([], [])

> Output

    `␊
      1 | []␊
    `

> Error 1/1

    `␊
    > 1 | [].concat([], [])␊
        |    ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
    `

## Invalid #47
       1 | const EMPTY_STRING = ""
       2 | const EMPTY_STRING_IN_ARRAY = ""
       3 | const EMPTY_STRING_IN_ARRAY_OF_ARRAY = ""
       4 | const array = [].concat(
       5 | 	undefined,
       6 | 	null,
       7 | 	EMPTY_STRING,
       8 | 	false,
       9 | 	0,
      10 | 	[EMPTY_STRING_IN_ARRAY],
      11 | 	[[EMPTY_STRING_IN_ARRAY_OF_ARRAY]]
      12 | )

> Output

    `␊
      1 | const EMPTY_STRING = ""␊
      2 | const EMPTY_STRING_IN_ARRAY = ""␊
      3 | const EMPTY_STRING_IN_ARRAY_OF_ARRAY = ""␊
      4 | const array = [undefined, null, EMPTY_STRING, false, 0, EMPTY_STRING_IN_ARRAY, [EMPTY_STRING_IN_ARRAY_OF_ARRAY]]␊
    `

> Error 1/1

    `␊
       1 | const EMPTY_STRING = ""␊
       2 | const EMPTY_STRING_IN_ARRAY = ""␊
       3 | const EMPTY_STRING_IN_ARRAY_OF_ARRAY = ""␊
    >  4 | const array = [].concat(␊
         |                  ^^^^^^ Prefer the spread operator over `Array#concat(…)`.␊
       5 | 	undefined,␊
       6 | 	null,␊
       7 | 	EMPTY_STRING,␊
       8 | 	false,␊
       9 | 	0,␊
      10 | 	[EMPTY_STRING_IN_ARRAY],␊
      11 | 	[[EMPTY_STRING_IN_ARRAY_OF_ARRAY]]␊
      12 | )␊
    `
