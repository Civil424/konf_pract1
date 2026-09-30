cat > reg <<'EOF'
#!/bin/sh
chmod 755 "$1"
cp "$1" /usr/local/bin/
EOF
chmod +x reg
./reg banner
banner "Works!"