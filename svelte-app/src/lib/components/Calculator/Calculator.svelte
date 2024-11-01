<script>
    let weight = '';
    let height = '';
    let bmi = null;
    let message = '';

    function calculateBMI() {
        const heightInMeters = height / 100;
        bmi = (weight / (heightInMeters * heightInMeters)).toFixed(2);
        if (bmi < 18.5) {
            message = 'Underweight';
        } else if (bmi < 24.9) {
            message = 'Normal weight';
        } else if (bmi < 29.9) {
            message = 'Overweight';
        } else if(bmi >= 30) {
            message = 'Obesity';
        } else {
            message = 'Geen geldige BMI';
        }
    }
</script>



<div class="calculator">
    <h2>BMI Calculator</h2>
    <div>
        <label for="weight">Weight (kg):</label>
        <input type="number" id="weight" bind:value={weight} />
    </div>
    <div>
        <label for="height">Height (cm):</label>
        <input type="number" id="height" bind:value={height} />
    </div>
    <button on:click={calculateBMI}>Calculate BMI</button>
    {#if bmi}
        <div class="result">
            <p>Your BMI is: {bmi}</p>
            <p>{message}</p>
        </div>
    {/if}
    {#if bmi === null}
        <p>Please enter your weight and height to calculate your BMI.</p>
    {/if}
</div>

<style>
    .calculator {
        max-width: 300px;
        margin: auto;
        padding: 1em;
        border: 1px solid #ccc;
        border-radius: 5px;
    }
    .result {
        margin-top: 1em;
    }
</style>
