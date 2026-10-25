# Mission 8 — Does This Problem Actually Need ML?

## 1. Example: Detecting Low Battery

Imagine creating a system that alerts a user when their phone battery becomes low.

| Aspect            | Traditional Programming                                 | Machine Learning                                                      |
| ----------------- | ------------------------------------------------------- | --------------------------------------------------------------------- |
| Working method    | Display an alert when battery level drops below 20%     | Learn battery usage patterns to estimate when the battery may run out |
| Requirements      | Current battery percentage                              | Historical battery usage and charging data                            |
| Main advantage    | Simple and predictable                                  | Can estimate future battery behaviour                                 |
| Main drawback     | Cannot estimate future usage by itself                  | Requires suitable data and may produce inaccurate estimates           |
| Possible failure  | Incorrect battery readings trigger the wrong alert      | Changing usage habits reduce prediction accuracy                      |
| Performance check | Verify whether the alert appears at the specified level | Compare predicted battery life with actual results                    |

## 2. Which Solution Is Better?

For a basic low-battery alert, a fixed rule is sufficient because the required condition is already known.

Machine learning becomes more useful when the goal is to estimate remaining battery life based on usage patterns, background applications, and other factors.

## 3. Checklist Before Using ML

1. **Define the goal:** Identify the exact problem to solve.
2. **Try simple methods:** Check whether ordinary programming can handle it.
3. **Examine the data:** Ensure relevant and reliable examples are available.
4. **Determine the output:** Decide what the system must predict.
5. **Measure performance:** Choose a suitable way to evaluate the result.
6. **Assess the risks:** Consider the consequences of incorrect predictions.

## Conclusion

Machine learning is useful when learning patterns from data provides an advantage over fixed rules. For straightforward problems with clearly defined conditions, traditional programming is often the simpler and more reliable option.

## Sources

Refer to `sources.md` for Google's resources on framing machine-learning problems.
