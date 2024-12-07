# Onboarding Sample

This sample mostly references the last example shown in the SettingsExpander page in the Windows Community Toolkit sample app.

## Step 1: Create new WinUI project
1. In "Create new project", search 'WinUI' and select 'Blank App, Packaged (WinUI 3 Desktop)'.

## Step 2: Install WinUI Community Toolkit packages via NuGet installer
1. Install `CommunityToolkit.WinUI.Controls.SettingsControls`.
2. Make sure the version is using [v8.2.241112-preview1](https://github.com/CommunityToolkit/Windows/releases/tag/v8.2.241112-preview1). Update this in the `.csproj` file. The preview version includes the settings control components.

## Step 3: Update `MainWindow.xaml`
1. Include Community Toolkit and WinUI libraries.
2. Update the stack panel alignment.
3. Add a title to the page.

## Step 4: Add basic `SettingsCard`
1. The `SettingsCard` component has the `Description` and `Header` attributes, and the optional `HeaderIcon` attribute.
   - Reference Fluent icon glyph Unicode values [here](https://learn.microsoft.com/en-us/windows/apps/design/style/segoe-fluent-icons-font#pua-e700-e900).
   - The `SettingsCard` looks like a text box, but you can add input elements inside it like toggles, check boxes, and drop downs.
3. Add a simple button inside this settings card.
4. Add a click handler in the `MainWindow` C# file and reference it in the button's `Click` attribute (for now, it won't do anything).

## Step 5: Add a `SettingsExpander` and nest the `SettingsCard` inside it
1. Add a `SettingsExpander.Items` component inside the `SettingsExpander`. This will contain the list of `SettingsCard` elements.

## Step 6: Add more elements to the `SettingsExpander`
1. Add a combo box that displays a drop down of items to select from.
2. Copy and paste the ComboBox setting card from Section 2 of the last example in the sample app.

## Step 7: Add a clickable settings card to the settings expander
1. This will be an empty settings card with the `IsClickEnabled` attribute set to `true`.

## Step 8: Replace the first setting button with a calendar date picker
1. Use the calendar date picker from the WinUI Gallery sample app.
2. Update the font size to 16 to match the other components in the settings expander.
3. Reference the element's `Date` property or add behavior with the `DateChanged` event handler. [Docs here](https://learn.microsoft.com/en-us/windows/windows-app-sdk/api/winrt/microsoft.ui.xaml.controls.calendardatepicker?view=windows-app-sdk-1.6).
