# Hubstaff to Deel Time Submission

Automatically submit worked hours from Hubstaff to Deel based on time tracking data.

## Features

- Fetches time tracking data from Hubstaff API
- Submits worked hours to Deel
- Prevents duplicate submissions
- Supports current Deel Pay Cycle only
- Debug mode for testing without actual submissions
- Cross-platform compatible (macOS, Linux)

## Prerequisites

- Python 3.8 or higher
- Hubstaff account with API access
- Deel account with API access
- pip (Python package manager)

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/alex-rn/submit-work-hours-hubstaff-deel.git
   cd submit-work-hours-hubstaff-deel
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On macOS/Linux
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create `.env` file:
   ```bash
   cp .env.example .env
   ```

5. Configure your environment variables in `.env`:

### Hubstaff Setup
1. Go to [Hubstaff Developer Portal](https://developer.hubstaff.com/)
2. Create a new application
3. Get your App Token and Auth Token
4. Find your Organization ID from Hubstaff dashboard

### Deel Setup
1. Contact Deel support to get API access
2. Get your API Key and Secret
3. Find your Contract ID from Deel dashboard

## Usage

1. Make sure your virtual environment is activated:
   ```bash
   source venv/bin/activate  # On macOS/Linux
   ```

2. Run the script:
   ```bash
   python submit_hours.py
   ```

### Debug Mode
Set `DEBUG_MODE=True` in `.env` to run the script without actual submissions. This will print the actions that would be taken without making actual API calls.

## Safety Features

- Duplicate submission prevention
- Multiple validation checks before submission
- Debug mode for testing
- Detailed logging

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

MIT License - see LICENSE file for details
