# NetworkSecurity

## Setup

### Prerequisites

- Python 3.10
- MongoDB
- Docker (optional)

### Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/yourusername/network-security-etl.git
    cd network-security-etl
    ```

2. Create and activate a virtual environment:

    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the dependencies:

    ```sh
    pip install -r requirements.txt
    ```

4. Set up environment variables:

    Create a [.env](http://_vscodecontentref_/8) file in the root directory and add your MongoDB URL:

    ```env
    MONGO_DB_URL=mongodb+srv://<username>:<password>@cluster0.mongodb.net/<dbname>?retryWrites=true&w=majority
    ```

## Usage

### Running the Application

To run the FastAPI application:

```sh
uvicorn app:app --reload