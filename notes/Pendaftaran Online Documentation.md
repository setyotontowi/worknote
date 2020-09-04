---
tags: [Research/Android]
title: Pendaftaran Online Documentation
created: '2019-11-21T06:13:09.843Z'
modified: '2019-11-25T07:43:00.618Z'
---

# Pendaftaran Online Documentation

## Technical Documentation

### 1. List Files
 
| No | Files                                                    | Keterangan  |
|----|-------------------------------------------------------   |-------------|
| 1. | **Activities/Akun/** AnnouncementActivity.java           |             |
| 2. | **Activities/Akun/** BiodataPasienBaruActivity.java      |             |
| 3. | **Activities/Akun/** BookingHistoryActivity.java         |             |
| 4. | **Activities/Akun/** ChangePasswordActivity.java         |             |
| 5. | **Activities/Akun/** InvoiceActivity.java                |             |
| 6. | **Activities/Akun/** PasienBaruDataActivity.java         |             |
| 7. | **Activities/Akun/** TermAndConditionActivity.java       |             |
| 8. | **Activities/Akun/** UserProfilActivity.java             |             |
| 9. | **Activities/InfoClinic/** DoctorQueueActivity.java      |             |
| 10.| **Activities/Login/** FirstActivity.java                 | Login       |
| 11.| **Activities/Login/** LoginActivity.java                 | Login       |
| 12.| **Activities/Login/** RegisterActivity.java              | Login       |
| 13.| **Activities/** InfoBayarActivity.java                   |             |
| 14.| **Activities/** MainActivity.java                        | Main        |
| 15.| **Activities/** OrderActivity.java                       |             |
| 16.| **Activities/** PasienBaruActivity.java                  |             |
| 17.| **Activities/** TicketActivity.java                      |             |
| 18.| **Adapters/** ActiveBookingAdapter.java                  |             |
| 19.| **Adapters/** BookingHistoryAdapter.java                 |             |
| 20.| **Adapters/** DataPasienBaruAdapter.java                 |             |
| 21.| **Adapters/** DoctorQueueAdapter.java                    |             |
| 22.| **Adapters/** InvoiceAdapter.java                        |             |
| 23.| **Adapters/** SampleAdapter.java                         |             |
| 24.| **Fragments/Login/** CreateNewPasswordFragment.java      |             |
| 25.| **Fragments/Login/** LoginFragment.java                  |             |
| 26.| **Fragments/Login/** VerificationForgotPassFragment.java |             |
| 27.| **Fragments/Main/** AccountFragment.java                 |             |
| 28.| **Fragments/Main/** InfoBedFragment.java                 |             |
| 29.| **Fragments/Main/** InfoClinicFragment.java              |             |
| 30.| **Fragments/Main/** ProfilFragment.java                  |             |
| 31.| **Fragments/Order/** ClinicFragment.java                 |             |
| 32.| **Fragments/Order/** DoctorFragment.java                 |             |
| 33.| **Fragments/Order/** EntryOrder2Fragment.java            |             |
| 34.| **Fragments/Order/** EntryOrderFragment.java             |             |
| 35.| **Fragments/Order/** ScheduleFragment.java               |             |
| 35.| **Fragments/Order/** ScheduleFragment.java               |             |
| 36.| **Fragments/Register/** RegisterFragment.java            |             |
| 37.| **Fragments/Register/** VerificationFragment.java        |             |
| 38.| **Models/** Antrian.java                                 |             |
| 39.| **Models/** Asuransi.java                                |             |
| 40.| **Models/** BedAvailable.java                            |             |
| 41.| **Models/** DataPasienBaru.java                          |             |
| 42.| **Models/** HasilBooking.java                            |             |
| 43.| **Models/** Image.java                                   |             |
| 44.| **Models/** Jadwal.java                                  |             |
| 45.| **Models/** JadwalDetail.java                            |             |
| 46.| **Models/** KeyValue.java                                |             |
| 47.| **Models/** MenuAccount.java                             |             |
| 48.| **Models/** Pasien.java                                  |             |
| 49.| **Models/** Pegawai.java                                 |             |
| 50.| **Models/** Poliklinik.java                              |             |
| 51.| **Models/** Sample.java                                  |             |
| 52.| **Utils/** BottomNavigationViewHelper.java               |             |
| 53.| **Utils/** GeneralHelper.java                            |             |
| 54.| **Utils/** ImageSliderFragment.java                      |             |
| 55.| **Utils/** MySingleton.java                              |             |
| 56.| **Utils/** RuntimePermissionActivity.java                |             |
| 57.| **Utils/** StartSnapHelper.java                          |             |
| 58.| **Utils/** URLSPanNoUnderline.java                       |             |
| 59.| **Views/** TicketView.java                               |             |

### 2. List Classes

1. **AnnouncementActivity**

| No | Files                                   | Method               | Keterangan          |
|----|-----------------------------------------|----------------------|---------------------|
| 1. | AnnouncementActivity                    | onCreate             |                     |
|    |                                         | getAnnouncement      |                     |
|    |                                         | initWebView          |                     |
|    |                                         | onSupportNavigateUp  |                     |
|    |                                         | onPause              |                     |
| 2. | MyWebChromeClient                       | myWebChromeClient    |                     |
|    |                                         | onPermissionRequest  |                     |
| 3. | GeneralHelper                           | showProgressDialog   |                     |
|    |                                         | captureResponse      |                     |
|    |                                         | captureJSONException |                     |
|    |                                         | dismissProgressDialog|                     |
|    |                                         | captureErrorListener |                     |
|    |                                         | headerPostAfterLogin |                     |
| 4. | MySingleton                             | getInstance          |                     |



2. **BiodataPasienBaruActivity**

| No | Files                                   | Method                 | Keterangan          |
|----|-----------------------------------------|------------------------|---------------------|
| 1. | BiodataPasienBaruActivity               | onCreate               |                     |
|    |                                         | setData                |                     |
|    |                                         | onPause                |                     |
|    |                                         | onSupportNavigateUp    |                     |
|    |                                         | onScrollChange         |                     |
| 2. | DataPasienBaru                          | getKonfirmasiRegPasien |                     |
|    |                                         | getKdJenisKelamin      |                     |
|    |                                         | getNoRM                |                     |
|    |                                         | getNmPasien            |                     |
|    |                                         | getNmRegPasien         |                     |
|    |                                         | getNoId                |                     |
|    |                                         | getTglLahir            |                     |
|    |                                         | getNmOrtu              |                     |
|    |                                         | getNmSuamiIstri        |                     |
|    |                                         | getAgamaList           |                     |
|    |                                         | getPendidikanList      |                     |
|    |                                         | getPekerjaanList       |                     |
|    |                                         | getAlamat              |                     |
|    |                                         | getRt                  |                     |
|    |                                         | getRw                  |                     |
|    |                                         | getDesaList            |                     |
|    |                                         | getKecamatanList       |                     |
|    |                                         | getKabupatenList       |                     |
|    |                                         | getProvinsiList        |                     |


3. **BookingHistoryActivity**

| No | Files                                   | Method                 | Keterangan            |
|----|-----------------------------------------|------------------------|-----------------------|
| 1. | BookingHistoryActivity                  | onCreate               |                       |
|    |                                         | onResume               |                       |
|    |                                         | getListBookingHistory  |                       |
|    |                                         | onSupportNavigateUp    |                       |
|    |                                         | onPause                |                       |
|    |                                         | onShowTicket           | BookingHistoryAdapter |
|    |                                         | onRefresh              |                       |
| 2. | InfoBayarActivity                       |                        | : intent              |
| 3. | FirstActivity                           |                        | : variables           |
| 4. | TicketActivity                          |                        | : intent              |
| 5. | BookingHistoryAdapter                   | onShowTicket           |                       |
| 6. | HasilBooking                            | HasilBooking           |                       |
| 7. | Pasien                                  | Pasien                 |                       |
| 8. | Poliklinik                              | Poliklinik             |                       |
| 9. | GeneralHelper                           | dismissProgressDialog  |                       |
|    |                                         | captureJSONException   |                       |
|    |                                         | captureErrorListener   |                       |
|    |                                         | headerPostAfterLogin   |                       |
|10. | MySingleton                             | getInstance            |                       |


4. **ChangePasswordActivity**

| No | Files                                   | Method                 | Keterangan            |
|----|-----------------------------------------|------------------------|-----------------------|
| 1. | ChangePasswordActivity                  | onCreate               |                       |
|    |                                         | requestChangePassword  |                       |
|    |                                         | validation             |                       |
|    |                                         | onSupportNavigateUp    |                       |
|    |                                         | onPause                |                       |
| 2. | FirstActivity                           |                        | : variables           |
| 3. | GeneralHelper                           | showProgressDialog     |                       |
|    |                                         | dismissProgressDialog  |                       |
|    |                                         | captureResponse        |                       |
|    |                                         | dialogInfo             |                       |
|    |                                         | captureJSONException   |                       |
|    |                                         | captureErrorListener   |                       |
|    |                                         | headerPostAfterLogin   |                       |


5. **InvoiceActivity**

| No | Files                                   | Method                 | Keterangan            |
|----|-----------------------------------------|------------------------|-----------------------|
| 1. | InvoiceActivity                         | onCreate               |                       |
|    |                                         | getListInvoice         |                       |
|    |                                         | onRefresh              |                       |
|    |                                         | onResume               |                       |
|    |                                         | onPause                |                       |
|    |                                         | onSupportNavigateUp    |                       |
|    |                                         | onShowInfoBayar        | InvoiceAdapter        |
| 2. | InfoBayarActivity                       |                        | : intent              |
| 3. | FirstActivity                           |                        | : variables           |
| 4. | InvoiceAdapter                          | InvoiceAdapter         |                       |
|    |                                         | notifyDataSetChanged   |                       |
| 5. | HasilBooking                            | HasilBooking           |                       |
|    |                                         | getCaraBayar           |                       |
|    |                                         | getStatusBayar         |                       |
| 6. | Pasien                                  | Pasien                 |                       |
| 7. | Poliklinik                              | Poliklink              |                       |
| 8. | GeneralHelper                           | captureResponse        |                       |
| 9. | MySingleton                             | getInstance            |                       |


6. **PasienBaruDataActivity**

| No | Files                                   | Method                 | Keterangan            |
|----|-----------------------------------------|------------------------|-----------------------|
| 1. | PasienBaruDataActivity                  | onCreate               |                       |
|    |                                         | getListDataPasienBaru  |                       |
|    |                                         | onRefresh              |                       |
|    |                                         | onResume               |                       |
|    |                                         | onPause                |                       |
|    |                                         | onSupportNavigateUp    |                       |
|    |                                         | onClickPasienBaru      |                       |
| 2. | FirstActivity                           |                        | : variables           |
| 3. | DataPasienBaruAdapter                   | DataPasienBaruAdapter  |                       |
|    |                                         | notifyDataSetChanged   |                       |
| 4. | DataPasienBaru                          | DataPasienBaru         |                       |
| 5. | KeyValue                                | KeyValue               |                       |
| 6. | GeneralHelper                           | captureResponse        |                       |
|    |                                         | captureJSONException   |                       |
|    |                                         | captureErrorListener   |                       |
|    |                                         | headerPostAfterLogin   |                       |
| 7. | MySingleton                             | getInstance            |                       |

7. **TermAndConditionActivity**

| No | Files                                   | Method                 | Keterangan            |
|----|-----------------------------------------|------------------------|-----------------------|
| 1. | TermAndConditionActivity                | onCreate               |                       |
|    |                                         | getTermAndCondition    |                       |
|    |                                         | initWebView            |                       |
|    |                                         | onSupportNavigateUp    |                       |
|    |                                         | onPause                |                       |
| 2. | GeneralHelperActivity                   | showProgressDialog     |                       |
|    |                                         | captureResponse        |                       |
|    |                                         | captureJSONException   |                       |
|    |                                         | dismissProgressDialog  |                       |
|    |                                         | captureErrorListener   |                       |
|    |                                         | headerPostAfterLogin   |                       |
| 3. | MySingleton                             | getInstance            |                       |
| 4. | MyWebChromeClient                       | MyWebChromeClient      |                       |
|    |                                         | onPermissionRequest    |                       |

8. **UserProfilActivity**

| No | Files                                   | Method                 | Keterangan            |
|----|-----------------------------------------|------------------------|-----------------------|
| 1. | UserProfilActivity                      | onCreate               |                       |
|    |                                         | setKelamin             |                       |
|    |                                         | setDatePicker          |                       |
|    |                                         | bodySaveProfil         |                       | 
|    |                                         | validation             |                       |
|    |                                         | saveProfil             |                       |
|    |                                         | getDataProfil          |                       |
|    |                                         | onSupportNavigateUp    |                       |
|    |                                         | onPause                |                       |
| 2. | FirstActivity                           |                        | :variables            |
| 3. | GeneralHelper                           | requestFocus           |                       |
|    |                                         | showProgressDialog     |                       |
|    |                                         | dismissProgressDialog  |                       |
|    |                                         | captureResponse        |                       |
|    |                                         | dialogInfo             |                       |
|    |                                         | captureJSONException   |                       |
|    |                                         | captureErrorListener   |                       |
|    |                                         | headerPostAfterLogin   |                       |

9. **DoctorQueueActivity**

| No | Files                                   | Method                 | Keterangan            |
|----|-----------------------------------------|------------------------|-----------------------|
| 1. | DoctorQueueActivity                     | onCreate               |                       |
|    |                                         | onResume               |                       |
|    |                                         | getListAntrian         |                       |
|    |                                         | onSupportNavigateUp    |                       |
|    |                                         | onPause                |                       |
|    |                                         | onRefresh              |                       | 
|    |                                         | search                 |                       |
| 2. | DoctorQueueAdapter                      | DoctorQueueAdapter     |                       |
|    |                                         | notifyDataSetChanged   |                       |
|    |                                         | getFilter              |                       |
| 3. | Antrian                                 | Antrian                |                       |
| 4. | Poliklinik                              | getNmPoliklinik        |                       |
|    |                                         | getPkPoliklinik        |                       |
| 5. | GeneralHelper                           | captureResponse        |                       |
|    |                                         | captureJSONException   |                       |
|    |                                         | captureErrorListener   |                       |
|    |                                         | getDateNowSQLFormat    |                       |
|    |                                         | headerPostAfterLogin   |                       |

10. **FirstActivity**

when user install it at first time or when prefs not yet generated. included also login and register activity

| No | Files                                 | Method                      | Keterangan            |
|----|---------------------------------------|-----------------------------|-----------------------|
| 1. | FirstActivity                         | onCreate                    |                       |
|    |                                       | onPermissionGranted         |                       |
|    |                                       | createPreferenceRegister    |                       |
|    |                                       | createPreferenceLogin       |                       |
|    |                                       | createPreferenceForgotPass  |                       |
|    |                                       | createPreferenceKodeBooking |                       |
|    |                                       | checkUpdate                 |                       |
|    |                                       | updateResult                |                       |
| 2. | MainActivity                          |                             | :intent               |
| 3. | GeneralHelper                         | isPrefExist                 |                       |
|    |                                       | captureResponse             |                       |
|    |                                       | showProgressDialog          |                       |
|    |                                       | captureJSONException        |                       |
|    |                                       | dismissProgressDialog       |                       |
|    |                                       | captureErrorListener        |                       |
|    |                                       | headerPostCheckUpdate       |                       |
| 4. | MySingleton                           | getInstance                 |                       |
| 5. | RunTimePermissionActivity             |                             | :extend               |

11. **LoginActivity**

| No | Files                              | Method                           | Keterangan            |
|----|----------------------------------- |--------------------------------- |-----------------------|
| 1. | LoginActivity                      | onCreate                         |                       |
|    |                                    | onSupportNavigateUp              |                       |
|    |                                    | onPause                          |                       |
|    |                                    | onVerificationForgotPassSuccess  |                       |
|    |                                    | onResetPasswordSuccess           |                       |
|    |                                    | onLoginSuccess                   |                       |
|    |                                    | onRequestForgotPasswordSuccess   |                       |
