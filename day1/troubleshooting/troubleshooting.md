# Suggestions for troubleshooting your code

## Identify the problem before searching for the solution.

- Work in a copy of your script or notebook
- Start at the top of the script or notebook
- Write print statements or run the code in chunks until you get the error
- If necessary, you can comment out code chunks, and run the code again to see if that helps identify the location of the error.
- Check that each code chunk does what you expect (e.g., using print statements), working top to bottom, ruling out chunks that perform properly.

## Your problem probably falls into one of these two buckets:

1. I just wrote it and it doesn't work.

    - I'm getting an error message, but I'm not sure what the error is.
        - Look it up online or with an LLM. Do you see anything that sounds right?
        - Start debugging.

   - It's not doing what I want it to.
      - Start debugging.
      - Could there be differences in your data? (some rows aren't formatted the same way as others, you have missing data in some places that you didn't notice, distributions vary, etc.)
        - Try using print statements inside loops to see if every row looks the same. You might print the actual data, or lengths of rows, something to look for differences.
        - Try creating a shorter version of your dataset with only a few rows – does that work the way you want?

2. It used to work, but now it doesn't.

   - Did you change anything in the code recently?
      - Start debugging just above the changed code.

   - Are you using a different data set?
      - Look at the raw data - how is the new dataset different from the old?
      - Try using print statements inside loops to see if every row looks the same. You might print the actual data, or lengths of rows, something to look for differences.
      - Try creating a shorter version of your dataset with only a few rows – does that work the way you want?

   - Are you running it on a different system? Local vs. server, script vs. Jupyter notebook, local Jupyter vs. colab, new laptop, etc.
      - Can you test it again on the old system?

   - Has it been a while since the last time you ran it?
      - Has Python or Anaconda updated?
      - Has a package updated? (might not be the package that's giving you an error – might be a dependency)
