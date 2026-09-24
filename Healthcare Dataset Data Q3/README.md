Q)Change Made
1)Removed 534 Duplicate Rows
2)Corrected 108 Negative Billing Amounts (abs())
3)Engineered Length_of_Stay Field

Q)Why Was It Necessary?
Identical records inflate total counts, artificially distorting patient admission volume, total billing calculations, and bed utilization metrics.

Billing amounts cannot be negative in administrative admission logs; these reflect negative sign entry artifacts or ledger debit adjustments.

Admission and discharge dates alone do not provide direct quantitative measures for hospital stay durations or bed turnaround efficiency.

Q)What Would Happen If You Didn't Do It?
Admission numbers and total revenue would be overstated, resulting in inaccurate hospital capacity planning and skewed financial forecasts.

Aggregate revenue calculations would be erroneously understated, and average cost estimations per condition would be skewed downwards.

Operational analysis of patient stay duration across departments or admission types would require complex manual calculations in downstream visualizations