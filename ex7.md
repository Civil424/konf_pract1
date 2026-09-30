```cat > task7 <<'EOF'
#!/bin/sh
for a in $(find "$1" -type f); do
  for b in $(find "$1" -type f); do
    if [ "$a" \< "$b" ] && cmp -s "$a" "$b"; then
      echo "$a и $b одинаковые"
    fi
  done
done
EOF
chmod +x task7
./task7 e```