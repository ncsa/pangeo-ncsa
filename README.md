# Pangeo Dask Scheduler Image

This repository contains a Docker image for running a Dask scheduler, specifically designed for use at NCSA. The image is based on Python 3.11 and is optimized for running as a Dask scheduler rather than in a Jupyter environment.

## Features

- Based on Python 3.11 slim image
- Runs as a non-root user for security
- Pre-configured as a Dask scheduler
- Easy to extend with additional dependencies via requirements.txt

## Usage

### Building the Image

```bash
docker build -t pangeo-dask-scheduler .
```

### Running the Scheduler

```bash
docker run -p 8786:8786 pangeo-dask-scheduler
```

The scheduler will be available on port 8786.

## Configuration

Add your required Python packages to `requirements.txt`. The image will automatically install these dependencies during the build process.

## License

This project is licensed under the BSD-3-Clause License - see the [LICENSE](LICENSE) file for details. 