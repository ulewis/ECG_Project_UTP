# Define compiler
CXX := g++ -std=c++17

# Include directories
INCDIR := -I../TML_ECG_Analyzer -I../Arduino_TML_ECG -I../CppUnitLite


# Source files
SOURCES := $(wildcard *.cpp)

# Object files
OBJECTS := $(SOURCES:.cpp=.o)

# Header files
# Header files
HEADERS := $(wildcard ../Arduino_TML_ECG/*.h)


# Executable name
EXECUTABLE := UnitTests

# Library paths
LDFLAGS := -L../CppUnitLite

# Libraries to link against
LDLIBS := -lCppUnitLite

# Compiler flags
CXXFLAGS := -g -Wall $(INCDIR)

# Targets
.PHONY: all clean

all: $(EXECUTABLE)

$(EXECUTABLE): $(OBJECTS)
	$(CXX) $(LDFLAGS) -o $@ $^ $(LDLIBS)

%.o: %.cpp $(HEADERS)
	$(CXX) $(CXXFLAGS) -c $< -o $@

clean:
	rm -f $(OBJECTS) $(EXECUTABLE)