cat > task4 <<'EOF'
#!/bin/sh
grep -oE '[A-Za-z_][A-Za-z0-9_]*' "$1" | sort -u | tr '\n' ' '
echo
EOF
chmod +x task4
./task4 hello.c