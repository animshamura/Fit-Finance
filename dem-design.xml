import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    private EditText incomeEditText, expenseEditText;
    private TextView balanceTextView;
    private double balance = 0.0;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        incomeEditText = findViewById(R.id.incomeEditText);
        expenseEditText = findViewById(R.id.expenseEditText);
        balanceTextView = findViewById(R.id.balanceTextView);
        Button addIncomeButton = findViewById(R.id.addIncomeButton);
        Button addExpenseButton = findViewById(R.id.addExpenseButton);

        addIncomeButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                addIncome();
            }
        });

        addExpenseButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                addExpense();
            }
        });
    }

    private void addIncome() {
        double income = Double.parseDouble(incomeEditText.getText().toString());
        balance += income;
        updateBalance();
        incomeEditText.setText("");
    }

    private void addExpense() {
        double expense = Double.parseDouble(expenseEditText.getText().toString());
        balance -= expense;
        updateBalance();
        expenseEditText.setText("");
    }

    private void updateBalance() {
        balanceTextView.setText(String.format("Balance: $%.2f", balance));
    }
}
