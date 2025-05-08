# jira-cheat-sheet
Jira Cheat Sheet with the most needed stuff..










# Security

## API Tokens
- https://id.atlassian.com/manage-profile/security/api-tokens







<br><br>
<br><br>

___


<br><br>
<br><br>



# MCP

## Unofficial
- https://github.com/sooperset/mcp-atlassian

```shell
docker pull ghcr.io/sooperset/mcp-atlassian:latest
```

```json
{
  "mcpServers": {
    "mcp-atlassian": {
      "command": "docker",
      "args": [
        "run",
        "-i",
        "--rm",
        "-e", "CONFLUENCE_URL",
        "-e", "CONFLUENCE_USERNAME",
        "-e", "CONFLUENCE_API_TOKEN",
        "-e", "JIRA_URL",
        "-e", "JIRA_USERNAME",
        "-e", "JIRA_API_TOKEN",
        "ghcr.io/sooperset/mcp-atlassian:latest"
      ],
      "env": {
        "CONFLUENCE_URL": "https://your-company.atlassian.net/wiki",
        "CONFLUENCE_USERNAME": "your.email@company.com",
        "CONFLUENCE_API_TOKEN": "your_confluence_api_token", // https://id.atlassian.com/manage-profile/security/api-tokens
        "JIRA_URL": "https://your-company.atlassian.net",
        "JIRA_USERNAME": "your.email@company.com",
        "JIRA_API_TOKEN": "your_jira_api_token" // https://id.atlassian.com/manage-profile/security/api-tokens
      }
    }
  }
}
```
- https://id.atlassian.com/manage-profile/security/api-tokens




<br><br>
<br><br>

___


<br><br>
<br><br>



# Show all Tickets which are DONE
Um alle Ihre Tickets anzuzeigen, die den Status "Done" haben, müssen Sie eine Jira-Suche durchführen und die entsprechenden Filter anwenden. Hier sind die Schritte, um Ihre erledigten Tickets in Jira anzuzeigen:

Öffnen Sie Jira in Ihrem Webbrowser und melden Sie sich bei Ihrem Konto an.
Klicken Sie auf die Schaltfläche "Suche" in der oberen Menüleiste.
Im Dropdown-Menü "Erweiterte Suche" klicken Sie auf "Erweiterte Suche". Dadurch wird die Suchmaske geöffnet.
Geben Sie den folgenden Suchbegriff in das Feld "JQL-Abfrage" ein: assignee = currentUser() AND status = Done.
Diese Abfrage gibt alle Tickets zurück, die aktuell von Ihnen zugewiesen sind und den Status "Done" haben.
Klicken Sie auf die Schaltfläche "Suche" oder drücken Sie die Eingabetaste auf Ihrer Tastatur. Jira wird alle Tickets anzeigen, die den Suchkriterien entsprechen.
Sie können den Suchergebnissen einen Namen geben und diese als Filter speichern, um sie später leicht wieder zu finden.
Kopieren Sie die URL aus der Adressleiste Ihres Browsers und speichern Sie diese, um den Link später erneut aufrufen zu können.
Hier ist ein Beispiel-Link, der auf Ihre erledigten Tickets basierend auf den obigen Schritten zeigt:

https://[your-jira-url]/issues/?jql=assignee%20%3D%20currentUser()%20AND%20status%20%3D%20Done
Bitte ersetzen Sie [your-jira-url] durch den tatsächlichen URL Ihres Jira-Servers.
