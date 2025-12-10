import javax.swing.*;
import javax.swing.table.DefaultTableModel;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class CarRentalSystem extends JFrame {

    // UI components
    private JTextField txtCustomerName;
    private JTextField txtPhone;
    private JComboBox<String> cmbCarModel;
    private JTextField txtDays;
    private JTextField txtRatePerDay;
    private JTextField txtTotalCost;

    private JButton btnCalculate;
    private JButton btnAddBooking;
    private JButton btnClear;

    private JTable tblBookings;
    private DefaultTableModel tableModel;

    // Car models and their rates
    private String[] carModels = {"Select Car", "Hatchback", "Sedan", "SUV", "Luxury"};
    private double[] carRates = {0.0, 1500.0, 2000.0, 3000.0, 5000.0};

    public CarRentalSystem() {
        setTitle("Car Rental System");
        setSize(800, 500);
        setLocationRelativeTo(null);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLayout(new BorderLayout(10, 10));

        // Top panel (title)
        JLabel
