# Entra Sign-in URL Builder

A free online tool to generate Microsoft Entra ID (Azure AD) OAuth 2.0 authorization URLs and admin consent URLs. Simplify the process of creating properly formatted sign-in URLs for various authentication scenarios.

🔗 **Live App:** [https://signin.merill.net](https://signin.merill.net)

## Why I Built This

I created this tool after repeatedly building authentication URLs manually, encoding parameters, looking up docs - a tedious process I'd done countless times. This simple tool streamlines URL generation by providing an intuitive form interface where you can quickly fill in parameters and instantly get a properly formatted result.

Beyond just convenience, I've made this to serves as an educational resource. Each parameter includes helpful tooltips and direct links to official Microsoft documentation and OAuth specs, making it easier for developers and admins to understand OAuth 2.0 flows and test things out when working with Microsoft Entra ID authentication.

## 💡 Pro Tips

- ✅ Always use HTTPS redirect URIs in production environments
- ✅ Handle the generated tokens with extreme care

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
