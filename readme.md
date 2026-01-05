# FluxionViz: Function & Derivative Visualizer

FluxionViz is an interactive web-based tool designed to visualize mathematical functions and their derivatives simultaneously. 

## The Story Behind This Project

I originally created this tool to help my son with his mathematics studies. Understanding calculus, specifically the relationship between a function and its derivatives, can be challenging without visual aids. I wanted to build something that would allow him to "play" with functions—tweak them, see the slopes change in real-time, and intuitively grasp the concepts of differentiation.

I am releasing this project to the public in the hopes that it might be useful to other students, teachers, and parents who are navigating the fascinating world of calculus.

## Features

- **Real-time Visualization**: Instantly see the graph of any mathematical function $f(x)$.
- **Automatic Differentiation**: The tool automatically calculates and plots the derivative $f'(x)$ (and higher-order derivatives) using symbolic differentiation.
- **Interactive Tangent Lines**: Hover over any point on the curve to see the tangent line and the exact slope value at that point.
- **Synchronized Views**: Moving your mouse over one chart automatically updates the pointer and values on all other synchronized derivative charts.
- **Dynamic Animation**: A built-in "play" mode animates the point moving across the function, allowing you to observe how the slope evolves over time.
- **Flexible & Extendable**: You can add multiple levels of derivatives (e.g., $f''(x)$, $f'''(x)$) dynamically.
- **Multi-language Support**: Fully localized in English (🇺🇸) and Korean (🇰🇷).
- **External Learning Tools**: Buttons to instantly query Google AI or WolframAlpha for deeper insights about the function.
- **Domain-Aware Visualization**: Distinctly visualizes regions where the function is undefined (e.g., negative domain for `log(x)`) using grayed-out traces.
- **Session History**: Automatically saves and restores your last used function, so you can pick up right where you left off.
- **Smart Axis Scaling**: Intelligently adjusts the viewing range to handle both diverging functions (like `tan(x)`) and bounded functions gracefully.
- **Performance Optimized**: Uses compiled expressions for instantaneous evaluation even with complex formulas.
- **Math Notation**: Properly renders mathematical formulas using LaTeX formatting for clear reading.

## Limitations & Disclaimer

This project, **FluxionViz**, is a visualization tool designed for **educational purposes**. 
It relies on numerical methods (JavaScript `Math.js` & `Plotly.js`) which may introduce discrepancies from pure mathematical theory.

**Known Limitations:**
1. **Floating Point Errors:** Tiny calculation errors may occur near zero or extremely large numbers.
2. **Discontinuities:** While we try to handle asymptotes, some vertical lines may appear where graphs should be discontinuous.
3. **Non-differentiable Points:** Points where a function is not differentiable (e.g., sharp corners or cusps) are not explicitly marked or handled as undefined, which might lead to misleading visual results in derivative graphs.
4. **Y-Axis Auto-Scaling**: The current logic uses percentile-based filtering (approx. top/bottom 3%) to handle functions with extreme values (like `tan(x)`). However, this approach can sometimes inadvertently crop valid ranges for bounded functions (e.g., semi-circles or functions starting exactly at 0).
5. **Device Compatibility**: This tool is optimized for **Desktop/PC** environments. Features like hover-based tangent visualization require a mouse cursor and may not function optimally on touch devices (smartphones/tablets).

Please use this tool to build intuition, but rely on formal mathematical proofs for strict definitions.

**Disclaimer:**
- This tool is for educational use only and is not a rigorous mathematical proof tool.
- Due to the nature of floating-point arithmetic, there may be slight errors or representation issues in undefined regions.
- The author provides this tool "as is" and is not responsible for any issues arising from its use (e.g., errors in homework).

## Tech Stack

This is a **single-file** application with no backend requirements. It runs entirely in your browser using:

- **HTML5 & Vanilla JavaScript**: for the core logic and structure.
- **Plotly.js**: for high-performance, interactive charting.
- **Math.js**: for powerful symbolic differentiation and expression parsing.
- **KaTeX**: for fast and beautiful rendering of mathematical notations.
- **Tailwind CSS**: for a modern, responsive user interface.
- **Google Fonts (Inter)**: for clean typography.

## How to Use

1.  **Open the File**: Simply open `index.html` in any modern web browser. No installation or server is required.
2.  **Enter a Function**: Type a mathematical expression (e.g., `x^3 - 2x`, `sin(x)`, `x * exp(x)`) in the input field.
3.  **Explore**:
    -   Move your mouse over the graph to inspect values and slopes.
    -   Use the scroll wheel to zoom the X-axis in and out.
    -   Click **"+ Add Derivative"** to see the next order derivative.
4.  **Animate**: Use the slider to control the playback speed and watch the relationship between the function and its derivatives unfold.

## Examples to Try

-   **Polynomials**: `x^3 - 3x + 2` (Watch where the slope is zero!)
-   **Trigonometry**: `sin(x)` (Notice how the derivative is `cos(x)`)
-   **Exponential**: `exp(x)` (The function that is its own derivative)
-   **Logarithmic**: `log(x)` (See the behavior near x=0)
-   **Non-differentiable**: `abs(x)` (Note: Visual indication for non-differentiable points is not yet implemented)

## Acknowledgments

This project was built with the assistance of LLMs **Gemini** and **Claude**, which served as virtual pair programmers throughout the development process.

## License

This project is open-sourced under the **MIT License**. You are free to use, modify, and distribute it.

---

*Created with love for math learners everywhere.*
