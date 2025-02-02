<p align="center" width="100%">
    <img width="33%" src="./icon.png" alt="Ansible Logo" />
</p>


# Ansible Playbook Runner for Alfred

This workflow filters a list of ansible playbooks, and then runs the selected playbook - outputting to either large type, a default text editor or copies the output to clipboard.

## Playbook Search

This workflow scans your Ansible directory (and all subdirectories) for YAML files containing valid playbooks and outputs them to an Alfred list

## Execution with Feedback

When you run a playbook, you get an initial notification indicating that the playbook is starting. When it's finished, you’ll see a success or error notification. Note that the actual ansible output isn't parsed, an error is only thrown if the playbook couldn't run for some reason.

## Output Options:

### Choose how you want to view the playbook output:

- Large Type: Display the results in Alfred’s Large Type view.
- Editor: Open the results in your default text editor.
- Clipboard: Copy the output directly to your clipboard.

## Installation

### Download or Clone the Workflow

Get the latest version of the workflow files and open them with Alfred.

### Add to Alfred
Drag and drop the workflow file into Alfred or use the import option in Alfred’s Workflows preferences.

## Configuration

Before using the workflow, you need to configure two key settings in Alfred’s built-in configuration editor:

```bash
ANSIBLE_PATH
OUTPUT
```
Open the workflow’s configuration editor in Alfred and fill in these fields to suit your preferences.

## Usage

### Invoke the Workflow
Use the designated keyword (set to 'ans') to activate the workflow in Alfred.

### Browse Your Playbooks

The workflow will display a list of all Ansible playbooks found in your configured directory. Each item shows the playbook name (prefixed with “Run:”) along with its relative location.

### Run a Playbook

Select a playbook from the list. An initial notification should appear, stating, "Running playbook: [Playbook Name]". The playbook is executed, and when it completes, you’ll receive a success or error notification.

### View the Output
Based on your OUTPUT_MODE setting, the output will be displayed in Large Type, opened in your text editor, or copied to your clipboard.

## Customization

### Modifying the Workflow
If you’d like to adjust the behavior further (for example, parsing more details from your playbook output or tweaking notifications), feel free to modify the provided scripts.

## Error Handling:
The workflow checks if any playbooks are found in your specified directory and provides a message if none are detected, doesn't output if there was a problem with the actual ansible playbook, just if it had issues running it.

## Troubleshooting

### No playbooks Found
Double-check that your ANSIBLE_PATH is correct and that your playbook files include a tasks: section.

### Incorrect Output
Verify your OUTPUT_MODE setting in the configuration editor to ensure it matches your preferred output method.

### Notifications Not Appearing
Ensure that your system notifications are enabled for Alfred and that you haven’t muted notification alerts.

## License

Feel free to distribute and modify this workflow as needed.
