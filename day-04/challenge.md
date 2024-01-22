// curry.js

// Curry function that takes a function as an argument
const curry = (func) => {
	// Store the original function's arity (number of parameters)
	const arity = func.length;
  
	// Internal recursive function to build up the curried function
	const curried = (...args) => {
	  // If enough arguments are provided, call the original function
	  if (args.length >= arity) {
		return func(...args);
	  }
  
	  // If not enough arguments are provided, return a curried function
	  return (...nextArgs) => curried(...args, ...nextArgs);
	};
  
	return curried;
  };
  
  export default curry;
  
