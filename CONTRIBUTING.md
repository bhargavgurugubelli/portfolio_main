# Contributing to 3D Developer Portfolio Website

First off, thank you for considering contributing to this portfolio template! 🎉 Community contributions are what make open source such an amazing place to learn, inspire, and create.

Please take a moment to review this document in order to make the contribution process easy and effective for everyone involved.

---

## 🛠️ Local Development Setup

To get the codebase running locally on your machine, follow these steps:

1. **Fork the Repository**
   Click the "Fork" button at the top right of this repository page to create a copy of the repo under your GitHub account.

2. **Clone Your Fork**
   ```bash
   git clone https://github.com/YOUR_USERNAME/portfolio_main.git
   cd portfolio_main
   ```

3. **Install Dependencies**
   Make sure you have [Node.js](https://nodejs.org/) installed (v18+ recommended).
   ```bash
   npm install
   ```

4. **Run the Development Server**
   Start the Vite development server locally:
   ```bash
   npm run dev
   ```
   Open your browser and navigate to `http://localhost:5173` (or the port specified in your console).

5. **Make Your Changes**
   Create a new branch for your feature or bug fix:
   ```bash
   git checkout -b feature/your-awesome-feature
   # or
   git checkout -b fix/bug-description
   ```

6. **Verify Code Quality**
   Ensure there are no build or compilation errors:
   ```bash
   npm run build
   ```

---

## 🎨 Guidelines & Best Practices

### Code Style
- **TypeScript**: We use TypeScript for type safety. Ensure variables, function parameters, and component props are typed correctly. Avoid using `any` unless absolutely necessary.
- **Components**: Group UI components in `src/components/` and pages in `src/pages/`. Keep them modular and focused.
- **Styling**: We use vanilla CSS and modular styles. Keep styles clean, responsive, and check compatibility across multiple viewport sizes.

### 📐 Three.js & WebGL Guidelines
Since this is a WebGL-intensive 3D website, performance is key:
- **Resource Disposal**: Always dispose of geometries, materials, and textures when Three.js components unmount to avoid WebGL memory leaks.
- **Frame Rate Optimization**: Limit heavy calculations inside the `requestAnimationFrame` or `useFrame` loop. Avoid instantiating new vectors or colors inside render loops.
- **Asset Size**: Keep 3D assets (`.gltf`, `.glb`, textures) as small as possible. Use compression tools like GLTF-Pipeline or DRACO compression if importing external models.

### ⚙️ Customization Rules
- **No Hardcoded Personal Info**: Do **NOT** hardcode your own or others' personal details directly inside components. All developer details, project lists, and content must be read dynamically from `src/config.ts`.
- If you introduce a new feature that contains text or links, add corresponding configuration settings to `src/config.ts`.

---

## 🚀 Submitting a Pull Request

1. **Commit your changes**: Write clear, descriptive commit messages.
   ```bash
   git commit -m "feat: add interactive 3D particle effect to contact page"
   ```
2. **Push to GitHub**:
   ```bash
   git push origin feature/your-awesome-feature
   ```
3. **Open a Pull Request**: Navigate to the original repository and click **Compare & pull request**. Complete the PR template details.
4. **Be Responsive**: Once submitted, maintainers or other community members may review your code and offer suggestions.

---

## 💬 Community & Discussions
If you have questions, suggestions, or want to showcase how you customized this portfolio, feel free to open a thread in the **GitHub Discussions** tab of this repository!
