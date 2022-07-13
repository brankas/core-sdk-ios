# Changelog of Balance Tap Framework

All notable changes to this project will be documented in this file.

## 1.1.0 - 2022-07-08

### Added

-  support for balance retrieval for Corporate Accounts
- **pngLogoUrl** field  within **BalanceBank** for the logo in PNG format
- support for sending unlisted BankCode from **getEnabledBanks()** function to **checkout()** function

### Changed

-  automatic bank selection when only 1 bank code is passed via **bankCodes** within **BalanceTapRequest**

## 1.0.0 - 2022-05-26

### Added

- **initialize()** function that accepts the API Key and the chosen environment to interact with (Sandbox or Production)
- **checkout()** function that is used to redirect the user to the Tap Web Application for Balance Retrieval inside WKWebView or Safari Web Browser
- **getEnabledBanks()** function to retrieve available banks for balance retrieval
- **retrieveCheckoutURL()** function to get the checkout URL for balance retrieval
- **getFrameworkVersion()** function for retrieving the current Framework Version
- **getBundleSeedID()** function for retrieving the Mobile Application Signature