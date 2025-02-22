# Astro Reviews

## Technologies

- Astro 5.3.0
- Node 20.12.2
- Tailwind CSS
- Postgres 16 (Neon)

## Getting Started

1. Install dependencies: `pnpm install`

2. Clonar .env.template y renombrar a .env

3. Crear la BD Postgres y hacer la creacion de la tabla y los inserts.

```sql
CREATE TABLE "Place" (
  "id" serial PRIMARY KEY,
  "title" varchar NOT NULL,
  "description" varchar NOT NULL,
  "avg_rating" decimal NOT NULL,
  "image" varchar NOT NULL
);

INSERT INTO "Place" (title, description, avg_rating, image)
VALUES
('La Librería Escondida', 'Un rincón acogedor escondido en un callejón, lleno de hallazgos raros y cómodos sillones de lectura.', 4.3, 'libreria.webp'),
('Mirador Celestial', 'Un mirador en la cima de una colina que ofrece impresionantes vistas panorámicas de las luces de la ciudad.', 5.0, 'mirador.webp'),
('Sendero del Bosque Encantado', 'Un sendero místico que serpentea entre árboles antiguos, del que se rumorea que está habitado por hadas.', 4.2, 'sendero.webp'),
('El Café Peculiar', 'Una cafetería vibrante decorada con muebles desiguales y obras de arte excéntricas.', 3.1, 'cafe.webp');
```

4. Start in Dev Mode `pnpm run dev`

## Build to Production

```bash
pnpm run build
```

## Prisma

```bash
npx prisma init

npx prisma db pull

npx prisma generate
```
