# Copilot Instructions

## Project Overview
This is Jacques Pillet's graphics programming portfolio website, built with Jekyll and hosted on GitHub Pages. It showcases graphics engines, 3D experiments, path tracers, and interactive WebGL demos spanning C++/Vulkan projects to Three.js browser experiments.

## Architecture & Structure

### Site Architecture
- **Jekyll static site** using `remote_theme: pages-themes/tactile@v0.2.0`
- **Root markdown files** (e.g., `gfx.md`, `Vulkan.md`, `GPUPT.md`) serve as project landing pages
- **Main README.md** acts as homepage with image-linked navigation to projects
- **Threejs/** directory contains self-contained interactive HTML experiments
- **Images/** directory organized by project with screenshots and assets

### Content Patterns
- **Project pages** follow consistent structure: title, repo link, feature overview, screenshots, dependencies/resources
- **Code examples** embedded in markdown using triple backticks with language specification
- **Image references** use GitHub raw URLs for external repos, relative paths for local assets
- **Navigation** via image links in README.md using `[![Alt](path)](destination)` pattern

### Three.js Experiments Structure
- **Self-contained HTML files** in `Threejs/ProjectName/index.html`
- **Shared assets** in `Threejs/js/` (three.js, dat.gui.min.js, OBJLoader.js, perlin.js)
- **Controls pattern**: dat.GUI folder with parameters, onChange handlers for real-time updates
- **Asset loading**: Cubemaps in `assets/cubemaps/`, models use relative paths to `../assets/`

## Development Workflows

### Adding New Projects
1. Create markdown file in root (e.g., `NewProject.md`)
2. Add image link to `README.md` in appropriate section (Recent/Older Stuff)
3. Add screenshot to `Images/Home/` directory
4. Follow project page template: description, repo link, features, gallery, dependencies

### Three.js Experiments
- Use `../js/three.js` and `../js/dat.gui.min.js` for consistency
- Follow naming: primary file as `Index.html` or `index.html`
- Implement dat.GUI controls in top-right corner
- Use shared asset structure: `../assets/` for textures, models

### Image Management
- **External projects**: Use GitHub raw URLs (`https://github.com/user/repo/blob/branch/path?raw=true`)
- **Local images**: Use relative paths (`Images/ProjectName/file.png`)
- **Consistent naming**: Use descriptive filenames, organize by project

## Key Conventions

### File Naming
- **Project pages**: CamelCase matching directory names (`Threejs.md`, `PathTracing.md`)
- **Three.js experiments**: Folders in PascalCase, main file as `Index.html` or `index.html`
- **Images**: Descriptive names, grouped by project in subdirectories

### Markdown Style
- **Headers**: Use `# ProjectName` for title, `## Section` for major sections
- **Links**: External repos as `[Link to the repo](url)`, inline code as backticks
- **Code blocks**: Always specify language (```cpp, ```html, ```javascript)
- **Images**: Use relative paths for local assets, alt text for accessibility

### Three.js Patterns
- **Scene setup**: Standard camera, renderer, scene initialization
- **Controls**: dat.GUI with folders, parameter objects with onChange handlers
- **Animation loop**: requestAnimationFrame pattern with render calls
- **Asset loading**: CubeTextureLoader for environments, shared geometry patterns

## External Dependencies
- **Jekyll/GitHub Pages**: Automatic deployment, no build process required
- **External repos**: Multiple GitHub repositories referenced (gfx, vulkan, gpupt_blog, etc.)
- **Three.js version**: Using local copy in `Threejs/js/three.js` (older version for compatibility)
- **Libraries**: dat.GUI for controls, OBJLoader for models, custom perlin.js for noise

## Resources & References
- Graphics programming focus: Vulkan, OpenGL, compute shaders, ray tracing
- Mathematical implementations: Perlin noise, fluid simulation, PBD physics
- External inspiration: LearnOpenGL, Catlike Coding, pbrt, Vulkan samples
- Asset sources: glTF Sample Models, Sketchfab, McGuire Graphics Archive