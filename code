#include <stdio.h>
#include <string.h>
#include <stdlib.h>

// Maximum size of the header
#define MAX_HEADER_SIZE 64
#define MAX_MESSAGE_SIZE 80
#define MAX_TOTAL_SIZE 1024

// Headers for each OSI layer
const char * headers[7] = {
    "[Application Layer]",
    "[Presentation Layer]",
    "[Session Layer]",
    "[Transport Layer]",
    "[Network Layer]",
    "[Data Link Layer]",
    "[Physical Layer]"
};

// Set function

void application_layer(char* message, int size);
void presentation_layer(char* message, int size);
void session_layer(char* message, int size);
void transport_layer(char* message, int size);
void network_layer(char* message, int size);
void data_link_layer(char* message, int size);
void physical_layer(char* message, int size);

// 7th layer of OSI model
void application_layer(char* message, int size) {
    char new_message[MAX_TOTAL_SIZE];
    
    // Add header in front of the message
    strcpy(new_message, headers[0]);
    strcat(new_message, message);

    int new_size = strlen(new_message);
    
    printf("Layer 7 (Application Layer): %s\n", new_message);

        // Call the next layer
    presentation_layer(new_message, new_size);
}

// 6th layer of OSI model
void presentation_layer(char* message, int size) {
    char new_message[MAX_TOTAL_SIZE];
    
    // Add header in front of the message
    strcpy(new_message, headers[1]);
    strcat(new_message, message);

    int new_size = strlen(new_message);

    printf("Layer 6 (Presentation Layer): %s\n", new_message);
        
        // Call the next layer
    session_layer(new_message, new_size);
}
// 5th layer of OSI model
void session_layer(char* message, int size) {
    char new_message[MAX_TOTAL_SIZE];
    
    // Add header in front of the message
    strcpy(new_message, headers[2]);
    strcat(new_message, message);

    int new_size = strlen(new_message);

    printf("Layer 5 (Session Layer): %s\n", new_message);
        
        // Call the next layer
    transport_layer(new_message, new_size);
}
// 4th layer of OSI model                      
void transport_layer(char* message, int size) {
    char new_message[MAX_TOTAL_SIZE];
    
    // Add header in front of the message
    strcpy(new_message, headers[3]);
    strcat(new_message, message);

    int new_size = strlen(new_message);

    printf("Layer 4 (Transport Layer): %s\n", new_message);
        
        // Call the next layer
    network_layer(new_message, new_size);
}
// 3rd layer of OSI model
void network_layer(char* message, int size) {
    char new_message[MAX_TOTAL_SIZE];
    
    // Add header in front of the message
    strcpy(new_message, headers[4]);
    strcat(new_message, message);

    int new_size = strlen(new_message);

    printf("Layer 3 (Network Layer): %s\n", new_message);
        
        // Call the next layer
    data_link_layer(new_message, new_size);
}
// 2nd layer of OSI model
void data_link_layer(char* message, int size) {
    char new_message[MAX_TOTAL_SIZE];
    
    // Add header in front of the message
    strcpy(new_message, headers[5]);
    strcat(new_message, message);

    int new_size = strlen(new_message);

    printf("Layer 2 (Data Link Layer): %s\n", new_message);
        
        // Call the next layer
    physical_layer(new_message, new_size);
}
// 1st layer of OSI model
void physical_layer(char* message, int size) {
    char new_message[MAX_TOTAL_SIZE];
    
    // Add header in front of the message
    strcpy(new_message, headers[6]);
    strcat(new_message, message);

    int new_size = strlen(new_message);

    printf("Layer 1 (Physical Layer): %s\n", new_message);
    printf("This is the last layer, no further processing.\n");
    printf("Ready to transmit the message.\n");
    printf("Final message size: %d bytes\n", (int)strlen(new_message)); 
}

int main(){
    char input_message[MAX_MESSAGE_SIZE + 1];
    printf("==== OSI Model Simulation ====\n");
    printf("Enter a message to send (max %d characters): ", MAX_MESSAGE_SIZE);

    // Read input message
    if (fgets(input_message, sizeof(input_message), stdin) != NULL){
        //remove newline character if present
        size_t len = strlen(input_message);
        if (len > 0 && input_message[len - 1] == '\n') {
            input_message[len - 1] = '\0';
        }
        printf("Starting OSI model processing...\n");
        printf("Original message: %s\n", input_message);
        
        // Start processing from the application layer
        application_layer(input_message, strlen(input_message));
        printf("OSI model processing completed.\n");
    } else {
        printf("Error reading input message.\n");   
        return 1;
    }
    return 0;
}



/* This code simulates the OSI model by processing a message through each layer,
// adding a header at each layer, and printing the message at each step.
// The message is processed from the application layer down to the physical layer,
// demonstrating how data is encapsulated at each layer of the OSI model.
// The program reads a message from the user, processes it through the OSI layers,
// and prints the final message ready for transmission.*/
