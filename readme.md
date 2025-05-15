# IRCTC Captcha Solver

This project automates the process of solving IRCTC captchas Python, and Playwright. It includes a Python-based captcha solver.

---

## Prerequisites

Before running the project, ensure the following are installed on your system:

1. **Python and pip**: Install Python from [here](https://www.python.org/).

---

## Installation Steps

# IRCTC Captcha Solver Setup Guide

## 1. Install Python and pip
Ensure Python is installed on your system. If `pip` is missing, install it using:

```bash
sudo apt-get update && sudo apt-get install python3-pip python3-venv -y
```

## 2. Create and Activate a Virtual Environment
Navigate to the project folder and create a virtual environment named `venv`:

```bash
python3 -m venv venv
```

### Activate the Virtual Environment:
- **Linux/macOS:**
  ```bash
  source venv/bin/activate
  ```
- **Windows (Command Prompt):**
  ```cmd
  venv\Scripts\activate
  ```

## 3. Install Python Dependencies
Once the virtual environment is activated, install the required dependencies:

```bash
pip install -r irctc-captcha-solver/requirements.txt
```

## 4. Verify the Captcha Solver
Run the Python captcha solver server to ensure it works correctly:

```bash
  python app-server.py --host 0.0.0.0 --port 5000
```

### Test the Server
Use `curl` to verify the API is running:

```bash
curl -X POST "http://localhost:5000/extract-text" \
-H "Content-Type: application/json" \
-d '{
     "image": "data:image/jpg;base64,iVBORw0KGgoAAAANSUhEUgAAAMsAAAAyCAYAAADyZi/iAAAFMElEQVR42u1cb0SdURhP0ockciVJ4tqH7MNEsg8zE8lkMpFMkoyZSdKXmZlMRjJJEpNMMpHMZCbmStKHkUkyM2YmMxMzmUzi3XntbE7PnvOv9977vtXvx3HvPed5fufc9z2/95znnHNvQQEAAAAAAAAAAAAAAAAAAAAAZBdBEBSK1C3SgkifRdoX6TBQgKsEQChBUCfS+8ACC4cJtZ7tSfu0w6edPt9B5s2T7PAhkj4G9znpq+KZwf4DsW3yrO8V8V/z9L9C/D9CKEFQKkeSIIdieejZpuEEiSUl0rcoHU/yrBGOkDNlsH9K7B94zhIOiH84Syjy4HhA/GchliC4Ty7KJ5GaRSqO0tEIdjy5dpIiFpnfwTSjz4O3n/Fvt/h0EvvXHvVd1ly6Vg+OZeLbCbEEwUqU4d4glh/kc7MjTwvx24tbLLJsgWlXjeOU8ifxXXTwqyQ+4UhR6Pg97il+v5T3wxFGpkqI5f8bWZglsUySzwuOPIvEbyIhYqkQadf3aR/aEJ/vrh3vuHGLsHupxkXK+4yjfzOp9z0i+z8X5jAXHU2gnnkypiwcKdoegYYkiEWWdzHfs9fAd5ux7/JozwzxHXIcFdTRpNZ3dArrIfXOQCm5D443SfaAhWOA2G85duK8iEXaLDEjRRVjV8NMIZc820NjpYyDzyXFfpu5D00OHBmf+OpMCSTqSphBLGznN3BsEfv+BIqlSgrEKAJm+vWDE5WlPRXM6Fxk8bmr2E/LvEnXVbWQnxndUxBL7sVSzgSKDRr/Rt20LUlikXa9zCW6oZT3+EzXLG16R3haLPbqyNch89qVvGWL/1VS3zamXnkQi8ynm3qTGv8pYjfvEUvkVSyakWNXxlzcyLMcoU1PCNewJV5RNz4rlIeWU9wiyh6R+qYQrOSpozErK3t0KiGH/p+6peaEioWLSeaZmCa0qY7QpnbCt2KwvahbwSIj1GUDxyrilZjEIsvoCYEeUt5j2sRMolik/S2HQflOxPtT7hq3iPxBxe4pKZtWyu55xCvlUEl+xTJsejoyqy9DUcSSLTh+74yBYiVL92jLZSde5D/X7biTEwEvNP6tPgsyEEtuxFLLdKS0LEvbDl4mXCzcDn0g89JZukd0g3dEY6fGK1WkTD0RsK/xH3GJLyGW3G/oZbhA1TbqJF0ssn7u7Fd/Fu9Ru+0gJ9m8/ajhUU8ENDLl66Se61BIPGJh4xLm0GRXVLHEcS2y1QYNd5ntBDER7KyGZ1a3QRwenCXxSvi+DAqJRyxFzOHKUWbjrghiYfnpaYhrpHzRdkKYxC2LpKyN8L+FOmLsaMzcm668TBxTiGdBLPRA6SgpV+Omag1HtS5uEZ/HCP841BGvWOotYUI9xOIct6xrrusnC89n7jSFeL9B+Nugjpg7GrMM+hebEaZ4Z0EspcyoXCzL+lx/0SjK5+gekHgtYeKVEqgjfrEMaMTSD7FY69jg4hYSr3RZOLrpb4zCVS/C+wbKSIZYuMOVB6aVF4jlXx3jpJoxmb/n+ucgZF/ruyYeegxlJEAs0nbe9V9OIJYjdfw3Aoh0wfe/DoTdF8XnvG2lDUhQR4vKfYbEwsUW6u9X5hx51IfVoC4WAiCWEysWTdyyrzugauDo1fgfWWUDIJaTLpbHhqX3c44cdQaOEagCYjktYmnTdPKvnjy7Gh7EKxDLqRFLMXPywbpI4rDIwp45AyCWEysWWdc609FvenJwf9O0CkUAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAACcYvwGObCH1snSinwAAAAASUVORK5CYII="
    }'
```

### Expected Response:
```json
{"error":"No base64 image string provided"}
```

## Troubleshooting

- **Captcha Solver Issues**: Ensure the Python server is running and accessible at `http://localhost:5001`.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

