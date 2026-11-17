# Live Website Viewer for PowerPoint

Self-hosted copy of the PowerPoint content add-in from [peopleworks/powerpointwebviewer](https://github.com/peopleworks/powerpointwebviewer), served from `https://crykn.github.io/powerpoint-webviewer/`.

## Setup

The add-in is needed both to **embed** web pages and to **view** presentations that contain embedded pages.

### PowerPoint for the Web

1. Download [`manifest.xml`](https://github.com/crykn/powerpoint-webviewer/releases/latest/download/manifest.xml)
2. Open a presentation, then **Insert → Add-ins → Upload My Add-in** → choose `manifest.xml`.

### PowerPoint for Windows

1. Download [`manifest.xml`](https://github.com/crykn/powerpoint-webviewer/releases/latest/download/manifest.xml)
2. Put `manifest.xml` in a folder, share it with your user (or everyone) via **Properties → Sharing**, and note
   the network path, e.g. `\\YOUR-PC\AddinManifests` (a local path like `C:\…` does not work).
3. Register the folder as a source of add-ins: **File → Options → Trust Center → Trust Center Settings → Trusted Add-in Catalogs**: add the path as *Catalog URL*, tick **Show in Menu**, confirm with **OK**.
4. Restart PowerPoint, open a presentation, then **Home → Add-ins → SHARED FOLDER → Live Website Viewer → Add**.

> [!NOTE]
> If the catalog settings are greyed out, they are locked by your organisation's IT.

### PowerPoint for Mac

1. Download [`manifest.xml`](https://github.com/crykn/powerpoint-webviewer/releases/latest/download/manifest.xml)
2. Copy `manifest.xml` to `~/Library/Containers/com.microsoft.Powerpoint/Data/Documents/wef/`
   (create `wef` if it is missing).
3. Restart PowerPoint, open a presentation, then **Home → Add-ins → Live Website Viewer**.

## Usage

### Create a slide

Insert the add-in on a slide, type a URL and press **Enter**. The box can be resized via its border.

> [!TIP]
> YouTube/Vimeo videos are supported, just paste the normal link. Alternatively use **Insert → Video → Online Video**, which works without the add-in.

> [!WARNING]
> Don't use URLs containing passwords or tokens: anyone with the `.pptx` can read them.

### While presenting

- Pages are loaded live, not stored in the `.pptx`; thus, an internet connection is required
- **✕** hides the controls; the small **⚙** in the corner brings them back. **↻** reloads the page.
- If a blank page or "refused to connect" is shown: the site likely forbids embedding. Use **Window** to open it in a separate window.

> [!WARNING]
> Slides load their saved websites automatically when opened. Only open presentations from people you trust.
