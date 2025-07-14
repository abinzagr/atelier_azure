# Microsoft DataOps Copilot Artifacts

This directory contains GitHub Copilot artifacts designed to help engineers implement DataOps best practices in Microsoft data platform projects. These artifacts leverage the patterns and examples from the samples in this repository to provide comprehensive guidance and accelerate development.

## Available Platforms

### Microsoft Fabric
DataOps artifacts for Microsoft Fabric projects implementing medallion architecture, CI/CD, and modern data engineering practices.

### Azure Databricks
DataOps artifacts for Azure Databricks projects with Unity Catalog, medallion architecture, comprehensive CI/CD pipelines, and enterprise data lakehouse patterns based on the proven parking sensors implementation.

## Available Artifacts

### Microsoft Fabric (`/fabric/`)

| Artifact | Purpose | Type |
|----------|---------|------|
| `fabric-dataops-instructions.md` | Core DataOps principles and implementation guidance | Instructions |
| `fabric-project-setup.md` | Interactive project setup assistant | Prompt |
| `fabric-cicd-instructions.md` | CI/CD pipeline implementation guide | Instructions |
| `fabric-medallion-prompt.md` | Medallion architecture implementation helper | Prompt |
| `fabric-infrastructure-prompt.md` | Infrastructure as Code template generator | Prompt |
| `fabric-testing-instructions.md` | Testing strategy and implementation guide | Instructions |
| `fabric-troubleshooting-prompt.md` | Troubleshooting assistant for common issues | Prompt |
| `fabric-best-practices-checklist.md` | Comprehensive best practices checklist | Checklist |

### Azure Databricks (`/databricks/`)

| Artifact | Purpose | Type |
|----------|---------|------|
| `databricks-dataops-instructions.md` | Core DataOps principles for Databricks with Unity Catalog | Instructions |
| `databricks-project-setup.md` | Interactive Databricks project setup assistant | Prompt |
| `databricks-cicd-instructions.md` | CI/CD pipeline implementation for Databricks | Instructions |
| `databricks-medallion-prompt.md` | Medallion architecture with Unity Catalog implementation | Prompt |
| `databricks-infrastructure-prompt.md` | Infrastructure as Code for Databricks and Unity Catalog | Prompt |
| `databricks-testing-instructions.md` | Testing strategy for Databricks projects | Instructions |
| `databricks-troubleshooting-prompt.md` | Troubleshooting assistant for Databricks issues | Prompt |
| `databricks-best-practices-checklist.md` | Comprehensive Databricks best practices checklist | Checklist |

## How to Use These Artifacts in Your Project

### Step 1: Choose Your Platform and Copy Artifacts

1. **Create a `.copilot` folder** in the root of your data project:
   ```bash
   mkdir .copilot
   ```

2. **Copy the relevant platform artifacts** from this repository to your project:

   **For Microsoft Fabric projects:**
   ```bash
   # Copy all Fabric artifacts
   cp -r /path/to/modern-data-warehouse-dataops/.copilot/fabric/* .copilot/
   
   # Or copy specific Fabric artifacts you need
   cp /path/to/modern-data-warehouse-dataops/.copilot/fabric/fabric-project-setup.md .copilot/
   cp /path/to/modern-data-warehouse-dataops/.copilot/fabric/fabric-dataops-instructions.md .copilot/
   ```

   **For Azure Databricks projects:**
   ```bash
   # Copy all Databricks artifacts
   cp -r /path/to/modern-data-warehouse-dataops/.copilot/databricks/* .copilot/
   
   # Or copy specific Databricks artifacts you need
   cp /path/to/modern-data-warehouse-dataops/.copilot/databricks/databricks-project-setup.md .copilot/
   cp /path/to/modern-data-warehouse-dataops/.copilot/databricks/databricks-dataops-instructions.md .copilot/
   ```

3. **Customize the artifacts** for your specific project needs by editing the files and updating:
   - Project-specific naming conventions
   - Your organization's specific requirements
   - Environment configurations
   - Security and compliance requirements

### Step 2: Configure GitHub Copilot to Use the Artifacts

#### Option A: Using Copilot Chat (Recommended)

1. **Open Copilot Chat** in VS Code (`Ctrl+Shift+I` or `Cmd+Shift+I`)

2. **Reference the instruction files** in your prompts:

   **For Fabric projects:**
   ```
   @workspace Using the guidance in .copilot/fabric-dataops-instructions.md, help me set up Infrastructure as Code for my Fabric project
   ```

   **For Databricks projects:**
   ```
   @workspace Using the guidance in .copilot/databricks-dataops-instructions.md, help me set up Infrastructure as Code for my Databricks project
   ```

3. **Use the prompt files directly**:

   **For Fabric:**
   ```
   @workspace Follow the instructions in .copilot/fabric-project-setup.md to help me create a new Fabric project
   ```

   **For Databricks:**
   ```
   @workspace Follow the instructions in .copilot/databricks-project-setup.md to help me create a new Databricks project
   ```

#### Option B: Manual Reference

1. **Open the relevant artifact** in VS Code
2. **Copy the prompt or instructions** to Copilot Chat
3. **Customize the prompt** with your specific project details

### Step 3: Leverage Platform-Specific Artifacts

#### **Microsoft Fabric Workflows**

**For New Fabric Project Setup:**
```
@workspace I'm starting a new Microsoft Fabric project. Follow the guidance in .copilot/fabric-project-setup.md to help me set up the project structure, infrastructure, and CI/CD pipelines.
```

**For Fabric Infrastructure as Code:**
```
@workspace Using .copilot/fabric-infrastructure-prompt.md, generate Terraform configurations for my Fabric project with these requirements: [describe your specific needs]
```

**For Fabric CI/CD Implementation:**
```
@workspace Help me implement CI/CD pipelines following the patterns in .copilot/fabric-cicd-instructions.md for my Azure DevOps project
```

**For Fabric Medallion Architecture:**
```
@workspace Using .copilot/fabric-medallion-prompt.md, help me implement a medallion architecture for my data pipeline that processes [describe your data]
```

#### **Azure Databricks Workflows**

**For New Databricks Project Setup:**
```
@workspace I'm starting a new Azure Databricks project. Follow the guidance in .copilot/databricks-project-setup.md to help me set up the project structure, infrastructure, and CI/CD pipelines.
```

**For Databricks Infrastructure as Code:**
```
@workspace Using .copilot/databricks-infrastructure-prompt.md, generate Bicep/Terraform configurations for my Databricks lakehouse with Unity Catalog
```

**For Databricks CI/CD Implementation:**
```
@workspace Help me implement CI/CD pipelines following the patterns in .copilot/databricks-cicd-instructions.md for my Azure DevOps project
```

**For Databricks Medallion Architecture:**
```
@workspace Using .copilot/databricks-medallion-prompt.md, help me implement a medallion architecture with Unity Catalog for processing [describe your data]
```

#### **Testing Strategy (Both Platforms)**
```
@workspace Following .copilot/[platform]-testing-instructions.md, help me implement a comprehensive testing strategy for my [platform] project
```

#### **Troubleshooting (Both Platforms)**
```
@workspace I'm experiencing [describe issue]. Use .copilot/[platform]-troubleshooting-prompt.md to help me diagnose and resolve this problem
```

#### **Best Practices Review (Both Platforms)**
```
@workspace Review my [platform] project against the checklist in .copilot/[platform]-best-practices-checklist.md and identify areas for improvement
```

## Pro Tips for Maximum Effectiveness

### 1. **Combine Artifacts**
Use multiple artifacts together for comprehensive guidance:
```
@workspace Using both .copilot/fabric-dataops-instructions.md and .copilot/fabric-testing-instructions.md, help me implement a testing strategy that aligns with DataOps best practices
```

### 2. **Iterative Development**
Use the artifacts iteratively as you build your project:
- Start with `fabric-project-setup.md` for initial structure
- Use `fabric-infrastructure-prompt.md` for IaC implementation
- Apply `fabric-cicd-instructions.md` for pipeline setup
- Validate with `fabric-best-practices-checklist.md`

### 3. **Customize for Your Organization**
Modify the artifacts to include:
- Your organization's naming conventions
- Specific security requirements
- Compliance standards
- Preferred tools and technologies

### 4. **Keep Artifacts Updated**
- Regularly update the artifacts based on lessons learned
- Incorporate new Fabric features and capabilities
- Share improvements with your team

## Common Use Cases

### Starting a New Data Platform Project

**For Fabric:**
```bash
# 1. Copy Fabric artifacts to your project
cp -r /path/to/modern-data-warehouse-dataops/.copilot/fabric .copilot/

# 2. In Copilot Chat:
@workspace Follow .copilot/fabric-project-setup.md to create a new Fabric DataOps project for processing customer analytics data
```

**For Databricks:**
```bash
# 1. Copy Databricks artifacts to your project
cp -r /path/to/modern-data-warehouse-dataops/.copilot/databricks .copilot/

# 2. In Copilot Chat:
@workspace Follow .copilot/databricks-project-setup.md to create a new Databricks DataOps project with Unity Catalog for processing real-time sensor data
```

### Implementing CI/CD for Existing Project

**For Fabric:**
```bash
# In Copilot Chat:
@workspace Using .copilot/fabric-cicd-instructions.md, help me add CI/CD pipelines to my existing Fabric project that currently has manual deployments
```

**For Databricks:**
```bash
# In Copilot Chat:
@workspace Using .copilot/databricks-cicd-instructions.md, help me add CI/CD pipelines to my existing Databricks project with notebook testing and Unity Catalog deployment
```

### Troubleshooting Platform-Specific Issues

**For Fabric:**
```bash
# In Copilot Chat:
@workspace My Fabric deployment is failing with authentication errors. Use .copilot/fabric-troubleshooting-prompt.md to help me diagnose the issue
```

**For Databricks:**
```bash
# In Copilot Chat:
@workspace My Databricks cluster is experiencing performance issues with Spark jobs. Use .copilot/databricks-troubleshooting-prompt.md to help me optimize performance
```

### Architecture Review and Optimization

**Cross-Platform:**
```bash
# In Copilot Chat:
@workspace Review my current data architecture against .copilot/databricks-medallion-prompt.md and .copilot/databricks-best-practices-checklist.md to identify improvements for migrating from Fabric to Databricks
```

## Learning Resources

To maximize the value of these artifacts, familiarize yourself with the reference implementations in this repository:

### **Microsoft Fabric Samples**
- **`/fabric/fabric_dataops_sample/`** - Complete end-to-end DataOps implementation
- **`/fabric/fabric_ci_cd/`** - CI/CD pipeline patterns and configurations
- **`/fabric/fabric_cicd_gitlab/`** - GitLab-specific CI/CD examples
- **`/fabric/feature_engineering_on_fabric/`** - Advanced data engineering patterns

### **Azure Databricks Samples**
- **`/databricks/parking_sensors/`** - Complete end-to-end DataOps implementation with medallion architecture and Unity Catalog
- **`/databricks/parking_sensors/infrastructure/`** - Bicep infrastructure patterns for Databricks and Unity Catalog
- **`/databricks/parking_sensors/devops/`** - Azure DevOps CI/CD pipeline configurations with multi-stage deployment
- **`/databricks/parking_sensors/src/`** - Python package structure and testing patterns for data transformations
- **`/databricks/parking_sensors/tests/`** - Integration testing framework for data pipelines and Great Expectations validation
- **`/databricks/parking_sensors/databricks/`** - Notebook organization and Unity Catalog configuration patterns

## Contributing

If you develop additional artifacts or improvements:

1. Test them in real Fabric projects
2. Document the use cases and benefits
3. Follow the same naming and structure conventions
4. Submit pull requests to share with the community

## Support

For questions about using these artifacts:
- Reference the original sample projects in `/fabric/` and `/databricks/`
- Check the troubleshooting guide in `fabric-troubleshooting-prompt.md` and `databricks-troubleshooting-prompt.md`
- Review the documentation links in the instruction files

---

**Happy Engineering!**

These artifacts are designed to make GitHub Copilot more effective at helping you implement robust DataOps practices in your Microsoft data platform projects. Whether you're building on Fabric or Databricks, use these as starting points and customize them to fit your specific needs and organizational requirements.
