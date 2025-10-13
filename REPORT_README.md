# EN3160 Assignment 2 Report

## Report Structure

The LaTeX report (`report.tex`) is a 4-page academic document covering all four questions of the assignment:

1. **Question 1**: Blob Detection Using Laplacian of Gaussian (LoG)
2. **Question 2**: RANSAC for Line and Circle Fitting
3. **Question 3**: Homography-Based Image Warping
4. **Question 4**: Image Stitching with SIFT and RANSAC

## Compiling the Report

### Using pdfLaTeX (Recommended)

```bash
pdflatex report.tex
pdflatex report.tex  # Run twice for proper cross-references
```

### Using Online LaTeX Editors

1. **Overleaf**: Upload `report.tex` to [Overleaf](https://www.overleaf.com)
2. **ShareLaTeX**: Upload to ShareLaTeX
3. Click "Recompile" to generate PDF

### Using VS Code with LaTeX Workshop

1. Install the LaTeX Workshop extension
2. Open `report.tex`
3. Press `Ctrl+Alt+B` (or `Cmd+Option+B` on Mac) to build
4. View PDF with `Ctrl+Alt+V`

### Using MikTeX (Windows)

```powershell
pdflatex report.tex
```

### Using TeXLive (Linux/Mac)

```bash
pdflatex report.tex
```

## Required LaTeX Packages

The report uses these packages (usually included in standard LaTeX distributions):

- `geometry` - page margins
- `graphicx` - image inclusion
- `amsmath` - mathematical equations
- `listings` - code syntax highlighting
- `xcolor` - colors for code
- `hyperref` - hyperlinks and PDF bookmarks
- `subcaption` - subfigures
- `float` - figure positioning

## Adding Images to the Report

To include actual images from your notebook outputs:

1. **Save images from notebook** (add these cells to your notebook):

```python
# After running blob detection (Question 1)
cv.imwrite('sunflower_detection.png', out)

# After RANSAC line/circle (Question 2)
plt.savefig('ransac_line_circle.png', dpi=150, bbox_inches='tight')

# After homography warping (Question 3)
cv.imwrite('homography_warp.png', out)

# After stitching (Question 4)
cv.imwrite('stitching_result.png', out)
```

2. **Uncomment the image lines in LaTeX**:

In `report.tex`, find lines like:

```latex
% \includegraphics[width=0.8\textwidth]{sunflower_detection.png}
```

Remove the `%` to activate:

```latex
\includegraphics[width=0.8\textwidth]{sunflower_detection.png}
```

## Report Features

### Content Included

- ✅ Detailed methodology for each question
- ✅ Mathematical formulations and equations
- ✅ Code listings with syntax highlighting
- ✅ Results and parameter values
- ✅ Discussion and analysis
- ✅ Comparison of methods
- ✅ Figure placeholders for all outputs

### Writing Style

The report is written in a student-appropriate academic style:

- Clear and accessible language
- Not overly formal or complex
- Explains reasoning and decisions
- Discusses challenges and solutions
- Appropriate for undergraduate/graduate coursework

### Structure

1. **Introduction** - Overview of all tasks
2. **Question 1** - LoG blob detection methodology, implementation, results, discussion
3. **Question 2** - RANSAC fitting, includes "circle first" discussion
4. **Question 3** - Homography warping with rationale for image choice
5. **Question 4** - SIFT matching and stitching with homography comparison
6. **Conclusion** - Learning outcomes and key takeaways

## Customization

### Adjusting Page Count

To make the report longer or shorter:

- **Expand**: Add more detailed explanations, additional experiments, parameter sensitivity analysis
- **Compress**: Remove some code listings, make figures smaller, reduce discussion sections

### Modifying Content

Feel free to edit:

- Replace placeholder values with your actual results
- Add your own observations and insights
- Include additional experiments or variations
- Adjust figure captions and references

## Troubleshooting

### Common Issues

**"File not found" errors**: Make sure all image files are in the same directory as `report.tex`

**Missing packages**: Install full LaTeX distribution (MikTeX or TeXLive)

**Code formatting issues**: Check that special characters in listings are properly escaped

**Figure placement**: Use `[H]` option in `\begin{figure}[H]` for exact positioning

## Export Options

After compiling, you'll have:

- `report.pdf` - The final report document
- `report.aux`, `report.log` - Auxiliary files (can be deleted)

To submit, typically you only need `report.pdf`.

## Questions?

If you encounter issues compiling or want to modify the report structure, check:

- LaTeX distribution is properly installed
- All required packages are available
- Image files are in the correct location
- No special characters are breaking the LaTeX syntax
