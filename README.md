# Elasticsearch Langdetect Ingest Processor

**Note: Maintainer wanted. I cannot guarantee to keep maintaining this, so if you want to take over as a maintainer, please fork the repo, provide new packages per release and give me a ping to link to your repository!**

Uses the [langdetect](https://github.com/YouCruit/language-detection/) plugin.

Note that Elasticsearch has native support for langdetection nowadays using the
`inference` ingest processor. See more in
[the documentation](https://www.elastic.co/guide/en/machine-learning/current/ml-lang-ident.html)

**Note**: As of Elasticsearch 8.3.3 the lingua implementation has been
removed again due to issues with the security manager. Feel free to check
out previous commits and create a PR if you got it working to include it
again.

## Installation

| ES    | Command |
| ----- | ------- |
| 8.5.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.5.0.1/ingest-langdetect-8.5.0.1.zip` |
| 8.4.3 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.4.3.1/ingest-langdetect-8.4.3.1.zip` |
| 8.4.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.4.2.1/ingest-langdetect-8.4.2.1.zip` |
| 8.4.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.4.1.1/ingest-langdetect-8.4.1.1.zip` |
| 8.4.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.4.0.1/ingest-langdetect-8.4.0.1.zip` |
| 8.3.3 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.3.3.1/ingest-langdetect-8.3.3.1.zip` |
| 8.3.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.3.2.1/ingest-langdetect-8.3.2.1.zip` |
| 8.3.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.3.1.1/ingest-langdetect-8.3.1.1.zip` |
| 8.3.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.3.0.1/ingest-langdetect-8.3.0.1.zip` |
| 8.2.3 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.2.3.1/ingest-langdetect-8.2.3.1.zip` |
| 8.2.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.2.2.1/ingest-langdetect-8.2.2.1.zip` |
| 8.2.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.2.1.1/ingest-langdetect-8.2.1.1.zip` |
| 8.2.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.2.0.1/ingest-langdetect-8.2.0.1.zip` |
| 8.1.3 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.1.3.1/ingest-langdetect-8.1.3.1.zip` |
| 8.1.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.1.2.1/ingest-langdetect-8.1.2.1.zip` |
| 8.1.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.1.1.1/ingest-langdetect-8.1.1.1.zip` |
| 8.1.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.1.0.1/ingest-langdetect-8.1.0.1.zip` |
| 8.0.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.0.1.1/ingest-langdetect-8.0.1.1.zip` |
| 8.0.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.0.0.1/ingest-langdetect-8.0.0.1.zip` |
| 8.0.0-rc1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.0.0-rc1.1/ingest-langdetect-8.0.0-rc1.1.zip` |
| 8.0.0-beta1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.0.0-beta1.1/ingest-langdetect-8.0.0-beta1.1.zip` |
| 8.0.0-alpha2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/8.0.0-alpha2.1/ingest-langdetect-8.0.0-alpha2.1.zip` |
| 7.17.10 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.17.10.1/ingest-langdetect-7.17.10.1.zip` |
| 7.17.7 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.17.7.1/ingest-langdetect-7.17.7.1.zip` |
| 7.17.6 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.17.6.1/ingest-langdetect-7.17.6.1.zip` |
| 7.17.5 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.17.5.1/ingest-langdetect-7.17.5.1.zip` |
| 7.17.4 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.17.4.1/ingest-langdetect-7.17.4.1.zip` |
| 7.17.3 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.17.3.1/ingest-langdetect-7.17.3.1.zip` |
| 7.17.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.17.2.1/ingest-langdetect-7.17.2.1.zip` |
| 7.17.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.17.1.1/ingest-langdetect-7.17.1.1.zip` |
| 7.17.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.17.0.1/ingest-langdetect-7.17.0.1.zip` |
| 7.16.3 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.16.3.1/ingest-langdetect-7.16.3.1.zip` |
| 7.16.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.16.2.1/ingest-langdetect-7.16.2.1.zip` |
| 7.16.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.16.1.1/ingest-langdetect-7.16.1.1.zip` |
| 7.16.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.16.0.1/ingest-langdetect-7.16.0.1.zip` |
| 7.15.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.15.2.1/ingest-langdetect-7.15.2.1.zip` |
| 7.15.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.15.1.1/ingest-langdetect-7.15.1.1.zip` |
| 7.15.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.15.0.1/ingest-langdetect-7.15.0.1.zip` |
| 7.14.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.14.2.1/ingest-langdetect-7.14.2.1.zip` |
| 7.14.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.14.1.1/ingest-langdetect-7.14.1.1.zip` |
| 7.14.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.14.0.1/ingest-langdetect-7.14.0.1.zip` |
| 7.13.4 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.13.4.1/ingest-langdetect-7.13.4.1.zip` |
| 7.13.3 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.13.3.1/ingest-langdetect-7.13.3.1.zip` |
| 7.13.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.13.2.1/ingest-langdetect-7.13.2.1.zip` |
| 7.13.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.13.1.1/ingest-langdetect-7.13.1.1.zip` |
| 7.13.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.13.0.1/ingest-langdetect-7.13.0.1.zip` |
| 7.12.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.12.1.1/ingest-langdetect-7.12.1.1.zip` |
| 7.12.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.12.0.1/ingest-langdetect-7.12.0.1.zip` |
| 7.11.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.11.2.1/ingest-langdetect-7.11.2.1.zip` |
| 7.11.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.11.1.1/ingest-langdetect-7.11.1.1.zip` |
| 7.11.0 | Not available Elasticsearch issues |
| 7.10.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.10.2.1/ingest-langdetect-7.10.2.1.zip` |
| 7.10.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.10.1.1/ingest-langdetect-7.10.1.1.zip` |
| 7.10.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.10.0.1/ingest-langdetect-7.10.0.1.zip` |
| 7.9.3 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.9.3.1/ingest-langdetect-7.9.3.1.zip` |
| 7.9.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.9.2.1/ingest-langdetect-7.9.2.1.zip` |
| 7.9.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.9.1.1/ingest-langdetect-7.9.1.1.zip` |
| 7.9.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.9.0.1/ingest-langdetect-7.9.0.1.zip` |
| 7.8.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.8.1.1/ingest-langdetect-7.8.1.1.zip` |
| 7.8.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.8.0.1/ingest-langdetect-7.8.0.1.zip` |
| 7.7.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.7.1.1/ingest-langdetect-7.7.1.1.zip` |
| 7.7.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.7.0.1/ingest-langdetect-7.7.0.1.zip` |
| 7.6.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.6.2.1/ingest-langdetect-7.6.2.1.zip` |
| 7.6.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.6.1.1/ingest-langdetect-7.6.1.1.zip` |
| 7.6.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.6.0.1/ingest-langdetect-7.6.0.1.zip` |
| 7.5.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.5.2.1/ingest-langdetect-7.5.2.1.zip` |
| 7.5.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.5.1.1/ingest-langdetect-7.5.1.1.zip` |
| 7.5.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.5.0.1/ingest-langdetect-7.5.0.1.zip` |
| 7.4.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.4.2.1/ingest-langdetect-7.4.2.1.zip` |
| 7.4.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.4.1.1/ingest-langdetect-7.4.1.1.zip` |
| 7.4.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.4.0.1/ingest-langdetect-7.4.0.1.zip` |
| 7.3.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.3.2.1/ingest-langdetect-7.3.2.1.zip` |
| 7.3.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.3.1.1/ingest-langdetect-7.3.1.1.zip` |
| 7.3.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.3.0.1/ingest-langdetect-7.3.0.1.zip` |
| 7.2.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.2.1.1/ingest-langdetect-7.2.1.1.zip` |
| 7.2.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.2.0.1/ingest-langdetect-7.2.0.1.zip` |
| 7.1.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.1.1.1/ingest-langdetect-7.1.1.1.zip` |
| 7.1.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.1.0.1/ingest-langdetect-7.1.0.1.zip` |
| 7.0.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.0.1.1/ingest-langdetect-7.0.1.1.zip` |
| 7.0.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/7.0.0.1/ingest-langdetect-7.0.0.1.zip` |
| 6.8.23 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.23.1/ingest-langdetect-6.8.23.1.zip` |
| 6.8.22 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.22.1/ingest-langdetect-6.8.22.1.zip` |
| 6.8.21 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.21.1/ingest-langdetect-6.8.21.1.zip` |
| 6.8.20 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.20.1/ingest-langdetect-6.8.20.1.zip` |
| 6.8.19 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.19.1/ingest-langdetect-6.8.19.1.zip` |
| 6.8.18 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.18.1/ingest-langdetect-6.8.18.1.zip` |
| 6.8.17 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.17.1/ingest-langdetect-6.8.17.1.zip` |
| 6.8.16 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.16.1/ingest-langdetect-6.8.16.1.zip` |
| 6.8.15 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.15.1/ingest-langdetect-6.8.15.1.zip` |
| 6.8.14 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.14.1/ingest-langdetect-6.8.14.1.zip` |
| 6.8.13 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.13.1/ingest-langdetect-6.8.13.1.zip` |
| 6.8.12 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.12.1/ingest-langdetect-6.8.12.1.zip` |
| 6.8.11 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.11.1/ingest-langdetect-6.8.11.1.zip` |
| 6.8.10 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.10.1/ingest-langdetect-6.8.10.1.zip` |
| 6.8.9 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.9.1/ingest-langdetect-6.8.9.1.zip` |
| 6.8.8 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.8.1/ingest-langdetect-6.8.8.1.zip` |
| 6.8.7 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.7.1/ingest-langdetect-6.8.7.1.zip` |
| 6.8.6 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.6.1/ingest-langdetect-6.8.6.1.zip` |
| 6.8.5 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.5.1/ingest-langdetect-6.8.5.1.zip` |
| 6.8.4 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.4.1/ingest-langdetect-6.8.4.1.zip` |
| 6.8.3 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.3.1/ingest-langdetect-6.8.3.1.zip` |
| 6.8.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.2.1/ingest-langdetect-6.8.2.1.zip` |
| 6.8.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.1.1/ingest-langdetect-6.8.1.1.zip` |
| 6.8.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.8.0.1/ingest-langdetect-6.8.0.1.zip` |
| 6.7.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.7.2.1/ingest-langdetect-6.7.2.1.zip` |
| 6.7.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.7.1.1/ingest-langdetect-6.7.1.1.zip` |
| 6.7.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.7.0.1/ingest-langdetect-6.7.0.1.zip` |
| 6.6.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.6.2.1/ingest-langdetect-6.6.2.1.zip` |
| 6.6.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.6.1.1/ingest-langdetect-6.6.1.1.zip` |
| 6.6.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.6.0.1/ingest-langdetect-6.6.0.1.zip` |
| 6.5.4 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.5.4.1/ingest-langdetect-6.5.4.1.zip` |
| 6.5.3 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.5.3.1/ingest-langdetect-6.5.3.1.zip` |
| 6.5.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.5.2.1/ingest-langdetect-6.5.2.1.zip` |
| 6.5.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.5.1.1/ingest-langdetect-6.5.1.1.zip` |
| 6.5.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.5.0.1/ingest-langdetect-6.5.0.1.zip` |
| 6.4.3 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.4.3.1/ingest-langdetect-6.4.3.1.zip` |
| 6.4.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.4.2.1/ingest-langdetect-6.4.2.1.zip` |
| 6.4.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.4.1.1/ingest-langdetect-6.4.1.1.zip` |
| 6.4.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.4.0.1/ingest-langdetect-6.4.0.1.zip` |
| 6.3.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.3.2.1/ingest-langdetect-6.3.2.1.zip` |
| 6.3.1 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.3.1.1/ingest-langdetect-6.3.1.1.zip` |
| 6.3.0 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.3.0.1/ingest-langdetect-6.3.0.1.zip` |
| 6.2.4 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.2.4.1/ingest-langdetect-6.2.4.1.zip` |
| 6.2.3 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.2.3.1/ingest-langdetect-6.2.3.1.zip` |
| 6.2.2 | `bin/elasticsearch-plugin install https://github.com/spinscale/elasticsearch-ingest-langdetect/releases/download/6.2.2.1/ingest-langdetect-6.2.2.1.zip` |
| 5.2.0 | `bin/elasticsearch-plugin install https://oss.sonatype.org/content/repositories/releases/de/spinscale/elasticsearch/plugin/ingest-langdetect/5.2.0.1/ingest-langdetect-5.2.0.1.zip` |
| 5.1.2 | `bin/elasticsearch-plugin install https://oss.sonatype.org/content/repositories/releases/de/spinscale/elasticsearch/plugin/ingest-langdetect/5.1.2.1/ingest-langdetect-5.1.2.1.zip` |
| 5.1.1 | `bin/elasticsearch-plugin install https://oss.sonatype.org/content/repositories/releases/de/spinscale/elasticsearch/plugin/ingest-langdetect/5.1.1.1/ingest-langdetect-5.1.1.1.zip` |

## Usage


```
PUT _ingest/pipeline/langdetect-pipeline
{
  "description": "A pipeline to do whatever",
  "processors": [
    {
      "langdetect" : {
        "field" : "my_field",
        "target_field" : "language"
      }
    }
  ]
}

PUT /my-index/my-type/1?pipeline=langdetect-pipeline
{
  "my_field" : "This is hopefully an english text, that will be detected."
}

GET /my-index/my-type/1

# Expected response
{
  "my_field" : "This is hopefully an english text, that will be detected.",
  "language": "en"
}
```

You could also set certain fields that use different analyzers for different languages

```
PUT _ingest/pipeline/langdetect-analyzer-pipeline
{
  "description": "A pipeline to index data into language specific analyzers",
  "processors": [
    {
      "langdetect": {
        "field": "my_field",
        "target_field": "lang"
      }
    },
    {
      "script": {
        "source": "ctx.language = [:];ctx.language[ctx.lang] = ctx.remove('my_field')"
      }
    }
  ]
}

PUT documents
{
  "mappings": {
    "doc" : {
      "properties" : {
        "language": {
          "properties": {
            "de" : {
              "type": "text",
              "analyzer": "german"
            },
            "en" : {
              "type": "text",
              "analyzer": "english"
            }
          }
        }
      }
    }
  }
}

PUT /my-index/doc/1?pipeline=langdetect-analyzer-pipeline
{
  "my_field" : "This is an english text"
}

PUT /my-index/doc/2?pipeline=langdetect-analyzer-pipeline
{
  "my_field" : "Das hier ist ein deutscher Text."
}

GET my-index/doc/1

GET my-index/doc/2
```

## Configuration

| Parameter | Use |
| --- | --- |
| field          | Field name of where to read the content from |
| target_field   | Field name to write the language to |
| max_length     | Max length of of characters to read, defaults to 10kb, requires a byte size value, like 1mb |
| ignore_missing | Ignore missing source field. Not throwing exception in that case. Expects for boolean value, defaults to false. |

## Setup

In order to install this plugin, you need to create a zip distribution first by running

```bash
gradle clean check
```

This will produce a zip file in `build/distributions`.

After building the zip file, you can install it like this

```bash
bin/plugin install file:///path/to/ingest-langdetect/build/distribution/ingest-langdetect-0.0.1-SNAPSHOT.zip
```

## Side notes

In order to cope with the security manager, a special factory is used to load the languages from the classpath.
You can check out the `SecureDetectorFactory` class. This implementation also does not use jsonic to prevent the use of reflection when loading the languages.
