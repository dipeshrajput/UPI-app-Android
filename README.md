# UPI-app-Android
Youtube link->https://youtu.be/sJiTHK95TEw

kind of structure|
                \/

al uri: Uri = Uri.Builder()
        .scheme("upi")
        .authority("pay")
        .appendQueryParameter("pa", MY_UPI_ID)
        .appendQueryParameter("pn", MY_USER_NAME)
        //.appendQueryParameter("mc", "1234")
        //.appendQueryParameter("tr", "123456789")
        .appendQueryParameter("tn", "test transaction note")
        .appendQueryParameter("am", "2500.00")
        .appendQueryParameter("cu", "INR")
        //.appendQueryParameter("url", "https://test.merchant.website")
        .build()
    
    
    val intent = Intent(Intent.ACTION_VIEW)
    intent.data = uri
    intent.setPackage(GOOGLE_PAY_PACKAGE_NAME)
    startActivityForResult(intent, PAY_REQUEST_CODE)
