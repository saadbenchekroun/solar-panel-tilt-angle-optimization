# Solar Panel Tilt Angle Optimization

This project demonstrates the use of mathematical methods to optimize the tilt angle of solar panels for maximum efficiency. We use a polynomial model to represent the solar panel efficiency as a function of the tilt angle and implement both Lagrange interpolation and the Dichotomy method for root finding.
![solar](https://github.com/user-attachments/assets/a4d922e9-7e58-41c2-b321-14a12fd1cee5)


## Project Structure

- `racinef.m`: Plots the efficiency of the solar panel as a function of the tilt angle.
- `lagrange.m`: Implements Lagrange interpolation to predict solar efficiency at intermediate tilt angles.
- `dichotomie.m`: Finds the optimal tilt angle using the Dichotomy (Bisection) method.

## How It Works

1. **Plotting Solar Efficiency**: `racinef.m` generates a plot of the solar panel efficiency over a range of tilt angles (0° to 90°). The efficiency curve is modeled using a polynomial approximation.

2. **Lagrange Interpolation**: `lagrange.m` allows us to estimate the efficiency of the solar panel at any tilt angle, even if we only have data for a few angles. For example, if we know the efficiency at 0°, 30°, 60°, and 90°, we can use this method to estimate the efficiency at 45°.

3. **Dichotomy Method for Optimization**: `dichotomie.m` uses the Bisection method to find the tilt angle that maximizes the solar panel efficiency. The method works by finding the root of the derivative of the efficiency function.

## How to Run the Code

1. Open MATLAB.
2. Run `racinef.m` to visualize the solar panel efficiency curve.
3. Use `lagrange.m` to predict solar efficiency at specific tilt angles.
4. Use `dichotomie.m` to find the optimal tilt angle for your solar panel installation.

## Example

- Plot the efficiency curve using `racinef.m`.
- Predict the efficiency at 45° using `lagrange.m`:
    ```
    angles = [0, 30, 60, 90];
    efficiency = [0.5, 0.75, 0.8, 0.6];
    predicted_efficiency = lagrange(angles, efficiency, 45);
    ```
- Find the optimal tilt angle using `dichotomie.m`:
    ```
    [optimal_angle, iterations] = dichotomie(20, 70, 1e-4);
    ```

## License

This project is licensed under the GNU General Public License.
