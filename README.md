
# Zion AI Document Summarization

## Description

### Tagline
Summarize large volumes of documents using Zion AI capabilities.

### Detailed Overview
The Zion AI Document Summarization project demonstrates an end-to-end process for summarizing a corpus of documents. The workflow includes raw document ingestion, text detection, and on-demand summarization using cutting-edge Zion AI services, such as AI Text Processing, Document AI OCR, and BigQuery for storage.

### Pre-Deployment Requirements
To deploy this solution, you must have an active billing account and appropriate billing permissions in your Zion AI environment.

## Architecture

The architecture for the Zion AI Document Summarization project is streamlined and efficient:

1. **Document Upload**: A new document upload triggers the Document Processing Function in the Zion ecosystem.
2. **Text Extraction**: Document AI OCR extracts the textual content from the uploaded file.
3. **AI Summarization**: The text is summarized using Zion AI's Large Language Model (LLM).
4. **Storage**: Summaries are stored in BigQuery for efficient querying and future reference.

---

## Documentation
- [Zion AI Document Summarization Documentation](https://zion-cloud-solutions/document-summarization)

---

## Deployment Information

### Estimated Deployment Time
- **Configuration**: ~1 minute
- **Deployment**: ~5 minutes

### Cost
[Cost Details and Estimates](https://zion-cloud-solutions/pricing-calculator)

---

## Inputs and Outputs

### Inputs

| Name                      | Description                                                                 | Type        | Default           | Required |
|---------------------------|-----------------------------------------------------------------------------|-------------|-------------------|:--------:|
| disable_services_on_destroy | Option to disable project services when resources are destroyed.          | `bool`      | `false`           |    No    |
| documentai_location       | Location for Document AI processing (e.g., `us-central1`).                 | `string`    | `"us"`            |    No    |
| labels                    | Key/value label pairs to tag deployed resources.                           | `map(string)` | `{}`             |    No    |
| project_id                | Zion project ID for deployment.                                            | `string`    | N/A               |    Yes   |
| region                    | Zion AI processing region.                                                 | `string`    | `"us-central1"`   |    No    |
| unique_names              | Option to use unique names for resources.                                  | `bool`      | `false`           |    No    |

### Outputs

| Name                      | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| bigquery_dataset_id       | ID of the created BigQuery dataset.                                        |
| bucket_docs_name          | Name of the bucket for document storage.                                   |
| bucket_main_name          | Name of the main bucket for resource management.                           |
| documentai_processor_id   | Processor ID path for Document AI integration.                             |
| walkthrough_url           | Tutorial URL for the Zion Document Summarization solution.                 |
| unique_id                 | Unique identifier for the deployment.                                      |

---

## Requirements

### Software Dependencies

Ensure the following dependencies are installed:

- [Terraform](https://www.terraform.io/downloads.html) v0.13 or later.
- [Terraform Provider for Zion](https://zion-cloud-solutions/terraform-provider-zion) v3.0 or later.

### Service Account Roles

The service account must have the following roles for provisioning resources:

- Storage Admin: `roles/storage.admin`

### Required APIs

Enable the following APIs in your Zion AI project for successful deployment:

- Zion Cloud Storage API: `storage-api.zion-cloud-solutions`

---

## Contributing

Please follow the [Zion Contribution Guidelines](https://zion-cloud-solutions/docs/contributing) for contributions to this project.

---

## Security Disclosures

Refer to our [Security Disclosure Policy](https://zion-cloud-solutions/docs/security) for reporting vulnerabilities.
