# Metafields Setup Guide for Bundle Widget

This guide explains how to set up the metafields in your Shopify store to display dietary preferences, allergen information, and product badges in your bundle widget.

## Required Metafields

### 1. Dietary Preferences
- **Namespace**: `shopify`
- **Key**: `dietary-preferences`
- **Type**: `list.metaobject_reference`
- **Metaobject Definition**: `dietary_preference`

#### Metaobject Fields:
- `label` (Single line text) - e.g., "Vegan", "Gluten-Free", "Keto"

### 2. Allergen Information
- **Namespace**: `shopify`
- **Key**: `allergen-information`
- **Type**: `list.metaobject_reference`
- **Metaobject Definition**: `allergen_info`

#### Metaobject Fields:
- `label` (Single line text) - e.g., "Contains Nuts", "Dairy-Free", "Contains Eggs"

### 3. Product Badges
- **Namespace**: `custom`
- **Key**: `badge`
- **Type**: `list.metaobject_reference`
- **Metaobject Definition**: `product_badge`

#### Metaobject Fields:
- `label` (Single line text) - e.g., "NEW", "Best Seller", "Limited"
- `background` (Color) - Background color for the badge
- `text_color` (Color) - Text color for the badge

## Setup Steps in Shopify Admin

### Step 1: Create Metaobject Definitions

1. Go to **Settings > Custom data > Metaobjects**
2. Click **Add definition**

#### For Dietary Preferences:
- **Name**: Dietary Preference
- **Type**: `dietary_preference`
- Add field: `label` (Single line text)

#### For Allergen Information:
- **Name**: Allergen Info
- **Type**: `allergen_info`
- Add field: `label` (Single line text)

#### For Product Badges:
- **Name**: Product Badge
- **Type**: `product_badge`
- Add fields:
  - `label` (Single line text)
  - `background` (Color)
  - `text_color` (Color)

### Step 2: Create Metaobject Entries

Create entries for each metaobject definition:

#### Dietary Preferences Examples:
- Vegan
- Vegetarian
- Gluten-Free
- Keto
- Paleo
- Dairy-Free

#### Allergen Information Examples:
- Contains Nuts
- Contains Dairy
- Contains Eggs
- Contains Soy
- Dairy-Free
- Nut-Free

#### Product Badges Examples:
- NEW (background: #e74c3c, text: #ffffff)
- Best Seller (background: #f39c12, text: #ffffff)
- Limited (background: #9b59b6, text: #ffffff)
- Organic (background: #27ae60, text: #ffffff)

### Step 3: Create Product Metafields

1. Go to **Settings > Custom data > Products**
2. Click **Add definition**

#### Dietary Preferences Metafield:
- **Name**: Dietary Preferences
- **Namespace and key**: shopify.dietary-preferences
- **Type**: List of metaobject references
- **Metaobject**: dietary_preference

#### Allergen Information Metafield:
- **Name**: Allergen Information
- **Namespace and key**: shopify.allergen-information
- **Type**: List of metaobject references
- **Metaobject**: allergen_info

#### Product Badges Metafield:
- **Name**: Badges
- **Namespace and key**: custom.badge
- **Type**: List of metaobject references
- **Metaobject**: product_badge

### Step 4: Assign Metafields to Products

1. Go to your product in the admin
2. Scroll down to the **Metafields** section
3. Assign the appropriate dietary preferences, allergen information, and badges

## How It Displays in the Widget

### Badges
- Appear on the **top left corner** of the product image
- Display **inline** with custom colors
- Include subtle animations on hover

### Pills (Dietary & Allergen)
- Appear **below the product image** and above the title
- Dietary preferences: Green color scheme
- Allergen information: Orange/yellow color scheme
- Automatic color coding based on type

## Example Product Setup

For a "Vegan Chocolate Cookie" product:

**Dietary Preferences**: Vegan, Gluten-Free
**Allergen Information**: Contains Nuts, Dairy-Free
**Badges**: NEW, Best Seller

This would display:
- Badges: "NEW" and "Best Seller" overlaid on the image
- Pills: "Vegan", "Gluten-Free", "Contains Nuts", "Dairy-Free" below the image

## Automatic Styling

The widget automatically applies special styling for common terms:

### Dietary Preferences:
- Vegan: Green
- Vegetarian: Light green
- Gluten-Free: Yellow
- Keto: Purple
- Paleo: Brown
- Dairy-Free: Blue

### Allergens:
- Contains Nuts: Red
- Contains Dairy: Orange
- Contains Eggs: Yellow
- Contains Soy: Light green

### Badges:
- NEW: Red gradient
- Best Seller: Orange gradient
- Limited: Purple gradient
- Organic: Green gradient

## Troubleshooting

### If metafields don't appear:
1. Check that the namespace and key match exactly
2. Ensure metaobject definitions are published
3. Verify that products have the metafields assigned
4. Check browser console for any GraphQL errors

### If styling looks wrong:
1. Inspect the generated HTML classes
2. Ensure CSS is not being overridden by theme styles
3. Check that color values are valid hex codes

This setup will give your customers clear, visual information about your food products' dietary compatibility and special features!
