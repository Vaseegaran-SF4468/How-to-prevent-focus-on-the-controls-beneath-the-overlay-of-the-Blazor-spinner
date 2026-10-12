# How to Prevent Focus on Controls Beneath a Blazor Spinner Overlay

## Overview

This sample demonstrates how to prevent users from interacting with or tabbing into UI elements that are visually covered by a loading overlay while a Syncfusion [Blazor Spinner](https://www.syncfusion.com/blazor-components/blazor-spinner) is displayed. Preventing focus from reaching underlying controls helps maintain a consistent user experience and improves accessibility during loading or processing operations.

The repository shows a Blazor application that displays a Spinner overlay and blocks access to controls beneath it until the loading operation is complete. This approach helps avoid unexpected keyboard navigation and user actions while the application is in a busy state.

## Key Features

- Uses the Syncfusion `SfSpinner` component to display a loading overlay during processing operations.
- Binds the Spinner visibility through the `@bind-Visible` property to dynamically show or hide the overlay.
- Applies the Spinner `Label="Loading"` property to provide an accessible loading message for users.
- Uses the `CssClass="e-spin-overlay"` property to render the Spinner as an overlay that covers underlying content.
- Configures `ZIndex="1000"` to ensure the Spinner overlay remains above all interactive page elements.
- Demonstrates programmatic Spinner control using an `SfSpinner` component reference (`@ref`).
- Shows user interaction with Syncfusion `SfButton` and `SfTextBox` components while validating focus behavior beneath the overlay.
- Uses Blazor event handling (`@onclick`) to activate the loading overlay when the button is clicked.
- Invokes JavaScript through `IJSRuntime.InvokeAsync()` to manage DOM accessibility and focus behavior while the Spinner is active.
- Implements accessibility-related attributes including `role="dialog"`, `aria-modal="true"`, and `tabindex="-1"` to support focus containment and prevent unintended navigation to covered controls.
- Demonstrates a practical approach for blocking keyboard focus on underlying UI elements while asynchronous operations are in progress.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone or download this repository.
2. Open `SpinnerOverlay.sln`.
3. Restore all NuGet packages.
4. Build the solution.
5. Run the application using `Ctrl+F5`.

**Visual Studio Code**

1. Open the repository folder in Visual Studio Code.
2. Navigate to the project directory.

```bash
dotnet restore
dotnet run
```

3. Open the URL displayed in the terminal after the application starts.

## Project Structure

- `Pages/Index.razor` - Main demonstration page containing the `SfSpinner`, `SfButton`, and `SfTextBox` components, Spinner visibility binding, accessibility attributes, and JavaScript interop used to prevent focus on controls beneath the overlay.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Official Spinner documentation: https://blazor.syncfusion.com/documentation/spinner/getting-started

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.