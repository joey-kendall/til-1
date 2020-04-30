# Expect a function with parameters to throw an exception
If we want to expect a function to throw an exception for certain input parameters, the key point is that we must pass in a function definition and not call our function inside the expect. The code is below for an example of a function which should throw an exception for negative integer inputs:

func.js:
```
const func = (n) => {
  if (n < 0) {
    throw new Error("negative input")
  }
  return n
}

module.exports = func
```
func.spec.js:
```
const func = require('./func.js')

describe('exception test', () => {
  it('should throw an exception', () => {
    expect(
    () => func(-1) // **Do not simply call func**
    ).toThrow()
  })
})
```
We pass an anonymous function to expect, which will throw for the input. Expect can then determine that this function will throw.
