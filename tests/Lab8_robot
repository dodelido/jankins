*** Settings ***
Library    SeleniumLibrary

*** Keywords ***
Open Browser To Login Page
    ${chrome_options}=    Evaluate    sys.modules['selenium.webdriver'].ChromeOptions()    sys
    Call Method    ${chrome_options}    add_argument    --no-sandbox
    Call Method    ${chrome_options}    add_argument    --disable-dev-shm-usage
    Call Method    ${chrome_options}    add_argument    --headless
    
    Create Webdriver    Chrome    options=${chrome_options}
    Go To    https://computing.kku.ac.th

*** Test Cases ***
System Health Check
    [Documentation]    ตรวจสอบสถานะระบบพื้นฐาน
    Log    Jenkins Robot Framework system is healthy
    Should Be True    ${True}

String Comparison Test
    [Documentation]    ทดสอบการเปรียบเทียบข้อความ
    ${msg}=    Set Variable    Software Engineering
    Should Be Equal    ${msg}    Software Engineering

Math Calculation Test
    [Documentation]    ทดสอบการคำนวณตัวเลข
    ${result}=    Evaluate    10 * 5
    Should Be Equal As Integers    ${result}    50

Fail Scenario Test
    [Documentation]    ตัวอย่าง test ที่ fail เพื่อทดสอบ Threshold
    ${value}=    Evaluate    2 + 2
    Should Be Equal As Integers    ${value}    5

