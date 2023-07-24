This is forked from the open-source [AWS graph explorer](https://github.com/aws/graph-explorer). This resolves a niche use case that I faced.
Please see the official documentation provided by AWS graph explorer to understand more.

# What this fork solves?
I had a use case where I needed to use AWS graph explorer to present the graph database by integrating it into a web application. The user using the web application would need to seamlessly connect to the AWS Neptune database and be able to use all features of the web application.

The changes I made are to meet those requirements.

# Changes from the actual opensource repository
- Remove connection-related components (for creating, editing and removing connections to databases) so the user could directly get nodes from the Amazon Neptune database.
- Use a custom authorization token to enable authentication of the user through the web application.
- Use configuration variables to connect with the target database by default.

# Additional steps for setting up
- Copy the `.env.example` file
- Rename the example file as `.env`
- Provide the necessary connection variables in the env file
- Save auth token as `custom-auth-token` in localStorage

## License
This project is licensed under the Apache-2.0 License.
