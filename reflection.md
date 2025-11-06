1.	Which issues were the easiest to fix, and which were the hardest? Why?
Ans:
Easiest: Naming conventions and docstrings - just renaming and adding descriptions.
Hardest: Mutable default argument (logs=[]) - required understanding Python logic and changing function behavior.

2.	Did the static analysis tools report any false positives? If so, describe one example.
Ans:
Yes. The global statement warning was a false positive. We need global stock_data for all functions to access the same data. Removing it would require major code refactoring.

3.	How would you integrate static analysis tools into your actual software development workflow? Consider continuous integration (CI) or local development practices.
Ans: 
Run tools locally before committing code. Set up CI/CD pipeline (GitHub Actions) to automatically check all pull requests. Block merges if code quality score is too low.

4.	What tangible improvements did you observe in the code quality, readability, or potential robustness after applying the fixes?
Ans:
Score improved from 4.80/10 to 10/10. Removed security risk (eval). Fixed error handling (specific exceptions). Added docstrings for clarity. Code is now production-ready.