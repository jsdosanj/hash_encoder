# hash_encoder
Python hash_encoder using SHA_256 algorithm

import hashlib

def hash_encode(string):
    # Create a new SHA-256 hash object
    hash_object = hashlib.sha256()
    
    # Convert the string to bytes and update the hash object
    hash_object.update(string.encode('utf-8'))
    
    # Get the hashed representation
    hashed_string = hash_object.hexdigest()
    
    # Return the hashed string
    return hashed_string

# Example usage
string_to_encode = "Hello, World!"
hashed_string = hash_encode(string_to_encode)
print("Hashed String:", hashed_string)
