# Changelog of Statement Tap Framework

All notable changes to this project will be documented in this file.

## 3.1.0 - 2022-07-08

### Added

- **pngLogoUrl** field  within **StatementBank** for the logo in PNG format
- support for sending unlisted BankCode from **getEnabledBanks()** function to **checkout()** function

## 3.0.0 - 2022-05-26

### Added

- **downloadStatement()** function to return the statement list in Data format or to directly download Statement List to the mobile phone in **CSV** format
-  support for statement retrieval for Corporate Accounts
-  **isCorporate** field on DirectBank

### Changed

-  sorted returned banks from **getEnabledBanks()** function
-  automatic bank selection when only 1 bank code is passed via **bankCodes** within **StatementTapRequest**
-  renamed **Bank** to **StatementBank**
-  renamed **BankCode** to **StatementBankCode**
-  renamed **Account** to **StatementAccount**

### Fixed

-  enabling of autoConsent within **StatementTapRequest**
-  retrieval of statement list when StatementRetrievalRequest is passed

## 2.1.2 - 2022-04-29

### Fixed

-  returning of errors via **checkout** function when StatementRetrieval is passed

## 2.1.1 - 2022-04-27

### Fixed

-  returning of errors via **checkout** function

## 2.1.0 - 2022-04-18

### Changed

-  getEnabledBanks parameter **closure: @escaping ([BankCode], String?) -> Void** to **closure: @escaping ([Bank], String?) -> Void**

## 2.0.0 - 2022-02-24

### Added

- option to do Statement Retrieval via **StatementRetrievalRequest** passed inside **StatementTapRequest** after Tap Web Session
- added separate function **retrieveCheckoutURL** to get the checkout URL
- added **getEnabledBanks** function to retrieve available banks for statement retrieval

### Changed

- removed **showInBrowser** option from **StatementTapRequest** because just retrieving the URL is already in another function
- **bankCodes** from **StatementTapRequest** now accepts **nil** value; if it is set to nil, all enabled banks will be shown automatically in the Tap Web Application

## 1.4.0 - 2022-01-13

### Added

- function for retrieving the current Framework Version
- function for retrieving the Mobile Application Signature (Bundle Identifier and Seed ID)
- support for transactional retries within the WebView

## 1.3.0 - 2022-01-07

### Fixed

- End of transaction (success or failure) detection within the WebView for the new URL Format

## 1.2.0 - 2021-11-22

### Added

- option to hide the Back Button on the Navigation Bar

## 1.1.0 - 2021-10-26

### Changed

- Minimum **iOS Version** from **11** to **12**

### Added

- BPI and BDO **errorCode** to **onResult** function from **CoreDelegate**

## 1.0.2 - 2021-09-10

### Fixed

- closing of webview when transaction is cancelled or failed

## 1.0.1 - 2021-09-02

### Fixed

- **bankList** not reflecting on Tap Web Application if defined inside the **StatementTapRequest** constructor instead of using the accessor

## 1.0.0 - 2021-08-13

### Added

- initialize() function that accepts the API Key and the chosen environment to interact with (Sandbox or Production)
- checkout() function that is used to redirect the use the Tap Web Application for Statement Retrieval
- clearRememberMe() function that clears all credentials saved within the custom WKWebView
