from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
import time

def setup_driver():
    driver = webdriver.Chrome()
    driver.implicitly_wait(10)
    return driver

def test_home_page_load(driver):
    driver.get("https://www.medplusmart.com")
    
def login_function(driver):
    sign_up=driver.find_element(By.XPATH,'//*[@id="signInLink"]/span[1]')
    sign_up.click()
    time.sleep(5)
    phone_field=WebDriverWait(driver, 5).until(
        EC.presence_of_element_located((By.XPATH, '//*[@id="mobileNumber"]'))
    )
    phone_field.send_keys('6366024023')
    time.sleep(5)
    otp_button=driver.find_element(By.XPATH,'/html/body/div[2]/div/div[1]/div/div/div[2]/div/div/div/button')
    otp_button.click()
    time.sleep(15)
    skip=driver.find_element(By.XPATH,'/html/body/div[2]/div/div[1]/div/div/div[2]/div/div/a')
    skip.click()
    time.sleep(5)
    
def user_details(driver):
    user=driver.find_element(By.XPATH,'//*[@id="app"]/header/div/div[2]/div[3]/button')
    user.click()
    time.sleep(5)
    my_account=driver.find_element(By.XPATH,'//*[@id="app"]/header/div/div[2]/div[3]/div/button[1]')
    my_account.click()
    time.sleep(5)
    time.sleep(5)
    home_button=driver.find_element(By.XPATH,'//*[@id="app"]/div/main/nav/ol/li[1]/button')
    home_button.click()
    time.sleep(5)
    clear_cart=driver.find_element(By.XPATH,'//*[@id="app"]/header/div/div[2]/div[2]/div/button')
    clear_cart.click()
    time.sleep(5)
    clear=driver.find_element(By.XPATH,'//*[@id="app"]/header/div/div[2]/div[2]/div/div/div/div[1]/span')
    clear.click()
    
def medicine_search(driver):
    medicine=driver.find_element(By.XPATH,'//*[@id="app"]/div/main/div/div/div[1]/div/div/div[1]/div/input')
    medicine.click()
    time.sleep(5)
    search_field= driver.find_element(By.XPATH,'/html/body/div[2]/div/div[1]/div/div/div/div/div/div[1]/div/div/input')
    search_field.send_keys('dolo')
    time.sleep(5)
    select1=driver.find_element(By.XPATH,'/html/body/div[2]/div/div[1]/div/div/div/div/div/div[2]/div/div[1]/div/div[2]/div[1]/div[1]/p[1]')
    select1.click()
    time.sleep(10)
    add_to_cart=driver.find_element(By.XPATH,'//*[@id="app"]/div[2]/main/div/div/div/div[1]/section[1]/div[1]/div/div[2]/div[2]/div[3]/button')
    add_to_cart.click()
    time.sleep(5)
    product2=driver.find_element(By.XPATH,'//*[@id="app"]/header/div/div[2]/div/input')
    product2.click()
    time.sleep(5)
    search2=driver.find_element(By.XPATH,'/html/body/div[2]/div/div[1]/div/div/div/div/div/div[1]/div/div/input')
    search2.send_keys('horlicks')
    select2=driver.find_element(By.XPATH,'/html/body/div[2]/div/div[1]/div/div/div/div/div/div[2]/div/div[1]/div/div[2]/div[1]/div[2]/a')
    select2.click()
    time.sleep(5)
    clear=driver.find_element(By.XPATH,'/html/body/div[2]/div/div[1]/div/div/div/div/div/div[1]/div/div/button')
    clear.click()
    time.sleep(5)
    search3=driver.find_element(By.XPATH,'/html/body/div[2]/div/div[1]/div/div/div/div/div/div[1]/div/div/input')
    search3.send_keys('zandu balm')
    time.sleep(5)
    select3=driver.find_element(By.XPATH,'/html/body/div[2]/div/div[1]/div/div/div/div/div/div[2]/div/div[1]/div/div[2]/div[2]/div[1]/p[1]')
    select3.click()
    time.sleep(5)
    add_to_cart=driver.find_element(By.XPATH,'//*[@id="app"]/div[2]/main/div/div/div/div[1]/section[1]/div[1]/div/div[2]/div[2]/div[3]/button')
    add_to_cart.click()
    time.sleep(5)
    
def cart_function(driver):
    view_cart=driver.find_element(By.XPATH,'//*[@id="shopping-cart-icn-36"]')
    view_cart.click()
    time.sleep(10)
    home=driver.find_element(By.XPATH,'//*[@id="app"]/div[2]/main/nav/ol/li[1]/span/a')
    home.click()
    time.sleep(5)

def store_finder(driver):
    store=driver.find_element(By.XPATH,'//*[@id="app"]/header/div/div[2]/a[2]')
    store.click()
    time.sleep(5)
    home=driver.find_element(By.XPATH,'//*[@id="app"]/div[2]/main/nav/ol/li[1]/span/a')
    home.click()
    time.sleep(5)
    
def log_out(driver):
    menu=driver.find_element(By.XPATH,'//*[@id="app"]/header/div/div[2]/div[3]/button')
    menu.click()
    time.sleep(5)
    exit=driver.find_element(By.XPATH,'//*[@id="app"]/header/div/div[2]/div[3]/div/button[13]')
    exit.click()
    time.sleep(5)

driver = setup_driver()
test_home_page_load(driver)
time.sleep(10)
login_function(driver)
time.sleep(10)
user_details(driver)
time.sleep(10)
medicine_search(driver)
time.sleep(5)
cart_function(driver)
time.sleep(5)
store_finder(driver)
time.sleep(10)
log_out(driver)
time.sleep(5)
