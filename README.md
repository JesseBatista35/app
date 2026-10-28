echo "=== Firefox no agente? ==="
command -v firefox && firefox --version 2>/dev/null

echo "=== Instalando Chromium via EPEL ==="
dnf install -y --setopt=install_weak_deps=False chromium 2>&1 | tail -15

CHROME=$(command -v chromium-browser || command -v chromium || true)
if [ -n "$CHROME" ]; then
  echo "Chrome encontrado: $CHROME"
  $CHROME --version
  echo "##vso[task.setvariable variable=CHROME_BIN]$CHROME"
else
  echo "##[warning]Chromium não instalado"
fi
exit 0
