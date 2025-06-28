# Mini Reconciliation Tool

A React app to compare transaction data from your internal system and payment provider CSV exports — highlighting matches, mismatches, and missing transactions.

## 🔍 Features Included

- Upload two CSV files: **Internal System Export** & **Provider Statement**
- Match transactions using `transaction_reference`
- Categorize results into:
  - Matched Transactions
  - Present only in Internal file
  - Present only in Provider file
- Highlight mismatches in `amount` or `status`
- Export each category as a separate CSV file
- Visual indicators for success, warnings, and errors
- Basic UI with feedback messages and loading states

## 📂 How to Use

1. Upload the **Internal System Export** CSV file  
2. Upload the **Provider Statement** CSV file  
3. Click **Compare Transactions**  
4. View the categorized results with mismatches highlighted  
5. Optionally export each result group as a CSV

## 🧠 Assumptions Made

- Input CSV files must have headers: `transaction_reference`, `amount`, and `status`
- Files are small and manageable in the browser (client-side only)
- Users access the tool via modern desktop browsers (e.g., Chrome, Edge, Firefox)
- No user authentication is required

## ⚙️ Tech Stack

- **React** (Functional components + Hooks)
- **PapaParse** for CSV parsing
- **react-csv** for export functionality
- **Vite** for development and build tooling

## 🚀 Improvements I'd Make with More Time

- Enhance mobile responsiveness for smaller screens
- Support varied column naming and field validation
- Build a backend to:
  - Handle larger files
  - Log audits
  - Enable secure file storage
- Add CSV preview/edit capability before comparing
- Add transaction count summaries and filtering options (e.g., show only mismatches)
- Implement dark mode or customizable UI themes

