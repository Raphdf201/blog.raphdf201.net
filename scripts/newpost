#!/bin/bash
read -p "Title: " title
read -p "Category: " category

slug=$(echo "$title" | tr '[:upper:]' '[:lower:]' | tr ' ' '-' | tr -cd '[:alnum:]-')
date=$(date +"%Y-%m-%d %H:%M:%S %z")
file="_posts/$(date +%Y-%m-%d)-$slug.md"

cat > "$file" <<EOF
---
layout: post
title: "$title"
date: $date
categories: $category
---
## $title

content
EOF

echo "Created $file"
