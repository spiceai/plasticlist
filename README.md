# plasticlist.org with Spice

This repository contains a Spice application for [plasticlist.org](https://plasticlist.org), enabling super-fast SQL queries, vector searches, and LLM-based chat interactions over the dataset.

## Prerequisites

1. Install the Spice CLI if you haven't already. Refer to the [Getting Started](https://docs.spiceai.org/getting-started) guide.
2. A valid OpenAI API Key.

## Getting Started

1. Clone this repository and navigate to the project directory:

   ```bash
   git clone https://github.com/spiceai/plasticlist.git
   cd plasticlist
   ```

2. Set up your `.env.local` file:

   ```bash
   cp .env .env.local
   # Edit the .env.local file to include your API key and other required configurations.
   ```

3. Run Spice. Ensure the working directory is `plasticlist`:

   ```bash
   spice run
   ```

   This will set up the datasets and the configured LLM model for queries and searches.

## How to Use

### SQL Query with `spice sql`

Use the `spice sql` command to run SQL queries against the datasets. For example, to query the `samples` dataset:

```bash
spice sql
```

```sql
> SELECT * FROM samples WHERE category = 'plastic' LIMIT 10;
```

This retrieves up to 10 records where the category is "plastic."

### Search with `spice search`

Perform vector-based searches using the `spice search` command. Example:

```bash
spice search
```

```text
search> Whole Foods
```

This finds results related to ocean pollution prevention from the dataset.

### LLM Chat with `spice chat`

Engage with the dataset through an LLM using the `spice chat` command. Example:

```bash
spice chat
```

```text
chat> What are the most common types of plastic in the dataset?
```

The LLM will generate a response based on the dataset and the GPT model configured in the `spicepod.yml` file.

## Additional Notes

- Modify the `spicepod.yml` file to add new datasets or models.
- For detailed documentation on each command, refer to the [Spice CLI documentation](https://docs.spiceai.org/cli).

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
