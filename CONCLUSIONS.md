The tests were conducted on two different articles with both existing and non-existing substrings. Here are the key conclusions based on the data:

Summary of Results
Existing Substring:

Article 1:
Boyer-Moore: 0.010857 seconds
Knuth-Morris-Pratt: 0.035397 seconds
Rabin-Karp: 0.056896 seconds
Article 2:
Boyer-Moore: 0.012978 seconds
Knuth-Morris-Pratt: 0.063642 seconds
Rabin-Karp: 0.088302 seconds
Non-Existing Substring:

Article 1:
Boyer-Moore: 0.012217 seconds
Knuth-Morris-Pratt: 0.085013 seconds
Rabin-Karp: 0.119839 seconds
Article 2:
Boyer-Moore: 0.012417 seconds
Knuth-Morris-Pratt: 0.098722 seconds
Rabin-Karp: 0.129539 seconds
Conclusions
Boyer-Moore Algorithm:

This algorithm consistently performed the fastest in all scenarios, both for existing and non-existing substrings in both articles.
It shows significant efficiency, making it a preferred choice for string search operations, especially when dealing with large texts.
Knuth-Morris-Pratt Algorithm:

The Knuth-Morris-Pratt (KMP) algorithm performed better than Rabin-Karp but was slower than Boyer-Moore in all cases.
The difference in execution time between existing and non-existing substrings was noticeable, with non-existing substrings taking slightly longer.
Rabin-Karp Algorithm:

Rabin-Karp was the slowest among the three algorithms across all test scenarios.
The algorithm's performance was significantly impacted by the presence of non-existing substrings, resulting in the highest execution times.
Efficiency Analysis
Existing Substring Efficiency:

Boyer-Moore's efficiency can be attributed to its heuristic nature, which skips sections of the text, leading to faster search times.
KMP, while not as fast as Boyer-Moore, still maintains reasonable performance due to its preprocessing step that builds a partial match table.
Rabin-Karp's hashing mechanism, while useful for detecting potential matches, incurs overhead, especially when confirming false positives.
Non-Existing Substring Efficiency:

The performance of Boyer-Moore remains strong even with non-existing substrings, demonstrating its robustness.
KMP's performance degrades slightly, but it remains predictable due to its linear complexity in the worst case.
Rabin-Karp shows the most significant slowdown, highlighting its less optimal performance for scenarios with many hash collisions or non-matching substrings.
Final Remarks
Best Overall Performance: Boyer-Moore is the best overall performer and is recommended for most practical applications involving substring search due to its superior speed and efficiency.
Balanced Performance: Knuth-Morris-Pratt provides a good balance between preprocessing time and search efficiency, making it suitable for applications where preprocessing time is less of a concern.
Specific Use-Cases: Rabin-Karp may still be useful in specific scenarios, such as multiple pattern searches, but generally performs the worst in this comparison.
These conclusions highlight the strengths and weaknesses of each algorithm, guiding their application based on specific requirements and constraints.
