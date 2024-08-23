# Use the official OWASP ZAP base image
FROM owasp/zap2docker-stable:latest

# Set environment variables if needed (e.g., for configuration)
ENV ZAP_USER=user
ENV ZAP_PASSWORD=password

# Optionally copy custom scripts or configuration files
# COPY ./custom-config.xml /zap/wrk/

# Expose a custom port (e.g., 9090)
EXPOSE 9090

# Set default command (you can override this in docker-compose or when running the container)
ENTRYPOINT ["zap.sh"]
# Default arguments to run ZAP in daemon mode and use the custom port
CMD ["-daemon", "-host", "0.0.0.0", "-port", "9090"]

