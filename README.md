# Entra Sign-in URL Builder

A free online tool to generate Microsoft Entra ID (Azure AD) OAuth 2.0 authorization URLs and admin consent URLs. Simplify the process of creating properly formatted sign-in URLs for various authentication scenarios.

🔗 **Live App:** [https://signin.merill.net](https://signin.merill.net)

## Why I Built This

I created this tool after repeatedly building authentication URLs manually - a tedious process I'd done countless times. This simple web app streamlines URL generation by providing an intuitive form interface where you can quickly fill in parameters and instantly get a properly formatted result.

Beyond just convenience, it serves as an educational resource. Each parameter includes helpful tooltips and direct links to official Microsoft documentation, making it easier for developers and admins to understand OAuth 2.0 flows and build confidence when working with Microsoft Entra ID authentication.

## ✨ Features

### 🎯 URL Types

- **Authorization Code URLs** - Generate secure OAuth 2.0 authorization URLs for web applications
- **Admin Consent URLs** - Create tenant-wide consent URLs for administrative approval

### 🏢 Tenant Support

- **Multi-tenant (`/common`)** - Works with any Entra ID tenant or personal Microsoft accounts
- **Single-tenant (`/organizations`)** - Only organizational accounts
- **Consumer (`/consumers`)** - Only personal Microsoft accounts
- **Specific tenant** - Target a specific tenant by ID or domain name

### 🛡️ Security Features

- **State parameter generation** - CSRF protection with auto-generated random values
- **Nonce parameter generation** - Replay attack protection for OpenID Connect
- **Real-time URL validation** - Ensures generated URLs are properly formatted
- **Copy-to-clipboard** - Secure copying of generated URLs

### 📋 OAuth 2.0 Parameters

- **Client ID** - Your application's identifier
- **Redirect URI** - Where users are sent after authentication
- **Scopes** - Permissions your app requests with Microsoft Graph permission picker
- **Response Type** - Code, token, or hybrid flows
- **Response Mode** - Query, fragment, or form_post
- **Prompt** - Control user interaction (login, consent, select_account, none)
- **Login Hint** - Pre-fill username field
- **Domain Hint** - Direct users to specific identity provider

### 🎨 User Experience

- **Clean, modern interface** - Built with Tailwind CSS and Shadcn-inspired components
- **Responsive design** - Works on desktop, tablet, and mobile
- **Animated URL display** - Eye-catching gradient border for generated URLs
- **Collapsible sections** - Hide/show optional parameters
- **Contextual help** - Tooltips and links to Microsoft documentation
- **Form persistence** - Remembers your inputs while browsing

### 🔍 Microsoft Graph Integration

- **Permission browser** - Search and select from 500+ Microsoft Graph permissions
- **Permission descriptions** - Understand what each permission does
- **Smart filtering** - Find permissions by name or functionality
- **One-click selection** - Easily add permissions to your scope

## 🚀 Use Cases

- **Testing Microsoft Graph API integrations** - Quickly generate auth URLs for API testing
- **Debugging authentication issues** - Troubleshoot Entra ID sign-in problems
- **Creating sign-in links** - Generate URLs for custom applications
- **Admin consent workflows** - Create tenant-wide permission approval URLs
- **Learning OAuth 2.0** - Understand authentication flows and parameters
- **Rapid prototyping** - Speed up authentication workflow development
- **Documentation and tutorials** - Generate example URLs for guides

## 🛠️ Technical Details

### Authentication Flows Supported

- **Authorization Code Flow** - Most secure, recommended for web applications
- **Implicit Flow** - For single-page applications (deprecated but supported)
- **Hybrid Flow** - Combination of code and implicit flows

### Base URL Endpoints

- `https://login.microsoftonline.com/common/oauth2/v2.0/authorize`
- `https://login.microsoftonline.com/organizations/oauth2/v2.0/authorize`
- `https://login.microsoftonline.com/consumers/oauth2/v2.0/authorize`
- `https://login.microsoftonline.com/{tenant}/oauth2/v2.0/authorize`
- `https://login.microsoftonline.com/{tenant}/adminconsent`

### Built With

- **HTML5** - Semantic markup and modern web standards
- **Tailwind CSS** - Utility-first CSS framework
- **Vanilla JavaScript** - No frameworks, pure web APIs
- **Lucide Icons** - Beautiful, consistent iconography
- **Progressive Web App** - Installable with offline capabilities

## 💡 Pro Tips

- ✅ Always use HTTPS redirect URIs in production environments
- ✅ Include appropriate scopes based on your application's requirements  
- ✅ Use the state parameter to prevent CSRF attacks
- ✅ For admin consent, use `.default` scope to request all configured permissions
- ✅ Test with different tenant types to ensure compatibility
- ✅ Include `openid` scope for OpenID Connect flows
- ✅ Add `offline_access` scope if you need refresh tokens

## 📚 Resources

- [Microsoft Identity Platform Documentation](https://learn.microsoft.com/azure/active-directory/develop/)
- [OAuth 2.0 Authorization Code Flow](https://learn.microsoft.com/azure/active-directory/develop/v2-oauth2-auth-code-flow)
- [OpenID Connect on Microsoft Identity Platform](https://learn.microsoft.com/azure/active-directory/develop/v2-protocols-oidc)
- [Microsoft Graph Permissions Reference](https://learn.microsoft.com/graph/permissions-reference)
- [Admin Consent Workflow](https://learn.microsoft.com/azure/active-directory/develop/v2-admin-consent)

## 🤝 Contributing

Found a bug or have a feature request? Please open an issue on GitHub. Contributions are welcome!

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

Made with ❤️ for the Microsoft Entra community
