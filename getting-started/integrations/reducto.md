---
description: >-
  Learn how to connect Reducto to JetAdmin to parse documents, extract
  structured data, classify files, and build document-processing workflows
  powered by AI.
hidden: true
---

# Reducto

Reducto is an AI-powered document processing platform that helps organizations transform unstructured documents into structured, usable data. It can classify documents, parse complex layouts, extract fields, split multi-document files, and edit documents programmatically. Reducto is designed for AI workflows, document automation, and Retrieval-Augmented Generation (RAG) applications.

## Connecting Reducto

To connect your Reducto account:

1. Open the **Data** tab from the left sidebar.
2. Click **Add Resource**.
3. Select **Reducto** from the list of available resources.
4. Authenticate your Reducto account.

arcade

{% hint style="info" %}
Once connected, the Reducto resource becomes available anywhere JetAdmin supports external resources.
{% endhint %}

## What can it do?

The Reducto integration gives JetAdmin access to advanced document processing capabilities.

From JetAdmin, you can:

* Upload documents for processing
* Classify documents by type
* Parse documents into structured content
* Extract specific fields into JSON
* Split large documents into logical sections
* Edit supported documents programmatically
* Use document data inside AI Agents and workflows

Reducto supports a wide range of document types including PDFs, images, spreadsheets, presentations, and scanned documents.

## Where to use it?

Reducto is most useful whenever your application needs **document understanding**, **data extraction**, or **AI-ready document processing**.

You can use it in:

| JetAdmin feature   | Common use cases                                                                          |
| ------------------ | ----------------------------------------------------------------------------------------- |
| **AI Agents**      | Analyze documents, answer questions from files, extract structured information            |
| **Workflows**      | Automate document processing, route files, extract business data, process uploads         |
| **Internal tools** | Build document review tools, contract analyzers, invoice processors, or knowledge systems |

Typical business use cases include:

* Invoice processing
* Contract analysis
* Document classification
* Data extraction
* Knowledge base ingestion
* RAG pipelines
* Financial document processing
* Customer onboarding workflows

## Available tools (Actions)

| Action                | Description                                                                                         |
| --------------------- | --------------------------------------------------------------------------------------------------- |
| **Upload File**       | Upload a document for processing by Reducto.                                                        |
| **Classify Document** | Categorize documents into predefined document types.                                                |
| **Parse Document**    | Convert documents into structured, AI-ready content including text, tables, and layout information. |
| **Extract Data**      | Extract specific fields and return structured JSON based on a defined schema.                       |
| **Split Document**    | Divide large documents into logical sections or separate documents.                                 |
| **Edit Document**     | Modify supported documents programmatically using instructions or structured inputs.                |

## Example prompts for AI Agents

#### Extract invoice data

```
Upload this invoice to Reducto and extract the invoice number, vendor name, invoice date, and total amount.
```

#### Classify uploaded files

```
Classify all uploaded documents as invoices, contracts, bank statements, or tax documents.
```

#### Parse a contract

```
Parse this contract and summarize the key obligations, renewal terms, and termination clauses.
```

#### Build structured JSON

```
Extract customer information, billing details, and payment terms from this document and return them as structured JSON.
```

#### Split a document package

```
Split this 150-page PDF into separate documents based on document type and provide the page ranges for each section.
```

#### Process onboarding documents

```
Analyze the uploaded onboarding package and extract all customer details required for CRM creation.
```

## Example

This example demonstrates how an AI Agent can process an uploaded document with Reducto and extract structured information.

arcade

> 💡 **Recommended use case**
>
> A great demo for this integration is an **Invoice Processing Agent**:
>
> * Upload an invoice PDF
> * Classify it automatically
> * Extract invoice fields
> * Return structured JSON
> * Create a record in your database
>
> This showcases nearly every Reducto capability in a single workflow.
