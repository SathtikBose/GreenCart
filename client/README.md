# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.

# GreenCart Fullstack Setup

## Development

### Server (Backend)

1. Install dependencies:
   ```
   cd ../server
   npm install
   ```
2. Start server:
   ```
   npm run dev
   ```

### Client (Frontend)

1. Install dependencies:
   ```
   npm install
   ```
2. Start client:
   ```
   npm run dev
   ```

Open [http://localhost:5173](http://localhost:5173) for frontend and [http://localhost:4000](http://localhost:4000) for backend API.

## Environment Variables

- Set backend `.env` as per sample.
- Set frontend `.env` for `VITE_BACKEND_URL` and `VITE_CURRENCY`.

## Notes

- Make sure MongoDB, Cloudinary, and Stripe credentials are correct.
- Stripe webhook endpoint should be set in Stripe dashboard to `/stripe` on your backend.
