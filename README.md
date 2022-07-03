# install 

apt-get install trivy

# vulnerability

trivy rootfs --severity HIGH,CRITICAL --timeout 15m /
trivy fs --severity HIGH,CRITICAL --timeout 15m path

#### if too long:
trivy rootfs --severity HIGH,CRITICAL --timeout 15m --security-checks vuln /
trivy fs --severity HIGH,CRITICAL --timeout 15m --security-checks vuln path


# Iac misconfiguration 

trivy config path
trivy image --security-checks config IMAGE_NAME #docker image
trivy fs --security-checks config /path/to/dir #path
trivy fs --severity HIGH,CRITICAL . 

# repo 

trivy repo https://github.com/knqyf263/trivy-ci-test