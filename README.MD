Project structure:
Two TestSuites for two SoapServices
  1. SpellServiceSoap TestSuite
  Four TestCases for first SoapService  
    1. text_get_positive(Condition example with groovy help)
    This test simply checks CheckTextRequest feature of first SoapService
    It got 7 steps:
      i. Properties - where we store temporaly variables
      ii. check_texts_set_up - checks if Properties are set for tests and sets them if they are empty
      iii. text_test_ru checks input of russian text
      iv. text_test_eng checks input of english text
      v. text_retest_ru - retests the results of text_test_ru
      vi. text_retest_eng - retests the rulults of text_test_eng
      vii. save_text_test is used for transfering data from 3 and 4 points to properties
      
    2. text_get_negative
    This test got negative result from expected
    It got 2 steps:
      1. text_test_ru
      2. text_test_eng
    3. texts_get_negative
    This test got negative result from expected
    It got 1 step:
      1. texts_test_ru
    4. text_get_positive(DDT example)
    The most complex one test, it includes two groovy scripts for running as a DDT test by TestRunner
    It got 5 steps:
      1. Properties - there stored all data for comparing results and providing data for test
      2. setting values for test - prepares all need data for current test step
      3. text_check - makes soap request and gets data
      4. save_results - transfers data from point 3 to Properties
      5. assertion - asserts result of test and continues it's execution until all data is checked
  2. SpellServiceSoap12 TestSuite
  Two TestCases for second SoapService
    1. ServiceSoap12 text_get_positive
    Simple positive test for second SoapService
    It got 2 steps:
      1. text_test_ru
      2. text_test_eng
    2. ServiceSoap12 text_get_negative
    Simple negative test for second SoapService
    It got 2 steps:
      1. text_test_ru
      2. text_test_eng
