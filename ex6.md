cat > task6 <<'EOF'
#!/bin/sh
for f in *.c *.js; do
  if head -n 1 "$f" | grep -q -e '^//' -e '^/\*'; then
    echo "$f: есть комментарий"
  else
    echo "$f: нет комментария"
  fi
done

for f in *.py; do
  if head -n 1 "$f" | grep -q '^#'; then
    echo "$f: есть комментарий"
  else
    echo "$f: нет комментария"
  fi
done
EOF
chmod +x task6
./task6