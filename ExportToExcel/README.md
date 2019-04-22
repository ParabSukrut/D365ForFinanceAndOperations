This class shows how you can utilized ExcelWorkbook and ExcelWorksheet classes wot export records from Dynamics 365 for finance and operations .This is generic class and can be used on any form.

For demonstration purpose I am just selected voucher transactions form and with only two records. Voucher transactions form is widely used by GL team and GL teams wants to export data from this form for reconciliation purpose. 
Steps to Implement this feature 
1.	Create extension for the form you want to implement this feature. 
2.	Add a button Group in an extension as shown in below screenshot . I added button group called “ExportGroup”
3.	Add export to Excel button in that group
4.	Subscribe to the onClicked event of that button and implement following code.

[FormControlEventHandler(formControlStr(LedgerTransVoucher, ExportToExcel), FormControlEventType::Clicked)]
    public static void ExportToExcel_OnClicked(FormControl sender, FormControlEventArgs e)
    {
        ExportToExcel		exporttoExcel;
        FormRun formRun = sender.formRun() as FormRun;
        


        exporttoExcel = new HSLExportToExcel();
        exporttoExcel.parmGridControl(formRun.design().controlName("OverviewGrid"));
        exporttoExcel.parmFileName('VoucherTrans');
        exporttoExcel.exportToExcel();

    }
