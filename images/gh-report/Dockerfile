FROM alpine:3.20

ARG GH_VERSION=2.62.0

RUN apk add --no-cache \
        bash \
        coreutils \
        curl \
        git \
        jq \
        tzdata \
        ca-certificates \
    && ARCH="$(apk --print-arch)" \
    && case "${ARCH}" in \
         x86_64)  GH_ARCH=amd64 ;; \
         aarch64) GH_ARCH=arm64 ;; \
         *) echo "unsupported arch: ${ARCH}" >&2; exit 1 ;; \
       esac \
    && curl -fsSL \
         "https://github.com/cli/cli/releases/download/v${GH_VERSION}/gh_${GH_VERSION}_linux_${GH_ARCH}.tar.gz" \
         -o /tmp/gh.tar.gz \
    && tar -xzf /tmp/gh.tar.gz -C /tmp \
    && mv "/tmp/gh_${GH_VERSION}_linux_${GH_ARCH}/bin/gh" /usr/local/bin/gh \
    && chmod +x /usr/local/bin/gh \
    && rm -rf /tmp/gh.tar.gz "/tmp/gh_${GH_VERSION}_linux_${GH_ARCH}" \
    && gh --version \
    && jq --version
