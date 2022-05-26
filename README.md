# Containers

Purpose: migrate Docker containers to Podman rootless containers

Allow binding on ports 80 and greater to unprivileged users

    sudo sysctl net.ipv4.ip_unprivileged_port_start=80

Configurer podman.socket as user service

    systemctl --user enable podman.socket
    systemctl --user start podman.socket
    systemctl --user status podman.socket