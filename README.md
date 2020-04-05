# VL.WinFormsUtils
Nodes for VL exposing some useful functions of the Windows Forms API and to retain SkiaRenderer window state between application restarts.

With this you can quickly add an extra layer of polish to your exported apps.

## Using the library
In order to use this library with vl you have to install the nuget that is available via nuget.org. For information on how to use nugets with vl, see [Managing Nugets](https://vvvv.gitbooks.io/the-gray-book/content/en/reference/libraries/dependencies.html#_manage_nugets) in the vl documentation. As described there you go to the commandline and then type:

    nuget install VL.WinFormsUtils

Once the VL.WinFormsUtils nuget is installed and referenced in your vl document you'll see the category "WinFormsUtils" in the nodebrowser. From there explore the nodes.

A HowTo patch "Use the library" is included and can be found in the Help Browser (F1).

## Nodes
- SkiaRenderer window state retention (position, size, fullscreen state):
  - StoreBounds (preferred, combines the other two)
  - BoundsReader
  - BoundsWriter
- SetTitle - sets the window title
- SetAlwaysOnTop - sets the on top property
- SetBorderStyle - sets look and behavior of the window
- Buttons:
  - SetMinimizeBox
  - SetMaximizeBox
  - SetControlBox
- Icons:
  - SetIcon - sets the window's icon, use any standard image file
  - SetShowIcon - show or hide the icon in the window's title bar
- Cursors:
  - SetCursor - change the current mouse cursor
  - Cursors - a category exposing all the standard System.Windows.Forms.Cursors
- Close Handling:
  - SetCloseHandler - use with DialogCloseHandler, PreventCloseHandler or make your own
  - DialogCloseHandler - Handles closing with a standard Windows.Forms.MessageBox
  - PreventCloseHandler - Always prevents closing of the window
  - PreventClose - SetCloseHandler + PreventCloseHandler
  - Close - close the window programmaticaly, works just like pressing the close button
