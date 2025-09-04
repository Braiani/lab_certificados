# Lab Certificados

This repository provides minimal configuration files and scripts for quickly setting up a Certificate Authority (CA) in a lab environment. It's intended as a reference or "gist" to copy and paste from when configuring your own CA.

## Contents

- `server.csr.conf` - Example OpenSSL CSR (Certificate Signing Request) configuration file.
- `server.ext` - Example OpenSSL certificate extensions file.
- `default-ssl.conf` - Nginx SSL base configuration.
- `README` - This documentation file.

## Requirements

- OpenSSL
- Bash
- nginx

## Usage

1. Clone this repository:
    ```bash
    git clone https://github.com/braiani/lab_certificados.git
    cd lab_certificados
    ```

2. Generate a private key and CSR:
    ```bash
    openssl req -new -config server.csr.conf -keyout server.key -out server.csr
    ```

3. Sign the CSR with your CA:
    ```bash
    openssl x509 -req -in server.csr -CA ca.crt -CAkey ca.key -CAcreateserial -out server.crt -days 365 -extfile server.ext
    ```

4. Configure nginx with `default-ssl.conf` and your generated certificates.

## Notes

- This setup is for educational and lab purposes only. Do not use in production.
- Protect your CA private key and configuration files.
- Adjust file paths and configuration options as needed for your environment.

## References

- [OpenSSL Documentation](https://www.openssl.org/docs/)
- [How to set up your own CA with OpenSSL](https://jamielinux.com/docs/openssl-certificate-authority/)
- [Nginx Documentation](https://nginx.org/en/docs/)

## License

This project is licensed under the MIT License.
