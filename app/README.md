# Stockroom

A responsive product inventory CRUD app built with Next.js App Router, React-Bootstrap, Redux Toolkit, Axios, Formik, Yup, and json-server.

## Run locally

Requirements: Node.js 20.9 or newer.

```bash
npm install
```

Start the json-server API in one terminal:

```bash
npm run server
```

Start Next.js in another terminal:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000). The API runs at [http://localhost:4000/products](http://localhost:4000/products).

The seeded sample catalog is in `db.json`; json-server writes CRUD changes back to that file. Restore the original sample data by reverting `db.json` to its checked-in version.

## Features

- Browse, search, and filter products by category.
- View product details and inventory value.
- Create and edit products with Formik/Yup validation.
- Delete products with a confirmation prompt.
- Redux Toolkit async actions and Axios API requests with visible loading and error states.
- Responsive Bootstrap dashboard with accessible form labels and feedback.

## Product data

Each record in `db.json` uses this shape:

```json
{
  "id": "p-1001",
  "name": "Everyday Canvas Tote",
  "sku": "ACC-001",
  "category": "Accessories",
  "price": 28,
  "stock": 42,
  "description": "A short product description."
}
```

## Configuration

Copy `.env.example` to `.env.local` to change `NEXT_PUBLIC_API_URL`. The default is `http://localhost:4000`. Restart the Next.js dev server after changing environment variables.

## Quality checks

```bash
npm run lint
npm run build
```

`npm run server` and `npm run dev` run independently; start both for CRUD operations.
