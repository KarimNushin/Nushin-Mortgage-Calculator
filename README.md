# Nushin Mortgage Calculator

A desktop mortgage calculator built in **Java 17 + Swing** by **Karim Nushin**.

It estimates a home buyer's monthly housing payment and generates a full amortization schedule.

## Features

- Home price and down payment
- Interest rate and loan term
- Monthly principal + interest
- Property tax estimate
- Homeowners insurance estimate
- HOA and PMI inputs
- Total estimated monthly housing payment
- Total interest over the loan term
- Full month-by-month amortization schedule
- Export amortization schedule to CSV
- No third-party runtime libraries

## Tech

- Java 17
- Java Swing
- Maven project structure

## Run in IntelliJ IDEA

1. Open this folder as a project.
2. Make sure Project SDK is Java 17 or newer.
3. Run:

`src/main/java/com/karimnushin/mortgage/MortgageCalculatorApp.java`

## Run from the command line without Maven

From the project folder:

```bash
mkdir out
javac -d out src/main/java/com/karimnushin/mortgage/*.java
java -cp out com.karimnushin.mortgage.MortgageCalculatorApp
```

On Windows PowerShell, the same commands work if Java is installed and available in PATH.

## Build with Maven

```bash
mvn package
java -jar target/nushin-mortgage-calculator-1.0.0.jar
```

## Mortgage formula

For a fixed-rate mortgage, the calculator uses the standard amortizing-loan payment formula:

```text
M = P × [ r(1+r)^n / ((1+r)^n - 1) ]
```

where:

- `M` = monthly principal and interest payment
- `P` = loan principal
- `r` = monthly interest rate
- `n` = number of monthly payments

When the interest rate is 0%, the calculator divides principal evenly across the loan term.

## Example

A $650,000 home with a $130,000 down payment, 6.50% interest rate, and a 30-year term is preloaded as the example scenario. Add local taxes, insurance, HOA, and PMI to estimate the total monthly housing payment.

## Disclaimer

This project is for educational and planning purposes only. Actual lender calculations, APR, closing costs, taxes, insurance, escrow requirements, PMI, HOA fees, and payment amounts may vary.

---

Built by **Karim Nushin**
