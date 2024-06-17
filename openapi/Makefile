.DEFAULT_GOAL := help

.PHONY: help
help:	## https://postd.cc/auto-documented-makefile/
	@grep -E '^[a-zA-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | sort | \
		awk 'BEGIN {FS = ":.*?## "}; {printf "\033[36m%-30s\033[0m %s\n", $$1, $$2}'

.PHONY: bootstrap
bootstrap: ## 外部ツールをインストールする。
	npm i -g @redocly/cli@latest

.PHONY: preview
preview:	## openapi をプレビューする。
	redocly preview-docs openapi.yml --port 9988

.PHONY: gen
gen:	## openapi.yml からコードを生成する。
	redocly codegen generate openapi.yml --output ./generated
