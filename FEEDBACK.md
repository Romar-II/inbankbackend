




Would suggest to rewrite loan amount check and loan period check, in verifyInputs method, to avoid negations
and put them in a separate method with proper names to improve code readability.

For example:

if (loanAmount>DecisionEngineConstants.MAXIMUM_LOAN_AMOUNT
|| loanAmount<DecisionEngineConstants.MINIMUM_LOAN_AMOUNT) {
throw new InvalidLoanAmountException("Invalid loan amount!");
}

if (loanPeriod > DecisionEngineConstants.MAXIMUM_LOAN_PERIOD
|| loanPeriod < DecisionEngineConstants.MINIMUM_LOAN_PERIOD) {
throw new InvalidLoanPeriodException("Invalid loan period!");
}

