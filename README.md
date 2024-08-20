CloudUploader CLI:

	• Create a bash-based CLI tool that allows users to quickly upload files to a specified cloud storage solution, providing a seamless upload experience similar to popular storage services.
	• Your tool should be able to upload a file: clouduploader /path/to/file.txt

	• Steps:​
	
		a. Create a GitHub Repo:
		
			§ Set up a repository for your project.
			§ Use branches and commit your code often.
			§ Utilize git commands (git init, git add, git commit, git branch, git push, etc.).
		
		b. Setup & Authentication:
		
			§ Choose a cloud provider (e.g., AWS S3, Google Cloud Storage, Azure Blob Storage).
			§ Set up authentication (e.g., az login for Azure).
			§ Use secure methods for handling credentials.
			§ Avoid hardcoding credentials directly into the script.
			§ Store credentials in environment variables or configuration files with restricted access.
			§ Utilize cloud provider's secure authentication methods (e.g., IAM roles for AWS, service principals for Azure).
		
		c. CLI Argument Parsing:
		
			§ Use bash's built-in $1, $2, etc., to parse command-line arguments.
			§ $1 could be the filename or path.
			§ Optionally, allow additional arguments like target cloud directory, storage class, or any other cloud-specific attributes.
			§ Validate and handle different types of input.\
			§ Check if the provided file path is valid and accessible.
			§ Ensure that additional arguments meet expected formats and values.
			§ Provide meaningful error messages for incorrect or missing inputs
		
		d. File Check:
		
			§ Before uploading, check if the file exists using [ -f $FILENAME ].
			§ Provide feedback if the file is not found.
		
		e. File Upload:
		
			§ Use the cloud provider's CLI to upload the file.
			§ Implement error handling to manage potential issues during upload.
		
		f. Upload Feedback:
		
			§ On successful upload, provide a success message.
			§ If there's an error, capture the error message and display it to the user.
		
		g. Advanced Features (Optional but recommended):
		
			§ Add a progress bar or percentage upload completion using tools like pv.
			§ Provide an option to generate and display a shareable link post-upload.
			§ Enable file synchronization -- if the file already exists in the cloud, prompt the user to overwrite, skip, or rename.
			§ Integrate encryption for added security before the upload.
		
		h. Documentation:
		
			§ Write a README.md file explaining how to set up, use, and troubleshoot the tool.
			§ Include a brief overview, prerequisites, usage examples, and common issues.
		
		i. Distribution:
		
			§ Package the script for easy distribution and installation. You can even provide a simple installation script or instructions to add it to the user's $PATH.
