# Object Serialization and Deserialization in C++

## Overview
This project demonstrates how to serialize and deserialize an object in C++. The example uses a class named `Serializable` that encapsulates a `name` and `age` attribute. The class provides methods to serialize the object to a binary file and deserialize it back into an object.

## Files Included
- `main.cpp`: The main C++ source file containing the implementation of the `Serializable` class and the main function.
- `data.bin`: The binary file used for serialization and deserialization (generated during execution).

## How It Works

1. **Serialization**:
    - The `serialize()` method writes the object's data to a binary file (`data.bin`).
    - The object is saved in its raw binary format using the `ofstream` stream.

2. **Deserialization**:
    - The `deserialize()` method reads the object's data from the binary file (`data.bin`).
    - The data is restored into a new `Serializable` object using the `ifstream` stream.

## How to Run the Project

1. **Compile the Code**:
    ```bash
    g++ -o serialize main.cpp
    ```

2. **Run the Executable**:
    ```bash
    ./serialize
    ```

3. **Expected Output**:
    ```
    Object serialized successfully.
    Object deserialized successfully.
    Deserialized Object:
    Name: Adesh
    Age: 20
    ```

## Notes
- **Binary File**: The binary file (`data.bin`) stores the serialized object and is essential for deserialization.
- **Safety Concerns**: The code uses raw binary I/O for simplicity, which can lead to issues with portability and versioning. For real-world applications, consider using more robust serialization methods like JSON, XML, or protocol buffers.

## Requirements
- C++11 or later.
- g++ compiler (for compilation).

## Author
- Adesh Ghadage

## License
This project is open-source and available under the MIT License.
