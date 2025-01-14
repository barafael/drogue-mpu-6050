# MPU6050-DMP Examples

This directory contains examples demonstrating various features of the MPU6050 sensor with its Digital Motion Processor (DMP).

## Examples

### [Basic Async](src/basic_async.rs)
Basic example showing how to:
- Initialize the sensor with async I2C
- Load and initialize the DMP firmware
- Perform sensor calibration
- Read accelerometer, gyroscope and temperature data

### [DMP Features](src/dmp_features.rs)
Example demonstrating sample rate configuration and high-frequency data sampling:
- Digital Motion Processor (DMP) initialization
- Configuring custom sample rate (100Hz)
- Reading combined 6-axis motion data
- High-frequency data sampling demonstration

### [FIFO Buffer](src/fifo_buffer.rs)
Example showing FIFO buffer operations:
- Initialize and calibrate the sensor
- Enable and configure FIFO buffer
- Monitor FIFO count and read data
- Handle buffer overflow conditions
- Process raw sensor data

### [Quaternion Data](src/quaternion.rs)
Example demonstrating 3D orientation tracking:
- Initialize and calibrate the sensor
- Configure DMP for quaternion output
- Read quaternion data for orientation
- Convert quaternions to Euler angles (roll, pitch, yaw)

### [Motion Detection](src/motion_detection.rs)
Example showing software-based motion detection:
- Initialize and calibrate the sensor
- Detect motion using configurable thresholds
- Wake on Interrupt Pin

## Building and Running

1. Connect your MPU6050 to a Raspberry Pi Pico:
   - SDA -> GP14
   - SCL -> GP15
   - VCC -> 3.3V
   - GND -> GND

2. Build and flash an example:
   ```bash
   # For the basic example
   cargo run --example basic_async

   # For DMP features example
   cargo run --example dmp_features

   # For FIFO buffer example
   cargo run --example fifo_buffer

   # For quaternion data example
   cargo run --example quaternion_async

   # For motion detection example
   cargo run --example motion_detection
   ```
