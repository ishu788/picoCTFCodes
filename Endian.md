## General Challenege 

solved by python script to get flag.



### Little Endian
    def text_to_little_endian(text):
        encoded_text = text.encode('utf-8')

        # Reverse the order of bytes for each character
        little_endian_bytes = b''.join(reversed([bytes([byte]) for byte in encoded_text]))

        return little_endian_bytes


### Big Endian


    def text_to_big_endian(text):
        
        encoded_text = text.encode('utf-8')

        # Convert each character's byte sequence to big endian representation
        big_endian_bytes = b''.join([bytes([byte]) for byte in encoded_text])

        return big_endian_bytes

# Example usage
text = "Hello, World!"
big_endian_representation = text_to_big_endian(text)
print("Big Endian Representation:", big_endian_representation.hex())



# Example usage
text = "Hello, World!"
little_endian_representation = text_to_little_endian(text)
print("Little Endian Representation:", little_endian_representation.hex())
