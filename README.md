# Awesome Peppol [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of specifications, software, libraries, tools and learning resources for the Peppol e-invoicing and e-procurement network.

[Peppol](https://peppol.org/) is a network for the exchange of electronic business documents such as invoices and orders. It uses the AS4 messaging protocol, Service Metadata Publishers (SMP) and the Service Metadata Locator (SML). OpenPeppol governs the network and publishes the Peppol BIS specifications.

This list is vendor-neutral. Entries from commercial and open-source projects appear on equal terms, in alphabetical order within each section.

## Contents

- [Specifications](#specifications)
- [National specifications](#national-specifications)
- [Access Points and AS4](#access-points-and-as4)
- [SMP servers](#smp-servers)
- [Libraries](#libraries)
  - [JavaScript and TypeScript](#javascript-and-typescript)
  - [PHP](#php)
  - [Python](#python)
  - [Ruby](#ruby)
  - [Go](#go)
  - [Java](#java)
  - [Other languages](#other-languages)
- [Validation](#validation)
- [Conversion and rendering](#conversion-and-rendering)
- [Command-line tools](#command-line-tools)
- [MCP servers and agent skills](#mcp-servers-and-agent-skills)
- [Directories and lookup](#directories-and-lookup)
- [Test tools and sample files](#test-tools-and-sample-files)
- [Learning resources](#learning-resources)
- [Related lists](#related-lists)

## Specifications

- [BIS Billing 3.0](https://docs.peppol.eu/poacc/billing/3.0/) - Peppol BIS Billing 3.0 specification with syntax bindings, business rules, code lists and examples.
- [BIS Billing 3.0 national rules](https://docs.peppol.eu/poacc/billing/3.0/national-rules/) - Country-specific BIS Billing 3.0 rules that apply based on the country of the seller.
- [BIS Billing 3.0 source](https://github.com/OpenPeppol/peppol-bis-invoice-3) - OpenPeppol repository with the Schematron rules, example files and sources of BIS Billing 3.0.
- [eDelivery code lists](https://docs.peppol.eu/edelivery/codelists/) - Peppol code lists for participant identifier schemes, document types, processes and transport profiles.
- [eDelivery specifications](https://docs.peppol.eu/edelivery/) - Peppol network specifications for SML, SMP, AS4, SBDH, identifiers and reporting.
- [EN 16931 at the European Commission](https://ec.europa.eu/digital-building-blocks/sites/display/DIGITAL/eInvoicing) - European Commission pages about EN 16931, the eInvoicing directive and implementation support.
- [EN 16931 validation artefacts](https://github.com/ConnectingEurope/eInvoicing-EN16931) - CEN/TC 434 Schematron and XSLT artefacts that validate UBL and CII invoices against EN 16931.
- [Peppol AS4 profile](https://docs.peppol.eu/edelivery/as4/specification/) - Current specification of the AS4 profile that Peppol Access Points use to exchange documents.
- [Peppol Interoperability Framework](https://peppol.org/learn-more/peppol-interoperability-framework/) - OpenPeppol agreements, policies and governance documents that define the Peppol network.
- [Peppol Post-Award BIS 3](https://docs.peppol.eu/poacc/upgrade-3/) - Specifications for orders, despatch advice, catalogues, message level response and other post-award documents.
- [PINT](https://docs.peppol.eu/poac/pint/pint/) - Peppol International invoice model that regional specializations such as PINT EU, PINT JP and PINT SG extend.
- [PINT EU](https://docs.peppol.eu/poac/eu/pint-eu/) - European specialization of PINT, aligned with Peppol BIS Billing 3.0 and EN 16931.

## National specifications

Country-specific usage of EN 16931 and Peppol.

- [A-NZ Peppol BIS 3.0](https://github.com/A-NZ-PEPPOL/A-NZ-PEPPOL-BIS-3.0) - Australia and New Zealand extensions to the Peppol BIS Billing 3.0 specification.
- [Belgian e-invoicing portal](https://einvoice.belgium.be/) - Belgian federal government information site about e-invoicing and the use of Peppol in Belgium.
- [EHF](https://anskaffelser.dev/) - Documentation of the Norwegian EHF formats that are exchanged over Peppol in Norway.
- [Factur-X](https://fnfe-mpe.org/factur-x/) - French and German hybrid PDF and XML invoice format, often converted to and from Peppol UBL.
- [InvoiceNow](https://www.imda.gov.sg/how-we-can-help/nationwide-e-invoicing-framework) - Singapore nationwide e-invoicing framework, run by IMDA and based on the Peppol network.
- [PINT JP](https://docs.peppol.eu/poac/jp/) - Japanese specializations of PINT for e-invoicing over Peppol in Japan.
- [PINT SG](https://docs.peppol.eu/poac/sg/) - Singapore specializations of PINT that InvoiceNow uses.
- [SI-UBL and NLCIUS validation](https://github.com/peppolautoriteit-nl/validation) - Dutch Peppol Authority validation artefacts for the SI-UBL and NLCIUS formats.
- [XRechnung](https://xeinkauf.de/xrechnung/) - German CIUS of EN 16931, published by KoSIT and XEinkauf, also exchanged over Peppol.
- [XRechnung Schematron](https://github.com/itplr-kosit/xrechnung-schematron) - Official Schematron rules for the German XRechnung CIUS, mirrored from the KoSIT GitLab.

## Access Points and AS4

Software that sends and receives Peppol documents over AS4.

- [Domibus](https://ec.europa.eu/digital-building-blocks/sites/spaces/DIGITAL/pages/467110244/Domibus) - European Commission reference implementation of the eDelivery AS4 profile, written in Java.
- [Holodeck B2B](https://github.com/holodeck-b2b/Holodeck-B2B) - Java AS4 messaging gateway that implements the OASIS ebMS3 and AS4 specifications.
- [Node42 eDelivery](https://github.com/node42-dev/node42-edelivery) - Node.js Peppol toolkit for SMP lookup, document validation and AS4 sending and receiving.
- [Oxalis](https://github.com/OxalisCommunity/oxalis) - Original open-source Java Peppol Access Point. New feature work happens in Oxalis-NG.
- [Oxalis-NG](https://github.com/OxalisCommunity/oxalis-ng) - Next generation of Oxalis, an open-source Java implementation of the OpenPeppol AS4 profile.
- [phase4](https://github.com/phax/phase4) - Embeddable Java AS4 client and server with built-in Peppol and EC eDelivery profiles.
- [phoss AP](https://github.com/phax/phoss-ap) - Open-source Peppol Access Point built on phase4 and Spring Boot.

## SMP servers

Servers that publish the capabilities and endpoints of Peppol participants.

- [DomiSMP](https://ec.europa.eu/digital-building-blocks/sites/display/DIGITAL/DomiSMP) - European Commission reference SMP implementation for the eDelivery building block.
- [Holodeck SMP](https://github.com/holodeck-b2b/Holodeck-SMP) - SMP server based on the OASIS BDXR SMP and Peppol SMP specifications.
- [phoss SMP](https://github.com/phax/phoss-smp) - SMP server for Peppol SMP and OASIS BDXR SMP 1.0 and 2.0, with management UI and Docker images.

## Libraries

### JavaScript and TypeScript

- [e-invoice-api](https://github.com/e-invoice-be/e-invoice-ts) - TypeScript client for the e-invoice.be Peppol API, published on npm as `e-invoice-api`.
- [e-invoice-eu](https://github.com/gflohr/e-invoice-eu) - Generates EN 16931 invoices as UBL, CII, XRechnung or Factur-X from spreadsheet or JSON data.
- [einvoicing](https://github.com/esvit/einvoicing) - JavaScript library to create and parse EN 16931 invoices, with support for Peppol BIS.
- [peppol-billing](https://github.com/alpha-service/peppol-billing) - Typed TypeScript library to generate and parse Peppol BIS Billing 3.0 invoices and credit notes.
- [peppol-toolkit](https://github.com/PixelDrive/peppol-toolkit) - TypeScript toolkit to prepare and read documents for e-invoicing and Peppol integration.

### PHP

- [e-invoice-api](https://github.com/e-invoice-be/e-invoice-php) - PHP client for the e-invoice.be Peppol API, published on Packagist as `e-invoice/e-invoice-api`.
- [e-invoicing](https://github.com/easybill/e-invoicing) - PHP library from easybill to generate and read EN 16931 XML in UBL and CII syntax.
- [einvoicing](https://github.com/josemmo/einvoicing) - PHP library to read and create EN 16931 invoices, with a Peppol BIS preset.
- [ubl-invoice](https://github.com/num-num/ubl-invoice) - Object-oriented PHP library to read and create UBL and Peppol BIS files.

### Python

- [e-invoice-api](https://github.com/e-invoice-be/e-invoice-py) - Python client for the e-invoice.be Peppol API, published on PyPI as `e-invoice-api`.
- [peppol-py](https://github.com/iterasdev/peppol-py) - Python implementation to send Peppol eDelivery AS4 documents, also published on PyPI.

### Ruby

- [e-invoice-api](https://github.com/e-invoice-be/e-invoice-rb) - Ruby client for the e-invoice.be Peppol API, published on RubyGems as `e-invoice-api`.

### Go

- [einvoice](https://github.com/speedata/einvoice) - Go library to read, write and verify EN 16931 invoices that detects Peppol BIS Billing 3.0 rules.

### Java

- [e-invoice-java](https://github.com/e-invoice-be/e-invoice-java) - Java client for the e-invoice.be Peppol API.
- [peppol-bis-billing-3-generator](https://github.com/digipost/peppol-bis-billing-3-generator) - Java code from Digipost that generates Peppol BIS Billing 3.0 invoice XML.
- [peppol-commons](https://github.com/phax/peppol-commons) - Shared Peppol components for identifiers, code lists, SBDH, SMP and SML clients, MLR and MLS.
- [peppol-reporting](https://github.com/phax/peppol-reporting) - Java library for Peppol Transaction Statistics Reports (TSR) and End User Statistics Reports (EUSR).
- [ph-sbdh](https://github.com/phax/ph-sbdh) - Java library to read and write UN/CEFACT Standard Business Document Header (SBDH) documents.
- [ph-ubl](https://github.com/phax/ph-ubl) - Java library to read and write UBL 2.0, 2.1, 2.2, 2.3, 2.4 and 2.5 documents.
- [vefa-peppol](https://github.com/OxalisCommunity/vefa-peppol) - Peppol support library from the Oxalis community, used by the Oxalis Access Point.

### Other languages

- [XRechnung for Delphi](https://github.com/LandrixSoftware/XRechnung-for-Delphi) - XRechnung, ZUGFeRD and Peppol BIS Billing implementation for Delphi and Free Pascal.

## Validation

- [e-invoice.be Peppol Validator](https://e-invoice.be/peppol-validator) - Online validator for Peppol BIS 3.0 and UBL 2.1 invoices against EN 16931 and Peppol Schematron rules.
- [EU eInvoicing validator](https://www.itb.ec.europa.eu/invoice/upload) - European Commission online validator for EN 16931 invoices in UBL and CII syntax.
- [KoSIT Validator](https://github.com/itplr-kosit/validator) - Java command-line tool and library that validates XML with XML Schema and Schematron scenarios.
- [KoSIT Validator configuration for Peppol BIS](https://github.com/itplr-kosit/validator-configuration-bis) - Ready-to-use KoSIT Validator scenarios for Peppol BIS Billing 3.0.
- [Mustang](https://github.com/ZUGFeRD/mustangproject) - Java library, validator and command-line tool for Factur-X, ZUGFeRD, XRechnung and CII invoices.
- [Peppol Practical validation](https://peppol.helger.com/public/menuitem-validation-upload) - Online upload validator based on phive for Peppol BIS and many national rule sets.
- [peppolvalidator.com](https://peppolvalidator.com/) - Online validator for UBL invoices and credit notes against BIS Billing 3.0, EN 16931 and national rules.
- [ph-schematron](https://github.com/phax/ph-schematron) - Java Schematron library with pure, XSLT and SchXslt engines.
- [phive](https://github.com/phax/phive) - Generic Java validation engine for business documents, based on XML Schema and Schematron.
- [phive-rules](https://github.com/phax/phive-rules) - Validation rule sets for phive, including Peppol BIS, EN 16931, XRechnung and other national formats.

## Conversion and rendering

- [BIS presentation XSLT](https://github.com/SingleFaceToIndustry/bis_presentation_xslt) - XSLT stylesheets that render key Peppol BIS transactions in a human-readable form.
- [en16931-cii2ubl](https://github.com/phax/en16931-cii2ubl) - Java converter for EN 16931 invoices from UN/CEFACT CII to UBL.
- [GOBL UBL](https://github.com/invopop/gobl.ubl) - Go library that converts GOBL documents to and from UBL, with a Peppol context.
- [XRechnung visualization](https://github.com/itplr-kosit/xrechnung-visualization) - XSL transformations that render XRechnung and EN 16931 invoices as HTML or PDF.

## Command-line tools

- [e-invoice-eu CLI](https://github.com/gflohr/e-invoice-eu/tree/main/apps/cli) - Command-line tool that generates EN 16931 invoices, including UBL, published on npm as `@e-invoice-eu/cli`.
- [Peppol CLI](https://github.com/e-invoice-be/peppol-cli) - Command-line client for Peppol to send and receive documents, validate XML files and look up participants.

## MCP servers and agent skills

Model Context Protocol servers and skills that give AI assistants access to Peppol data or services.

- [Billit MCP](https://github.com/eltyBelgium/billit-mcp) - MCP server for the Belgian Billit e-invoicing and Peppol platform API.
- [e-invoice.be MCP server](https://e-invoice.be/mcp) - Remote MCP server at `api.e-invoice.be/mcp` with read-only tools for documents, deliveries and participant lookup.
- [e-invoice.be Peppol skill](https://www.skills.sh/e-invoice-be/peppol-cli/peppol) - Agent skill for the Peppol CLI. Install it with `npx skills add e-invoice-be/peppol-cli`.
- [eu-business-data-mcp](https://github.com/wsystemdev/eu-business-data-mcp) - Remote MCP server with tools for Peppol Directory routing, EN 16931 validation, UBL invoice creation and EU VAT checks.
- [mcp-einvoicing-be](https://github.com/cmendezs/mcp-einvoicing-be) - MCP server to validate, generate and transform Belgian Peppol BIS 3.0 invoices and look up participants.
- [mcp-peppol](https://github.com/pipeworx-io/mcp-peppol) - MCP server for Peppol participant lookup through the SML, SMPs and the Peppol Directory.
- [phoss Peppol MCP](https://github.com/Helger-IT/phoss-peppol-mcp) - Java MCP server with tools for SMP lookup, document type support checks and Peppol DNS resolution.

## Directories and lookup

- [Certified Peppol Service Providers](https://peppol.org/members/peppol-certified-service-providers/) - OpenPeppol list of certified Access Point and SMP service providers.
- [e-invoice.be Peppol Radar](https://e-invoice.be/peppol-radar) - Web tool to look up Peppol IDs and check registration status, with bulk checks from a CSV file.
- [Peppol Directory](https://directory.peppol.eu/) - Official OpenPeppol search for registered participants, with XML, JSON and CSV exports.
- [Peppol Practical participant check](https://peppol.helger.com/public/menuitem-tools-participant) - Online tool to query the SML and SMP records of a Peppol participant identifier.
- [phoss Directory](https://github.com/phax/phoss-directory) - Software that runs the Peppol Directory, with indexer, publisher, client and search API.
- [SMP Query Webapp](https://github.com/Helger-IT/smp-query-webapp) - Self-hostable web application that queries Peppol SMPs and returns JSON results.

## Test tools and sample files

- [BIS Billing 3.0 examples](https://github.com/OpenPeppol/peppol-bis-invoice-3/tree/master/rules/examples) - Official OpenPeppol example invoices and credit notes for Peppol BIS Billing 3.0.
- [NPa Peppol Test Tool](https://test.peppolautoriteit.nl/) - Dutch Peppol Authority tool to send and receive test documents on the Peppol test network.
- [Peppol Testbed](https://www.testbed.peppol.org/) - OpenPeppol conformance testing platform for Access Point and SMP service providers.
- [SI-UBL test set](https://github.com/peppolautoriteit-nl/testset) - Dutch Peppol Authority test documents for SI-UBL that should pass, warn or fail validation.
- [XRechnung test suite](https://github.com/itplr-kosit/xrechnung-testsuite) - Test instances for the XRechnung standard, published by KoSIT.

## Learning resources

- [Comparison of AS4 solutions for Peppol](https://xeinkauf.de/app/uploads/2023/09/Comparison_of_AS4_solutions_for_Peppol.pdf) - XEinkauf comparison of AS4 software for use in the Peppol network (PDF, 2023).
- [How to set up a Peppol Access Point](https://peppol.org/wp-content/uploads/2024/04/how_to_set-up_a__post-award__peppol_access_point_v2.1.pdf) - OpenPeppol guide to becoming a certified post-award Peppol service provider (PDF).
- [OpenPeppol Service Desk](https://openpeppol.atlassian.net/servicedesk/customer/portals) - Official portal for specification questions, test requests and onboarding of service providers.
- [Peppol country profiles](https://peppol.org/learn-more/country-profiles/) - OpenPeppol overview of Peppol adoption and the Peppol Authority in each country.
- [Peppol Practical](https://peppol.helger.com/) - Site by Philip Helger with Peppol tools and technical notes on SMP, MLR, MLS and reporting.
- [Testing in the Peppol Network](https://xeinkauf.de/app/uploads/2023/09/2023-08-17_Testing_in_the_Peppol_Network_V1.1_eng.pdf) - XEinkauf guide to test methods for Peppol service providers (PDF, 2023).

## Related lists

- [awesome-billing](https://github.com/kdeldycke/awesome-billing) - Billing and payments knowledge for cloud platforms, including e-invoicing.
- [awesome-einvoicing](https://github.com/facturxapi/awesome-einvoicing) - Sourced map of e-invoicing specifications, validators, libraries and corpora for EN 16931 and national formats.
- [awesome-europe](https://github.com/GeiserX/awesome-europe) - Open-source software for European institutions, regulations and standards, including electronic invoicing.
- [awesome-invoicing](https://github.com/causa-prima-ai/awesome-invoicing) - Invoicing and e-invoicing tools for freelancers and small businesses.

## Contributing

Contributions are welcome. Read the [contribution guidelines](contributing.md) first.
