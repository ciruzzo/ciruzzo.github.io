# ===== 設定 =====
MD = slides.md
HTML = index.html
PDF = output.pdf

FONT = "Noto Sans CJK JP"
MONO = "Noto Sans Mono CJK JP"

# ===== デフォルト =====
all: html pdf

# HTML生成
html:
	pandoc $(MD) -o $(HTML)

# PDF生成（beamer + 日本語）
pdf:
	pandoc $(MD) -t beamer \
		--pdf-engine=xelatex \
		-V mainfont=$(FONT) \
		-V sansfont=$(FONT) \
		-V monofont=$(MONO) \
		-o $(PDF)

# Git反映
push: html
	git add $(MD) $(HTML)
	git commit -m "update slides" $(MD) $(HTML)
	git push

# 一括（HTML + PDF + push）
release: html pdf push

# 掃除
clean:
	rm -f $(HTML) $(PDF)
