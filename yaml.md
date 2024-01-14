___
# YAML
Links: [[Python]]
Status: #🌞 
Tags: [[Deep Learning]]

<!--- Created on: 2023.12.04, 09:33 --->

- human-readable data serialization format often used for configuration files
- fosters reproducibility by enabling easy sharing and replication of AI model setups
___

# Anchors
- `&` denotes an anchor, which allows you to mark a location
- `*` references it elsewhere
```yaml
COMMON: &COMMON     # & denotes an anchor
  key1: value1
  key2: value2

other_key: *COMMON  # * denotes a reference
  # implicitely contains key1 and key2
```