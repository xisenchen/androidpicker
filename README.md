# androidPicker
公用选择器
1.时间选择器
    public void onYearPicker(final TextView view) {
        DatePicker picker = new DatePicker(this, DatePicker.YEAR);
        Calendar calendar = Calendar.getInstance();
        int yearNow =  calendar.get(Calendar.YEAR);
        picker.setRange(2009, yearNow);
        picker.setSelectedItem(yearNow, 1);

        picker.setOnDatePickListener(new DatePicker.OnYearMonthPickListener() {
            @Override
            public void onDatePicked(String year, String month) {
                view.setText(year);
                repYear = year;
            }
        });
        picker.show();
        picker.show();
    }
	
MainActivity有所有相关使用