# simple-latex-checker

This was created to help debug the __most common problem__ students face when trying to download their jupyter Notebooks as PDFs, erroneous spaces in their in-line latex. I spun this up in a few hours, so it would definitely be useful to add a few more features. 

To use:

1. Download the package

`pip install simple-latex-checker`

2. Import the package into your jupyter notebook

`import simple_latex_checker as slc`

3. Run the check

  - If you only want to check the latex bug, run this:

      `slc.run_check("<Your Notebook Name>.ipynb")`

  - If you want to check the latex bug, and that the number of cells matches what is expected (for otter autograder):
    
      - Add this Markdown cell at the very end
        
          `$ 1+1=2$`
    
      - Then run
        
          `slc.run_check("<Your Notebook Name>.ipynb", 0)`
        
          This will print the (expected number of cells + 1)

      - You can then run:

          `slc.run_check("<Your Notebook Name>.ipynb", <Expected Number of cells>)`
      
