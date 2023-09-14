-:
	@. ~/.nvm/nvm.sh && nvm install v18.17.1 || echo "install nvm!!!"
	@. ~/.nvm/nvm.sh && nvm use
install:
	@install gnostr-org /usr/local/bin/
	@$(MAKE) npm-install
npm-install:
	@npm install https://github.com/gnostr-org/node-webrtc/archive/refs/tags/v0.4.7.tar.gz
	@npm install
npm-start:
	@npm start
run:npm-install npm-start
