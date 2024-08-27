# Build stage
FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build-env
WORKDIR /app

# Copy everything and build
COPY . ./
RUN dotnet publish -c Release -o /app/output

# Runtime stage
FROM nginx:latest
WORKDIR /var/www/web

# Copy build artifacts
COPY --from=build-env /app/output/wwwroot .

# Copy custom nginx configuration
COPY nginx.conf /etc/nginx/nginx.conf

# Expose the required port
EXPOSE 80

# Start Nginx
CMD ["nginx", "-g", "daemon off;"]
