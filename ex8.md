cat > task8 <<'EOF'
#!/bin/sh
tar -cvf archive.tar "$2"/*."$1"
EOF
chmod +x task8

./task8 c d