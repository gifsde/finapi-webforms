# OpenAPIClient-php

The following pages give you some general information on how to use our APIs.<br/>The actual API services documentation then follows further below. You can use the menu to jump between API sections.<br/><br/>This page has a built-in HTTP(S) client, so you can test the services directly from within this page, by filling in the request parameters and/or body in the respective services, and then hitting the TRY button. Note that you need to be authorized to make a successful API call. To authorize, refer to the '<a target='_blank' href='https://docs.finapi.io/?product=access#tag--Authorization'>Authorization</a>' section of Access, or in case you already have a valid user token, just use the QUICK AUTH on the left.<br/>Please also remember that all user management functions should be looked up in <a target='_blank' href='https://docs.finapi.io/?product=access'>Access</a>.<br/><br/>You should also check out the <a target='_blank' href='https://documentation.finapi.io/webform/'>Web Form 2.0 Public Documentation</a> as well as <a target='_blank' href='https://documentation.finapi.io/access/'>Access Public Documentation</a> for more information. If you need any help with the API, contact <a href='mailto:support@finapi.io'>support@finapi.io</a>.<br/><h2 id=\"general-information\">General information</h2><h3 id=\"general-request-ids\"><strong>Request IDs</strong></h3>With any API call, you can pass a request ID via a header with name \"X-Request-Id\". The request ID can be an arbitrary string with up to 255 characters. Passing a longer string will result in an error.<br/><br/>If you don't pass a request ID for a call, finAPI will generate a random ID internally.<br/><br/>The request ID is always returned back in the response of a service, as a header with name \"X-Request-Id\".<br/><br/>We highly recommend to always pass a (preferably unique) request ID, and include it into your client application logs whenever you make a request or receive a response(especially in the case of an error response). finAPI is also logging request IDs on its end. Having a request ID can help the finAPI support team to work more efficiently and solve tickets faster.<h3 id=\"type-coercion\"><strong>Type Coercion</strong></h3>In order to ease the integration for some languages, which do not natively support high precision number representations, Web Form 2.0 API supports relax type binding for the openAPI type <code>number</code>, which is used for money amount fields. If you use one of those languages, to avoid precision errors that can appear from <code>float</code> values, you can pass the amount as a <code>string</code>.<h3 id=\"general-faq\"><strong>FAQ</strong></h3><strong>Is there a finAPI SDK?</strong><br/>Currently we do not offer a native SDK, but there is the option to generate an SDKfor almost any target language via OpenAPI. Use the 'Download SDK' button on this page for SDK generation.<br/><br/><strong>Why do I need to keep authorizing when calling services on this page?</strong><br/>This page is a \"one-page-app\". Reloading the page resets the OAuth authorization context. There is generally no need to reload the page, so just don't do it and your authorization will persist.


## Installation & Usage

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https:////.git"
    }
  ],
  "require": {
    "/": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure OAuth2 access token for authorization: BearerAccessToken
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AccountInformationServicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$bank_connection_update_task_details = new \OpenAPI\Client\Model\BankConnectionUpdateTaskDetails(); // \OpenAPI\Client\Model\BankConnectionUpdateTaskDetails

try {
    $result = $apiInstance->createBankConnectionUpdateTask($bank_connection_update_task_details);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountInformationServicesApi->createBankConnectionUpdateTask: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://webform-sandbox.finapi.io*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AccountInformationServicesApi* | [**createBankConnectionUpdateTask**](docs/Api/AccountInformationServicesApi.md#createbankconnectionupdatetask) | **POST** /api/tasks/backgroundUpdate | Update a bank connection
*AccountInformationServicesApi* | [**createForBankConnectionImport**](docs/Api/AccountInformationServicesApi.md#createforbankconnectionimport) | **POST** /api/webForms/bankConnectionImport | Import a bank connection
*CustomisationProfilesApi* | [**createProfile**](docs/Api/CustomisationProfilesApi.md#createprofile) | **POST** /api/profiles | Create a profile
*CustomisationProfilesApi* | [**deleteProfile**](docs/Api/CustomisationProfilesApi.md#deleteprofile) | **DELETE** /api/profiles/{id} | Delete a profile
*CustomisationProfilesApi* | [**editProfile**](docs/Api/CustomisationProfilesApi.md#editprofile) | **PATCH** /api/profiles/{id} | Edit a profile
*CustomisationProfilesApi* | [**getProfile**](docs/Api/CustomisationProfilesApi.md#getprofile) | **GET** /api/profiles/{id} | Get a profile
*CustomisationProfilesApi* | [**getProfiles**](docs/Api/CustomisationProfilesApi.md#getprofiles) | **GET** /api/profiles | Get profiles
*CustomisationTranslationsBETAApi* | [**createTranslation**](docs/Api/CustomisationTranslationsBETAApi.md#createtranslation) | **POST** /api/translations | Create a translation (BETA)
*CustomisationTranslationsBETAApi* | [**deleteTranslation**](docs/Api/CustomisationTranslationsBETAApi.md#deletetranslation) | **DELETE** /api/translations/{id} | Delete a translation (BETA)
*CustomisationTranslationsBETAApi* | [**getTranslation**](docs/Api/CustomisationTranslationsBETAApi.md#gettranslation) | **GET** /api/translations/{id} | Get a translation (BETA)
*CustomisationTranslationsBETAApi* | [**getTranslations**](docs/Api/CustomisationTranslationsBETAApi.md#gettranslations) | **GET** /api/translations | Get translations (BETA)
*PaymentInitiationServicesApi* | [**createForDirectDebitWithAccountId**](docs/Api/PaymentInitiationServicesApi.md#createfordirectdebitwithaccountid) | **POST** /api/webForms/directDebitWithAccountId | Create a direct debit with account ID
*PaymentInitiationServicesApi* | [**createForPaymentWithAccountId**](docs/Api/PaymentInitiationServicesApi.md#createforpaymentwithaccountid) | **POST** /api/webForms/paymentWithAccountId | Create a payment with account ID
*PaymentInitiationServicesApi* | [**createForStandalonePayment**](docs/Api/PaymentInitiationServicesApi.md#createforstandalonepayment) | **POST** /api/webForms/standalonePayment | Create a standalone payment
*PaymentInitiationServicesApi* | [**createForStandingOrder**](docs/Api/PaymentInitiationServicesApi.md#createforstandingorder) | **POST** /api/webForms/standingOrder | Create a standing order
*TasksApi* | [**getTask**](docs/Api/TasksApi.md#gettask) | **GET** /api/tasks/{id} | Get a task
*TasksApi* | [**getTasks**](docs/Api/TasksApi.md#gettasks) | **GET** /api/tasks | Get tasks
*WebFormsApi* | [**deleteWebForm**](docs/Api/WebFormsApi.md#deletewebform) | **DELETE** /api/webForms/{id} | Delete a web form
*WebFormsApi* | [**getWebForm**](docs/Api/WebFormsApi.md#getwebform) | **GET** /api/webForms/{id} | Get a web form
*WebFormsApi* | [**getWebForms**](docs/Api/WebFormsApi.md#getwebforms) | **GET** /api/webForms | Get web forms

## Models

- [AccountType](docs/Model/AccountType.md)
- [AddressData](docs/Model/AddressData.md)
- [Amount](docs/Model/Amount.md)
- [Aspect](docs/Model/Aspect.md)
- [BankConnectionImportDetails](docs/Model/BankConnectionImportDetails.md)
- [BankConnectionUpdateTaskDetails](docs/Model/BankConnectionUpdateTaskDetails.md)
- [Brand](docs/Model/Brand.md)
- [Callbacks](docs/Model/Callbacks.md)
- [Color](docs/Model/Color.md)
- [CountryCode](docs/Model/CountryCode.md)
- [CreateProfileDetails](docs/Model/CreateProfileDetails.md)
- [CreateTranslationDetails](docs/Model/CreateTranslationDetails.md)
- [Currency](docs/Model/Currency.md)
- [DirectDebitOrder](docs/Model/DirectDebitOrder.md)
- [DirectDebitWithAccountDetails](docs/Model/DirectDebitWithAccountDetails.md)
- [DirectDebitWithAccountReceiver](docs/Model/DirectDebitWithAccountReceiver.md)
- [EditProfileDetails](docs/Model/EditProfileDetails.md)
- [Error](docs/Model/Error.md)
- [Functionality](docs/Model/Functionality.md)
- [Icon](docs/Model/Icon.md)
- [ImportBankDetails](docs/Model/ImportBankDetails.md)
- [InvalidFieldError](docs/Model/InvalidFieldError.md)
- [Language](docs/Model/Language.md)
- [ManageSavedSettings](docs/Model/ManageSavedSettings.md)
- [Paging](docs/Model/Paging.md)
- [Payload](docs/Model/Payload.md)
- [PaymentPayer](docs/Model/PaymentPayer.md)
- [PaymentWithAccountDetails](docs/Model/PaymentWithAccountDetails.md)
- [PaymentWithAccountOrder](docs/Model/PaymentWithAccountOrder.md)
- [PaymentWithAccountRecipient](docs/Model/PaymentWithAccountRecipient.md)
- [PaymentWithAccountSender](docs/Model/PaymentWithAccountSender.md)
- [Profile](docs/Model/Profile.md)
- [ProfilesPage](docs/Model/ProfilesPage.md)
- [Recipient](docs/Model/Recipient.md)
- [Sender](docs/Model/Sender.md)
- [ShortTranslationBlock](docs/Model/ShortTranslationBlock.md)
- [StandalonePaymentDetails](docs/Model/StandalonePaymentDetails.md)
- [StandalonePaymentOrder](docs/Model/StandalonePaymentOrder.md)
- [StandalonePaymentRecipient](docs/Model/StandalonePaymentRecipient.md)
- [StandingOrderDetails](docs/Model/StandingOrderDetails.md)
- [Task](docs/Model/Task.md)
- [TaskCallback](docs/Model/TaskCallback.md)
- [TaskCallbacks](docs/Model/TaskCallbacks.md)
- [TaskPayload](docs/Model/TaskPayload.md)
- [TaskStatus](docs/Model/TaskStatus.md)
- [TaskType](docs/Model/TaskType.md)
- [TasksPage](docs/Model/TasksPage.md)
- [Text](docs/Model/Text.md)
- [TextColor](docs/Model/TextColor.md)
- [Translation](docs/Model/Translation.md)
- [TranslationBlock](docs/Model/TranslationBlock.md)
- [TranslationSet](docs/Model/TranslationSet.md)
- [TranslationSetsPage](docs/Model/TranslationSetsPage.md)
- [UserMetadata](docs/Model/UserMetadata.md)
- [ValidationError](docs/Model/ValidationError.md)
- [WebForm](docs/Model/WebForm.md)
- [WebFormCompletedCallback](docs/Model/WebFormCompletedCallback.md)
- [WebFormInfo](docs/Model/WebFormInfo.md)
- [WebFormStatus](docs/Model/WebFormStatus.md)
- [WebFormType](docs/Model/WebFormType.md)
- [WebFormsPage](docs/Model/WebFormsPage.md)

## Authorization

### BearerAccessToken

- **Type**: `OAuth`
- **Flow**: `password`
- **Authorization URL**: ``
- **Scopes**: 
    - **all**: no limitations

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `2.634.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
