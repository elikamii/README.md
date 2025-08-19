# A simple Python script to write and read from a file

def create_and_read_file(filename="example.txt", content="This is the initial content."):
    """
    Creates a new file with the given content and then reads it back.
    """
    try:
        # Write content to the file
        with open(filename, 'w') as f:
            f.write(content)
        print(f"Successfully wrote to '{filename}'.")

        # Read the content back from the file
        with open(filename, 'r') as f:
            read_content = f.read()
            print(f"Content read from '{filename}':\n{read_content}")
            
    except IOError as e:
        print(f"An error occurred: {e}")

if __name__ == "__main__":
    create_and_read_file()
