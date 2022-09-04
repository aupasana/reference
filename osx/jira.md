# JIRA

For on-premise installations, use a PAT and a JQL filter to query JIRA issues. 
This will then run it through `jq` to extract the issues and pretty-print

```zsh
curl -s -H "Authorization: Bearer #{jira_pat}" "https://domain.atassian.com/rest/api/2/search?&jql=labels=#{ARGV[0]}" | jq '.issues[]' | jq -s '.'`
```

Use this ruby snippet to extract information from the tickets. This will look for a "EXEC_SUMMARY" line and extract it.

```ruby
# Deserialize the json string into a hash
data_hash = JSON.parse(jira_json)

data_hash.each do |j|
    # Get the fields we care about
    key = j['key']
    status = j['fields']['status']['statusCategory']['name']
    description = j['fields']['description']
    summary = j['fields']['summary']
    extract = ""

    # Everything on a line starting from EXEC_SUMMARY: to the end of the line is the exec summary. It's presence is optional
    m_desc = description.match(/EXEC_SUMMARY: (?<extract>.*)/)
    if m_desc 
        extract = m_desc[:extract].chop()
    end

    # Output it however we want
    puts "#{key} \t #{summary} (#{status})\r\n#{extract}"
    puts
end 
```

