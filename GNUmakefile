NODE_VERSION=v18.17.1
-:
	@. ~/.nvm/nvm.sh && nvm install v18.17.1 || echo "install nvm!!!"
	@. ~/.nvm/nvm.sh && nvm use
install:
	@install gnostr-org /usr/local/bin/
	@$(MAKE) npm-install
npm-install:
	rm -rf ~/Library/Application\ Support/gnostr-org/extensions/gnostr/web/@adonisjs || echo
	rm -rf ~/Library/Application\ Support/gnostr-org/extensions/gnostr/web/@noble || echo
	rm -rf ~/Library/Application\ Support/gnostr-org/extensions/gnostr/web/@* || echo
	@npm install
npm-start:
	@npm start
run:npm-install npm-start

.PHONY: nvm
.ONESHELL:
nvm: ## 	nvm
	@echo "$(NODE_VERSION)" > .nvmrc
	@curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/master/install.sh | bash || git pull -C $(HOME)/.nvm && export NVM_DIR="$(HOME)/.nvm" && [ -s "$(NVM_DIR)/nvm.sh" ] && \. "$(NVM_DIR)/nvm.sh" && [ -s "$(NVM_DIR)/bash_completion" ] && \. "$(NVM_DIR)/bash_completion"  && nvm install $(NODE_VERSION) && nvm use $(NODE_VERSION)
	@source ~/.bashrc && nvm alias $(NODE_ALIAS) $(NODE_VERSION) &

nvm-clean: ## 	nvm-clean
	@rm -rf ~/.nvm
