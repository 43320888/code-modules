# Get Unique Class Name
## Description 
The script creates a random class name and returns the result as a string.
The script is optimized and is able to generate an infinite number of random lines very quickly (lightning fast).

⏰ The result of the last benchmark:
- 13 million 631 thousand 540 strings were created in 15968ms.
Try it: `
const set = new Set();

function bench(f) {
	let start = Date.now();
	for (let i = 0; i < 13631540; i++) set.add(f());

	return Date.now() - start;
}

alert( 'A set of unique classes of 13631540 pieces created for: ' + bench(getUniqueClassName) + 'ms' );
alert( 'The size of the unique collection should be 13631540 pieces: ' + [...set].length + 'pieces' );
`

The feature of work:
For the class name, as the first character, an array of 52 Latin letters is generated. Then the array is shuffled randomly.

Each call to the getUniqueClassName () method removes one element of the array and returns it as a result.

When the last element in the array ends, the cycle repeats with the creation of a new array of 52 Latin letters for the first character, to which is added an array of 64 Latin letters, numbers and signs "-", "_" for all subsequent characters.
Before returning, each newly created array is shuffled randomly.
## Installation & Use, Assistance, Credits, License
For that, read [Readme](https://github.com/hacking-logbook/code-modules) above, please: https://github.com/hacking-logbook/code-modules