CHROMEDRIVER_VERSION = 2.32
HEADLESS_CHROMIUM_VERSION = 1.0.0-29


build-SeleniumHeadlessChromium:

	# Create folders for binaries
	mkdir -p $(ARTIFACTS_DIR)/bin
	mkdir -p $(ARTIFACTS_DIR)/lib

	# Download and unzip chromedriver
	curl -SL https://chromedriver.storage.googleapis.com/$(CHROMEDRIVER_VERSION)/chromedriver_linux64.zip > $(ARTIFACTS_DIR)/chromedriver.zip
	unzip $(ARTIFACTS_DIR)/chromedriver.zip -d $(ARTIFACTS_DIR)/bin/
	rm $(ARTIFACTS_DIR)/chromedriver.zip

	# Download and unzip headless chromium
	curl -SL https://github.com/adieuadieu/serverless-chrome/releases/download/v$(HEADLESS_CHROMIUM_VERSION)/stable-headless-chromium-amazonlinux-2017-03.zip > $(ARTIFACTS_DIR)/headless-chromium.zip
	unzip $(ARTIFACTS_DIR)/headless-chromium.zip -d $(ARTIFACTS_DIR)/bin/
	rm $(ARTIFACTS_DIR)/headless-chromium.zip

	# Download shared linux libs
	curl -SL https://github.com/21Buttons/pychromeless/blob/master/lib/libORBit-2.so.0?raw=true > $(ARTIFACTS_DIR)/lib/libORBit-2.so.0
	curl -SL https://github.com/21Buttons/pychromeless/blob/master/lib/libgconf-2.so.4?raw=true > $(ARTIFACTS_DIR)/lib/libgconf-2.so.4

	# Install Python dependencies
	python -m pip install -r requirements.txt -t $(ARTIFACTS_DIR)/python
