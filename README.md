def calculate_npv(discount_rate, cash_flows):
    npv = 0
    for t in range(len(cash_flows)):
        npv += cash_flows[t] / (1 + discount_rate) ** t
    return npv

# Example usage
discount_rate = 0.1  # 10%
cash_flows = [-1000, 200, 300, 400, 500]  # Initial investment and subsequent cash flows

npv = calculate_npv(discount_rate, cash_flows)
print(f"The NPV of the project is: {npv:.2f}")

