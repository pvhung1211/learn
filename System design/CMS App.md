https://www.youtube.com/watch?v=6omuUOZcWL0

```ts

// types/content.types.js

/**
 * Base Content Model
 */
export const ContentModel = {
  id: '',
  type: 'page|post|article|custom',
  title: '',
  slug: '',
  status: 'draft|published|archived',
  author: {
    id: '',
    name: '',
    email: ''
  },
  content: {
    blocks: [] // Content blocks
  },
  metadata: {
    seo: {
      title: '',
      description: '',
      keywords: [],
      ogImage: ''
    },
    featured: false,
    categories: [],
    tags: []
  },
  media: {
    featured_image: null,
    gallery: []
  },
  settings: {
    template: 'default',
    visibility: 'public|private|password',
    publishDate: null,
    expiryDate: null
  },
  timestamps: {
    createdAt: '',
    updatedAt: '',
    publishedAt: ''
  },
  version: 1,
  revisions: []
};

/**
 * Content Block Model (for page builder)
 */
export const ContentBlock = {
  id: '',
  type: 'text|image|video|gallery|embed|custom',
  order: 0,
  content: {},
  settings: {
    cssClass: '',
    customStyles: {},
    responsive: {
      mobile: {},
      tablet: {},
      desktop: {}
    }
  }
};

/**
 * Media Model
 */
export const MediaModel = {
  id: '',
  filename: '',
  url: '',
  type: 'image|video|document|audio',
  mimeType: '',
  size: 0,
  dimensions: {
    width: 0,
    height: 0
  },
  alt: '',
  title: '',
  description: '',
  metadata: {
    exif: {},
    colors: []
  },
  thumbnails: {
    small: '',
    medium: '',
    large: ''
  },
  uploadedBy: '',
  createdAt: '',
  updatedAt: ''
};

```