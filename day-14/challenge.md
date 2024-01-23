/**
 * Returns a boolean value for whether the owner should be alerted
 * @param {number} durationInWarehouse
 * @param {number} temperature
 * @returns {Boolean}
 */
export function shouldAlertOwner(durationInWarehouse, temperature) {
    const CRITICAL_TEMPERATURE = 30; // °C
    const SECONDARY_TEMPERATURE = 25; // °C
    const CRITICAL_DURATION = 7; // Days

    // Check if the temperature exceeds CRITICAL_TEMPERATURE
    const isCriticalTemperature = temperature > CRITICAL_TEMPERATURE;

    // Check if the durationInWarehouse is more than CRITICAL_DURATION
    // and if the temperature exceeds SECONDARY_TEMPERATURE
    const isSecondaryTemperature =
        durationInWarehouse > CRITICAL_DURATION && temperature > SECONDARY_TEMPERATURE;

    // Return true if either of the conditions is met
    return isCriticalTemperature || isSecondaryTemperature;
}

// Sample Tests

console.log(shouldAlertOwner(5, 26)); // Expected Output: false
console.log(shouldAlertOwner(8, 26)); // Expected Output: true
console.log(shouldAlertOwner(8, 32)); // Expected Output: true
