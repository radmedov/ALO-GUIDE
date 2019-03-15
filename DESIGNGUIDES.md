
# Design Guide ALO web
> **IMPORTANT:** It is preferable to provide a Sketch file instead of PSD. Why? Read below:

```
100% Non-Destructive. 
Photoshop has the capability to remain non-destructive, 
but it takes a steady hand not to break things. If you’re a web designer who uses Photoshop, 
you might find yourself conducting the same hide-away performance.
Hiding that extra copy of a layer in its vector or otherwise for safe assurance, 
the same safety net that causes a lot of mess and contributes to file bloat.

Sketch is intended for web-design.
Whether you’re designing a responsive website, an app icon or a batch of material design elements,
Sketch has a variety of pre-loaded templates that are all perfectly sized for your project.
```



## Index
- [Assets requirements](#assets-requirements)
- [The grid](#the-grid)
- [Fonts](#fonts)
- [Sketch/PSD file requirements](#sketchpsd-file-requirements)
    - [Artboards](#artboards)
    - [Initial settings(PSD)](#initial-settingspsd)
    - [Organize files](#organize-files)
    - [Smart objects(PSD)](#smart-objectspsd)
    - [Icons and logos](#icons-and-logos)
    - [Font layers](#font-layers)
  
## Assets requirements

We are using a progressive image rendering on the website. It means that browser is loading the images according to the screen DPR(Device Pixel Ratio) of the user(e.g., If the user has 4K/5K/Retina monitor the browser will load only high-resolution assets and vice versa.). It's very important to upload only the assets with the following sizes:

- **Universal banners:** Desktop - `2340px` width, Mobile - `1200px` width.

- **Homepage images:** Desktop - `2340px` width, Mobile - `1200px` width.

- **Full screen images:** Desktop - `5760px` width, Mobile - `2340px` width. 

- **Collection's full screen image:** `5760px` width.

- **Product image:** `930px` width.

- **File format:** `JPG` only.

> **NOTE:** All other assets must be at least @3x (e.g., if image has width 500px in sketch/psd export as 500 * 3=1500px).

> **IMPORTANT:** A gradient is not allowed on the Universal Banners.

## The grid

The grid is the common language that will help the designer and developer communicate how space, perspective, and aspect ratios work and appear.

We are using a [Bootstrap 4.0](https://getbootstrap.com/docs/4.2/layout/grid/) grid system with gaps.

[DEMO example is here](https://codepen.io/RayDevAlo/full/ebEmyq)

### Max container width

1170px

### Number of columns

12 columns

### Gap size
30px (15px on each side of a column). Gap size is static and never changes. Column size is dynamic and depends on the window size.

### Spacing

It is advisable to use only the following values: 0px, 16px, 24px, 48px, 75px.

### Breakpoints(Alo Yoga)

```
Small: 375px;
Medium: 768px;
Large: 990px;
Widescreen: 1366px;
```
### Breakpoints(AloGives)

```
Small: 576px;
Medium: 768px;
Large: 992px;
Widescreen: 1200px;
```

> **NOTE:** Mobile version <768px, Desktop version ≥768px

> **IMPORTANT:** Please, never start an element in the gap. Only inside of columns!!!

## Fonts

We are using only following fonts on the web-site:

- **Arquitecta**

- **Arquitecta Thin**

- **Arquitecta Black**

- **Arquitecta Bold**

- **Arquitecta Book**

- **Arquitecta Medium**

> **NOTE:** Never use `ITALIC` font style.

## Sketch/PSD file requirements

### Artboards
It's very important to use artboards with a unique name. The file must contain only task related artboards (e.g., `EOY-Sale-Desktop_1440px`, `EOY-Sale-Mobile_320px`). Desktop and mobile version must have its own artboard in the same file.

### Initial settings(PSD)
It's very important to use the following settings and rules:
- `72ppi` only
- No floating pixels(e.g., `23,5px` is incorrect `23px` is correct)
- Do not use points(e.g., `13pt` is incorrect `13px` is correct)
> **IMPORTANT:** The height of text block must be exactly as a line height in text settings!!!

### Organize files
One of the most important parts of the handoff is the ability for the developer to understand the intent of the designer.
Good file management goes a long way here. Organize your folder structure into logical subfolders and layers with descriptive names. (Folder 1, Layer 1 is not helpful. Label according to what is contained therein, such as CTA Button.) 
Consider the HTML structure when grouping files; this helps make the handoff more logical. `NAME EVERY SINGLE LAYER.`
Color code or add prefixes to layer names and folders to insinuate interactivity, such as hover states. This visual cue is really helpful for developers because with hundreds or more layers to sift through it can be easy to miss something (particularly hidden layers). Have a conversation with the developer so that he or she understands your color- or text-coding meanings. `DELETE UNUSED LAYERS.`

### Smart objects(PSD)
Keep all image and vector layers as a Smart Object. it’s important to use nondestructive techniques, such as layer styles. ([Nondestructive file practices](https://helpx.adobe.com/photoshop/using/nondestructive-editing.html) allow you to make changes without altering the original information or layer.)

### Icons and logos
All icons and logos must be implemented as a `VECTOR ASSET` only. Never use `RASTERIZED LAYERS` e.g. `JPG`, `PNG`, `SCREENSHOT` files. 

### Font layers
All font layers must be implemented as a `TEXT` only. Never use pictures with a text. Every paragraph, title, subtitle etc must have its own layer.

> **IMPORTANT:** Please, never use `SCREENSHOTS`, `RASTERIZED LAYERS` in the design files. Only high-quality assets.
> **IMPORTANT:** Double check that you use design elements that are within the design style of that particular page/website.(e.g., style of buttons, icons, headings, paragraphs etc must be the same as already exist on that page.)
