# Nginx Starter Pack

A production-ready Nginx configuration template for hosting multiple React applications with Express.js backends.

## 🚀 Features

- **2 React Apps** with static file serving
- **2 Express APIs** with reverse proxy configuration
- **SSL/TLS** encryption setup
- **HTTP to HTTPS** automatic redirect
- **Gzip compression** for optimal performance
- **WebSocket support** for real-time features
- **Client-side routing** support for React Router

## 📋 Architecture

This configuration demonstrates Nginx acting as:
- **Web Server**: Serves static React build files
- **Reverse Proxy**: Forwards API requests to Express backends
- **SSL Termination**: Handles HTTPS encryption/decryption

## 🔧 Configuration Overview

### React Applications
1. **Landing Page** (`server1.com`) - Serves from `/var/www/landing/dist`
2. **Admin Dashboard** (`dashboard.example.com`) - Serves from `/var/www/dashboard/dist`

### Express APIs
1. **API Server** (`api.example.com`) - Port 3000
2. **Web API** (`webapi.example.com`) - Port 8000

Both React apps proxy `/api/*` requests to the Express backend on port 8000.

## 📝 Usage

1. Replace example domains with your actual domains
2. Update SSL certificate paths
3. Adjust application root directories
4. Copy to `/etc/nginx/nginx.conf` or include in your main config
5. Test configuration: `sudo nginx -t`
6. Reload Nginx: `sudo systemctl reload nginx`

## 🔒 Security Features

- TLS 1.2 and 1.3 only
- Strong cipher suites
- Proper proxy headers for client IP forwarding
- Request body size limits
- Buffer overflow protection

## 📚 Learn More

This configuration includes detailed inline comments explaining each directive and its purpose.

## 📄 License

MIT License - Feel free to use and modify for your projects.
