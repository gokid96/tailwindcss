# Install Tailwind CLI

# 1. Install tailwindcss via npm, and create your tailwind.config.js file.

# Terminal

npm install -D tailwindcss@3
npx tailwindcss init

# 2. Configure your template paths

# Add the paths to all of your template files in your tailwind.config.js file.

# tailwind.config.js

/\*_ @type {import('tailwindcss').Config} _/
export default {

> content: ["./src/**/*.{html,js}"],

    theme: {
      extend: {},
    },
    plugins: [],

}

# 3. Add the Tailwind directives to your CSS

# Add the @tailwind directives for each of Tailwind’s layers to your main CSS file.

# src/input.css

@tailwind base;
@tailwind components;
@tailwind utilities;

# 4. Start the Tailwind CLI build process

# Run the CLI tool to scan your template files # for classes and build your CSS.

# Terminal start

npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
