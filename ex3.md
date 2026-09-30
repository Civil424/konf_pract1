```cat > banner <<'EOF'
#!/bin/sh
line=$(echo "$1" | sed 's/./-/g')
echo "+-$line-+"
echo "| $1 |"
echo "+-$line-+"
EOF
chmod +x banner
./banner "Hello from RTU MIREA!"```