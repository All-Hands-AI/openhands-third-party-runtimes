# OpenHands Third-Party Runtimes

This repository contains the third-party runtime implementations that were removed from the main OpenHands repository. These runtimes provide integration with external platforms for code execution and development environments.

**Note:** These are NOT officially supported by the OpenHands team.

## Included Runtimes

### 1. E2B Runtime
- **Location**: `openhands/runtime/impl/e2b/`
- **Description**: Integration with E2B sandboxed environments for secure code execution
- **Files**:
  - `e2b_runtime.py` - Main runtime implementation
  - `filestore.py` - File management utilities
  - `sandbox.py` - Sandbox management
  - `README.md` - E2B-specific documentation
- **Container**: `containers/e2b-sandbox/` - Docker configuration for E2B environments
- **Documentation**: `docs/usage/runtimes/e2b.mdx`

### 2. Modal Runtime
- **Location**: `openhands/runtime/impl/modal/`
- **Description**: Integration with Modal for serverless code execution
- **Files**:
  - `modal_runtime.py` - Main runtime implementation
- **Documentation**: `docs/usage/runtimes/modal.mdx`

### 3. Runloop Runtime
- **Location**: `openhands/runtime/impl/runloop/`
- **Description**: Integration with Runloop for managed development environments
- **Files**:
  - `runloop_runtime.py` - Main runtime implementation
  - `README.md` - Runloop-specific documentation
- **Documentation**: `docs/usage/runtimes/runloop.mdx`

### 4. Daytona Runtime
- **Location**: `openhands/runtime/impl/daytona/`
- **Description**: Integration with Daytona for development workspace management
- **Files**:
  - `daytona_runtime.py` - Main runtime implementation
  - `README.md` - Daytona-specific documentation
- **Documentation**: `docs/usage/runtimes/daytona.mdx`

## Why Were These Moved?

These third-party runtime implementations were moved out of the main OpenHands repository to:

1. **Reduce maintenance burden** - Focus core development on the primary local and remote runtimes
2. **Simplify dependencies** - Remove external service dependencies from the main codebase
3. **Improve modularity** - Allow third-party integrations to evolve independently
4. **Streamline CI/CD** - Reduce test complexity and build times for the main repository

## Usage

To use these runtimes with OpenHands, you would need to:

1. Copy the relevant runtime implementation back into your OpenHands installation
2. Install any required dependencies for the specific runtime by modifying `pyproject.toml`
3. Add the runtime to `openhands/runtime/__init__.py`
4. Configure the runtime according to its documentation
5. Set up authentication with the respective third-party service

## Contributing

If you maintain or use any of these runtimes and would like to contribute improvements:

1. Fork this repository
2. Make your changes
3. Submit a pull request with a clear description of the changes
4. Ensure any documentation is updated accordingly

## Support

For support with these third-party runtimes:

1. Check the individual README files in each runtime directory
2. Refer to the documentation in the `docs/usage/runtimes/` directory
3. Contact the respective third-party service providers for platform-specific issues
4. Open an issue in this repository for integration-related problems

## License

These runtime implementations maintain the same license as the original OpenHands project.
