# GulDiyet - Diet and Nutrition Management Platform

## Overview
GulDiyet is a modern and efficient platform designed to streamline the workflows of dietitians. Unlike other platforms, GulDiyet uniquely integrates advanced real-time communication and scalable microservices architecture to deliver unmatched performance and reliability. Its innovative features include PDF-based reporting, real-time appointment updates, and seamless management of laboratory results, making it a comprehensive solution for dietitians and their clients.

## Features
- **Appointment Management**: Schedule, modify, and track patient appointments.
- **Laboratory Results**: Manage test results and generate reports.
- **Real-Time Communication**: Uses SignalR for instant updates and notifications.
- **PDF Reporting**: Generate comprehensive patient and laboratory reports in PDF format.
- **Enterprise Service Bus (ESB)**: Implements MassTransit with RabbitMQ for efficient message brokering.
- **Scalable Architecture**: Built using Onion Architecture for modularity and maintainability.

## Project Structure
```
GulDiyet
│
├── Controllers
│   ├── AppointmentController.cs          # Handles appointment operations
│   ├── DietPlanController.cs             # Manages diet plans
│   ├── LaboratoryResultController.cs     # Handles lab results
│   ├── PatientController.cs              # Manages patient records
│   ├── UserController.cs                 # Manages user authentication
│
├── Middlewares
│   ├── NotifyNewDietPlanMiddleware.cs    # Sends notifications for new diet plans
│   ├── ValidateUserSession.cs            # Validates user sessions
│
├── Models
│   ├── ErrorViewModel.cs                 # Error handling model
│
├── Views
│   ├── Appointment                       # Views related to appointments
│   ├── LaboratoryResult                  # Views related to lab results
│   ├── Shared                            # Shared UI components
│
├── Infrastructure
│   ├── Persistence
│       ├── Migrations                    # Database migration files
│       ├── Repositories                  # Data access layer
│
├── wwwroot
│   ├── css                               # Custom CSS files
│   ├── js                                # Custom JavaScript files
│   ├── Images                            # Static image resources
│
├── appsettings.json                      # Application configuration
├── Program.cs                            # Entry point of the application
├── GulDiyet.csproj                       # Project file
```

## Technologies Used
- **Backend**: ASP.NET Core, SignalR
- **Frontend**: Razor Views, Bootstrap
- **Database**: Microsoft SQL Server
- **Messaging**: RabbitMQ, MassTransit
- **Architecture**: Onion Architecture

## Getting Started

### Prerequisites
Ensure the following tools are installed:
- **.NET 6.0 SDK**
- **Microsoft SQL Server**
- **RabbitMQ**

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/GulDiyet.git
   cd GulDiyet
   ```

2. Restore dependencies:
   ```bash
   dotnet restore
   ```

3. Apply database migrations:
   ```bash
   dotnet ef database update
   ```

4. Run the application:
   ```bash
   dotnet run
   ```

### Configuration
Update the `appsettings.json` file to configure:
- **Database Connection**: Add your SQL Server connection string.
- **RabbitMQ**: Set up RabbitMQ credentials and server URL.

## Usage
- **Access the Application**: Navigate to `http://localhost:5000` in your browser.
- **Manage Appointments**: Use the Appointment module to schedule or edit patient visits.
- **View Laboratory Results**: Access detailed laboratory reports.
- **Generate Reports**: Create and download PDF reports for patients and test results.

## Contribution
Contributions are welcome! Follow these steps:
1. Fork the repository.
2. Create a new feature branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -m 'Add feature'`
4. Push to the branch: `git push origin feature-name`
5. Submit a pull request.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Contact
For any inquiries or feedback, feel free to reach out:
- **Email**: eraykelesk@gmail.com
- **LinkedIn**: [Eray Keleş](https://linkedin.com/in/eraykeles)

---

Start streamlining dietitian workflows with GulDiyet today!
