# Custom Food Bundle Widget

A complete, production-ready bundle widget for Shopify stores using Recharge dynamic bundles. This widget is specifically designed for food stores and provides a modern, intuitive interface for customers to build custom food bundles.

## Features

### ✨ Modern UI Design
- Clean, professional design inspired by modern e-commerce sites
- Responsive layout that works on desktop, tablet, and mobile
- Smooth animations and hover effects
- Gradient backgrounds and modern styling

### 🍽️ Food-Focused Experience
- Collection-based navigation for easy product discovery
- Variant selection with clear bundle size options
- Real-time bundle validation and feedback
- Visual quantity controls for each product

### 🔧 Technical Features
- **Recharge SDK Integration**: Uses official Recharge SDK for bundle management
- **Shopify Storefront API**: Fetches product data with full pagination support
- **Dual Cart Support**: Works with both Shopify online stores and headless implementations
- **Real-time Validation**: Validates bundle constraints as customers make selections
- **Error Handling**: Comprehensive error handling with user-friendly messages

### 📱 Responsive & Accessible
- Mobile-first responsive design
- Keyboard navigation support
- Screen reader friendly with proper ARIA labels
- Touch-friendly controls for mobile devices

## Configuration

The widget is configured for your store with the following settings:

```javascript
const CONFIG = {
    storeIdentifier: 'rc-bundles.myshopify.com',
    storeDomain: 'https://rc-bundles.myshopify.com',
    storefrontAccessToken: 'ef69584f646c3ea0cfbe978d067d113d',
    bundleProductId: '8138138353916',
    appName: 'Custom Food Bundle Widget',
    appVersion: '1.0.0'
};
```

## How It Works

1. **Bundle Loading**: The widget loads bundle configuration from Recharge using the CDN API
2. **Variant Selection**: Customers choose their preferred bundle size
3. **Collection Navigation**: Customers can browse different food categories/collections
4. **Product Selection**: Add/remove items with quantity controls
5. **Real-time Validation**: Bundle rules are enforced in real-time
6. **Cart Integration**: Uses Recharge SDK to properly format bundle items for cart

## Bundle Rules

The widget automatically extracts and enforces bundle rules from your Recharge configuration:

- **Bundle Size Constraints**: Min/max total items in the bundle
- **Collection Constraints**: Per-collection min/max item requirements
- **Real-time Feedback**: Immediate validation with clear error messages

## Installation

1. **Upload the HTML file** to your server or Shopify theme
2. **Update configuration** if needed (store domain, access tokens, bundle ID)
3. **Test the widget** with your actual bundle configuration
4. **Customize styling** to match your brand if desired

## Customization

### Styling
The CSS is organized into sections for easy customization:
- Color schemes can be updated in the CSS variables
- Layout can be modified by adjusting grid templates
- Product card styling can be customized for your brand

### Content
- Update the header text to match your brand voice
- Modify collection tab labels and descriptions
- Customize validation messages and error text

### Functionality
- Add metafield support for dietary preferences/allergens
- Implement advanced filtering options
- Add product modal views for detailed information

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Android Chrome)

## Dependencies

- **Recharge SDK**: Loaded from CDN (`recharge-client-1.46.0.min.js`)
- **Shopify Storefront API Client**: Loaded from CDN (`storefront-api-client.min.js`)

## Performance

- **Pagination Support**: Handles large collections (1000+ products) efficiently
- **Caching**: Product data is cached to reduce API calls
- **Lazy Loading**: Products are loaded only when collections are selected
- **Optimized Requests**: Uses maximum allowed items per GraphQL request (250)

## Production Checklist

✅ **Technical Implementation**
- Recharge SDK properly initialized
- Bundle settings loaded from Recharge API
- Product pagination implemented for large collections
- Cart integration using official Recharge methods

✅ **User Experience**
- Real-time bundle validation
- Loading states and error handling
- Responsive design for all devices
- Clear visual feedback for user actions

✅ **Code Quality**
- Clean separation of concerns
- Proper error boundaries
- Accessible HTML structure
- Modern JavaScript practices

## Testing

Test the following scenarios:
1. **Bundle Rules**: Try various combinations to ensure validation works
2. **Large Collections**: Test with collections containing 250+ products
3. **Mobile Experience**: Test on actual mobile devices
4. **Cart Integration**: Complete purchases to ensure bundle items are properly formatted
5. **Error Scenarios**: Test with network failures and invalid configurations

## Support

For issues with:
- **Bundle Configuration**: Check your Recharge dashboard settings
- **Product Loading**: Verify Shopify Storefront API access token permissions
- **Cart Issues**: Ensure Recharge SDK is properly initialized

## License

This widget is provided as-is for your Shopify store. Customize and modify as needed for your specific requirements.
