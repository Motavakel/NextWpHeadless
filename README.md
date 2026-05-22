# Headless WordPress Next.js


<p align="center">
  <img src="screenshots/Landing.jpg" width="380" alt="home"/>
<!--   <img src="screenshots/blog.jpg" width="380" alt="blog"/> -->
</p>


<p align="justify">
A high-performance, SEO-optimized e-commerce and content platform built with Next.js 15 (App Router) and a headless WordPress backend. This project leverages the power of WPGraphQL, the WooCommerce REST API, and modern React tooling to deliver a fast, flexible, and scalable frontend experience.

## Can WordPress Be Used as the Backend for Next.js?

<p align="justify">
Absolutely. This project is a production-ready demonstration of using WordPress as a headless CMS. WordPress exposes its data via:

- **WPGraphQL** for posts, pages, categories, tags, and custom post types.
- **WooCommerce REST API** for product catalogs, categories, tags, and e-commerce data.

<p align="justify">
Next.js consumes these endpoints and renders a fully static or server-side rendered frontend, decoupling content management from presentation. The result is a website that combines WordPress's familiar admin interface with Next.js's performance and developer experience.

## Key Features

- **Next.js 15 App Router** with parallel routes, route groups, and dynamic routing.
- **Headless WordPress** integration via WPGraphQL for blog and page content.
- **Headless WooCommerce** integration via the official WooCommerce REST API for product data.
- **Apollo Client** for efficient GraphQL data fetching, caching, and state management.
- **TanStack React Query** for REST API calls (WooCommerce) with automatic background refetching and caching.
- **TypeScript** throughout for type safety and improved developer experience.
- **Tailwind CSS v4** with RTL support and custom utility classes.
- **Swiper** for touch-friendly sliders and carousels.
- **Modular component architecture** with clear separation of concerns (e.g., `plp` components, `ui` primitives).
- **Dynamic imports** and code splitting for optimal performance.

## Project Structure
The project follows a scalable folder structure designed for maintainability and separation of concerns.

```text
MAXPHONE/
├── .next/
├── node_modules/
├── public/
├── src/
│   ├── assets/
│   ├── app/
|   |   ├── api/
|   │   |   └── revalidate/
|   │   |       └── route.ts 
│   │   ├── (home)/
│   │   │   ├── components/
│   │   │   │   ├── Banner
│   │   │   │   │   ├── banner.client.tsx
|   |   |   |   |   └── banner.server.tsx
│   │   │   │   │  
│   │   │   │   ├── BannerSlider
│   │   │   │   │   ├── BannerSlider.client.tsx
|   |   |   |   |   └── BannerSlider.server.tsx
│   │   │   │   │  
│   │   │   │   ├── BrandSlider
│   │   │   │   │   ├── BrandSlider.client.tsx
|   |   |   |   |   └── BrandSlider.server.tsx
│   │   │   │   │  
│   │   │   │   ├── CategoryGrid
│   │   │   │   │   ├── CategoryGrid.client.tsx
|   |   |   |   |   └── CategoryGrid.server.tsx
│   │   │   │   │  
│   │   │   │   ├── HeroSlider
│   │   │   │   │   ├── HeroSlider.client.tsx
|   |   |   |   |   └── HeroSlider.server.tsx
│   │   │   │   │  
│   │   │   │   ├── SecondBrandSlider
│   │   │   │   │   ├── SecondBrandSlider.client.tsx
|   |   |   |   |   └── SecondBrandSlider.server.tsx
│   │   │   │   │  
│   │   │   │   └── skeletons
│   │   │   │      ├── BannerSkeleton.tsx
│   │   │   │      ├── BlogCardSkeleton.tsx
│   │   │   │      ├── CategoryGridSkeleton.tsx
|   |   |   |      └── BannerSliderSkeleton.tsx  
│   │   │   │   
│   │   │   └── page.tsx
.   .   .
.   .   .
│   │   ├── global.css
│   │   ├── favicon.ico
│   │   └── layout.tsx
│   │
│   ├── components/
│   │   ├── ui/
│   │
│   ├── hooks/
│   │    ├── useProductQuery.ts   
│   │    ├──  ....     
│   │    └── useCategoryQuery.ts 
│   │     
│   ├── providers/
│   │    └── QueryProvider.tsx    
│   │
│   ├── middleware.ts
│   │       
│   └── lib/
│       └── api/
│           ├── core/
│           │   ├── apolloClient.ts
│           │   └── wooCommerceClient.ts
│           │
│           └── graphql/
│
└── README.md

