# 🌊 Lafkn 🌊

A modern serverless framework scaffolding tool for cdktf projects.

## Installation

```bash
npm create lafkn@latest
```

Or use directly with npx:

```bash
npx create-lafkn
```

## Usage

Simply run the command and follow the interactive prompts:

```bash
npm create lafkn
```

The CLI will guide you through:

1. **Project name**: Choose a name for your project
2. **Directory selection**: If your current directory matches the project name, you'll be asked if you want to use it
3. **Service selection**: Choose which AWS services to include in your project
4. **Dependency installation**: Optionally install dependencies with your preferred package manager

## Available Services

Lafkn supports the following AWS services out of the box:

- **API Gateway** - RESTful API endpoints
- **Authentication** - User authentication and authorization
- **S3 Bucket** - Object storage
- **DynamoDB** - NoSQL database
- **EventBridge** - Event bus for event-driven architecture
- **SQS Queue** - Message queuing service
- **EventBridge Schedule** - Scheduled task execution
- **Step Functions** - State machine workflows

## Project Structure

After scaffolding, your project will have the following structure:

```
my-lafkn-app/
├── src/
│   └── index.ts
├── package.json
├── tsconfig.json
└── cdktf.json
```

The `package.json` will include only the services you selected during setup.

## Development

Once your project is created:

```bash
cd my-lafkn-app
npm install  # if you didn't install during setup
npm run build
npm run cdktf:synth
```

## Available Scripts

- `npm run build` - Compile TypeScript to JavaScript
- `npm run cdktf:deploy` - Build and deploy your infrastructure
- `npm run cdktf:destroy` - Destroy your infrastructure
- `npm run cdktf:synth` - Synthesize CloudFormation templates
- `npm run clean` - Clean build artifacts

## Support

For issues and questions, please open an issue on GitHub.

---

Built with ❤️ using [Eta](https://eta.js.org/) templates and [Inquirer](https://github.com/SBoudrias/Inquirer.js)
