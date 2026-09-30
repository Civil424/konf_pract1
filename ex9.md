cat > task9 <<'EOF'
#!/bin/sh
sed 's/    /\t/g' "$1" > "$2"
EOF
chmod +x task9

printf 'a    b\n        x\n' > in.txt
./task9 in.txt out.txt
od -c out.txt