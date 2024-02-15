## Devops Day 8

Creating a shell script project that integrates with the GitHub API can be a useful tool for automating various tasks related to managing repositories, issues, pull requests, and more. Below, I'll outline a basic example of a shell script project that interacts with the GitHub API. This project will focus on fetching repository information.

### Prerequisites:
1. **GitHub Personal Access Token**: Generate a personal access token with appropriate permissions (e.g., `repo` scope) from your GitHub account.
2. **cURL**: Ensure cURL is installed on your system. Most Unix-like systems come with cURL pre-installed.

### Project Structure:
```
github_api_integration/
│
├── get_repo_info.sh
├── .env
└── README.md
```

1. **`get_repo_info.sh`**: The main shell script that interacts with the GitHub API to fetch repository information.
2. **`.env`**: A file to store environment variables such as the GitHub personal access token.
3. **`README.md`**: Documentation about the project.

### `get_repo_info.sh`:
```bash
#!/bin/bash

# Load environment variables
source .env

# GitHub API URL
API_URL="https://api.github.com/repos"

# Function to fetch repository information
get_repo_info() {
    local owner=$1
    local repo=$2
    curl -s -H "Authorization: token $GITHUB_TOKEN" $API_URL/$owner/$repo
}

# Main function
main() {
    if [ $# -ne 2 ]; then
        echo "Usage: $0 <owner> <repo>"
        exit 1
    fi

    owner=$1
    repo=$2

    # Fetch repository information
    response=$(get_repo_info $owner $repo)

    # Output the response
    echo "$response"
}

# Execute main function with provided arguments
main "$@"
```

### `.env`:
```plaintext
GITHUB_TOKEN=YOUR_GITHUB_PERSONAL_ACCESS_TOKEN
```

Replace `YOUR_GITHUB_PERSONAL_ACCESS_TOKEN` with your actual GitHub personal access token.

### Usage:
1. Make sure you have execute permission for `get_repo_info.sh`: `chmod +x get_repo_info.sh`.
2. Run the script with the owner and repository name as arguments:
   ```bash
   ./get_repo_info.sh owner repo
   ```
