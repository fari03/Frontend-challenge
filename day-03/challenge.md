// index.js

// Function to find the distance value between two arrays
export const findTheDistanceValue = (arr1, arr2, d) => {
    let distanceValue = 0;
  
    for (let i = 0; i < arr1.length; i++) {
      let valid = true;
  
      for (let j = 0; j < arr2.length; j++) {
        if (Math.abs(arr1[i] - arr2[j]) <= d) {
          valid = false;
          break;
        }
      }
  
      if (valid) {
        distanceValue++;
      }
    }
  
    return distanceValue;
  };
  
