SDK_ROOT := ../..

SDK_LIB  := $(SDK_ROOT)/output/Linux/Release/libsl_lidar_sdk.a

CXX      := g++
CXXFLAGS := -std=c++11 -O2 \
            -I$(SDK_ROOT)/sdk/include \
            -I$(SDK_ROOT)/sdk/src

LDFLAGS  := $(SDK_LIB) -lSDL2 -lm -lpthread

TARGET   := ultra_simple
SRC      := main.cpp
OBJ      := $(SRC:.cpp=.o)

all: $(TARGET)

$(TARGET): $(OBJ)
	$(CXX) -o $@ $^ $(LDFLAGS)

%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c $< -o $@

clean:
	rm -f $(TARGET) $(OBJ)
