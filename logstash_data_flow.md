

# Logstash Data Flow for Security Logs

## Data Ingestion
- Logstash ingests security logs from various sources, such as syslog, files, or direct input streams.
- In our setup, we process security log data in a specific format.

## Processing
- Logstash uses filters (e.g., Grok, Mutate) to extract relevant fields like `description`, `hostname`, `source_ip`, and `severity`.
- The parsed data is structured into JSON format.

## Output
- The transformed security log data is stored in a JSON file (`logstash_output.json`).
- This JSON data can be further used for analysis or visualized using Kibana.

## Example Output
```json
{
  "description": "Virus Found",
  "hostname": "acmeincpc42",
  "source_ip": "10.58.194.142",
  "severity": "High"
}
