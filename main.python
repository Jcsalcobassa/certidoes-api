from fastapi import FastAPI, HTTPException
from pydantic import BaseModel
from selenium import webdriver
from selenium.webdriver.chrome.service import Service
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC

app = FastAPI()

class CertidaoRequest(BaseModel):
    documento: str  # CPF ou CNPJ

def certidao_debitos(driver, documento):
    driver.get("https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-de-debitos")
    wait = WebDriverWait(driver, 10)
    wait.until(EC.presence_of_element_located((By.ID, "cpf_cnpj"))).clear()
    driver.find_element(By.ID, "cpf_cnpj").send_keys(documento)
    wait.until(EC.element_to_be_clickable((By.ID, "btnConsultar"))).click()
    resultado = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, ".resultado"))).text
    return resultado

def certidao_negativa_debitos(driver, documento):
    driver.get("https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-negativa-de-debitos")
    wait = WebDriverWait(driver, 10)
    wait.until(EC.presence_of_element_located((By.ID, "cpf_cnpj"))).clear()
    driver.find_element(By.ID, "cpf_cnpj").send_keys(documento)
    wait.until(EC.element_to_be_clickable((By.ID, "btnConsultar"))).click()
    resultado = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, ".resultado"))).text
    return resultado

def certidao_regularidade_fiscal(driver, documento):
    driver.get("https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-de-regularidade-fiscal")
    wait = WebDriverWait(driver, 10)
    wait.until(EC.presence_of_element_located((By.ID, "cpf_cnpj"))).clear()
    driver.find_element(By.ID, "cpf_cnpj").send_keys(documento)
    wait.until(EC.element_to_be_clickable((By.ID, "btnConsultar"))).click()
    resultado = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, ".resultado"))).text
    return resultado

def certidao_distribuicao(driver, documento):
    driver.get("https://www.tjsp.jus.br/CertidaoDistribuicao")
    wait = WebDriverWait(driver, 10)
    wait.until(EC.presence_of_element_located((By.ID, "cpf_cnpj"))).clear()
    driver.find_element(By.ID, "cpf_cnpj").send_keys(documento)
    wait.until(EC.element_to_be_clickable((By.ID, "btnConsultar"))).click()
    resultado = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, ".resultado"))).text
    return resultado

def certidao_protesto(driver, documento):
    driver.get("https://www.protesto.com.br/certidao")
    wait = WebDriverWait(driver, 10)
    wait.until(EC.presence_of_element_located((By.ID, "cpf_cnpj"))).clear()
    driver.find_element(By.ID, "cpf_cnpj").send_keys(documento)
    wait.until(EC.element_to_be_clickable((By.ID, "btnConsultar"))).click()
    resultado = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, ".resultado"))).text
    return resultado

def certidao_acoes_trabalhistas(driver, documento):
    driver.get("https://www.trt1.jus.br/consultas/certidao")
    wait = WebDriverWait(driver, 10)
    wait.until(EC.presence_of_element_located((By.ID, "cpf_cnpj"))).clear()
    driver.find_element(By.ID, "cpf_cnpj").send_keys(documento)
    wait.until(EC.element_to_be_clickable((By.ID, "btnConsultar"))).click()
    resultado = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, ".resultado"))).text
    return resultado

def certidao_acoes_civeis(driver, documento):
    driver.get("https://www.tjsp.jus.br/CertidaoAcoesCiveis")
    wait = WebDriverWait(driver, 10)
    wait.until(EC.presence_of_element_located((By.ID, "cpf_cnpj"))).clear()
    driver.find_element(By.ID, "cpf_cnpj").send_keys(documento)
    wait.until(EC.element_to_be_clickable((By.ID, "btnConsultar"))).click()
    resultado = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, ".resultado"))).text
    return resultado

def certidao_inexistencia_debitos(driver, documento):
    driver.get("https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-inexistencia-de-debitos")
    wait = WebDriverWait(driver, 10)
    wait.until(EC.presence_of_element_located((By.ID, "cpf_cnpj"))).clear()
    driver.find_element(By.ID, "cpf_cnpj").send_keys(documento)
    wait.until(EC.element_to_be_clickable((By.ID, "btnConsultar"))).click()
    resultado = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, ".resultado"))).text
    return resultado

def certidao_fgts(driver, documento):
    driver.get("https://www.gov.br/fgts/pt-br/consultas/certidao")
    wait = WebDriverWait(driver, 10)
    wait.until(EC.presence_of_element_located((By.ID, "cpf_cnpj"))).clear()
    driver.find_element(By.ID, "cpf_cnpj").send_keys(documento)
    wait.until(EC.element_to_be_clickable((By.ID, "btnConsultar"))).click()
    resultado = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, ".resultado"))).text
    return resultado

def certidao_inss(driver, documento):
    driver.get("https://www.gov.br/inss/pt-br/consultas/certidao")
    wait = WebDriverWait(driver, 10)
    wait.until(EC.presence_of_element_located((By.ID, "cpf_cnpj"))).clear()
    driver.find_element(By.ID, "cpf_cnpj").send_keys(documento)
    wait.until(EC.element_to_be_clickable((By.ID, "btnConsultar"))).click()
    resultado = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, ".resultado"))).text
    return resultado

def certidao_simples_nacional(driver, documento):
    driver.get("https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-simples-nacional")
    wait = WebDriverWait(driver, 10)
    wait.until(EC.presence_of_element_located((By.ID, "cpf_cnpj"))).clear()
    driver.find_element(By.ID, "cpf_cnpj").send_keys(documento)
    wait.until(EC.element_to_be_clickable((By.ID, "btnConsultar"))).click()
    resultado = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, ".resultado"))).text
    return resultado

def certidao_icms(driver, documento):
    driver.get("https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-icms")
    wait = WebDriverWait(driver, 10)
    wait.until(EC.presence_of_element_located((By.ID, "cpf_cnpj"))).clear()
    driver.find_element(By.ID, "cpf_cnpj").send_keys(documento)
    wait.until(EC.element_to_be_clickable((By.ID, "btnConsultar"))).click()
    resultado = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, ".resultado"))).text
    return resultado

def certidao_iss(driver, documento):
    driver.get("https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-iss")
    wait = WebDriverWait(driver, 10)
    wait.until(EC.presence_of_element_located((By.ID, "cpf_cnpj"))).clear()
    driver.find_element(By.ID, "cpf_cnpj").send_keys(documento)
    wait.until(EC.element_to_be_clickable((By.ID, "btnConsultar"))).click()
    resultado = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, ".resultado"))).text
    return resultado

def certidao_ipva(driver, documento):
    driver.get("https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-ipva")
    wait = WebDriverWait(driver, 10)
    wait.until(EC.presence_of_element_located((By.ID, "cpf_cnpj"))).clear()
    driver.find_element(By.ID, "cpf_cnpj").send_keys(documento)
    wait.until(EC.element_to_be_clickable((By.ID, "btnConsultar"))).click()
    resultado = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, ".resultado"))).text
    return resultado

def certidao_itr(driver, documento):
    driver.get("https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-itr")
    wait = WebDriverWait(driver, 10)
    wait.until(EC.presence_of_element_located((By.ID, "cpf_cnpj"))).clear()
    driver.find_element(By.ID, "cpf_cnpj").send_keys(documento)
    wait.until(EC.element_to_be_clickable((By.ID, "btnConsultar"))).click()
    resultado = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, ".resultado"))).text
    return resultado

def certidao_cadastro_nacional(driver, documento):
    driver.get("https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-cadastro-nacional")
    wait = WebDriverWait(driver, 10)
    wait.until(EC.presence_of_element_located((By.ID, "cpf_cnpj"))).clear()
    driver.find_element(By.ID, "cpf_cnpj").send_keys(documento)
    wait.until(EC.element_to_be_clickable((By.ID, "btnConsultar"))).click()
    resultado = wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, ".resultado"))).text
    return resultado

@app.post("/certidoes")
def certidoes(request: CertidaoRequest):
    # Inicializa o driver do Selenium
    service = Service()
    options = webdriver.ChromeOptions()
    driver = webdriver.Chrome(service=service, options=options)
    wait = WebDriverWait(driver, 10)

    resultados = {}

    try:
        resultados["Certidão de Débitos"] = certidao_debitos(driver, request.documento)
        resultados["Certidão Negativa de Débitos"] = certidao_negativa_debitos(driver, request.documento)
        resultados["Certidão de Regularidade Fiscal"] = certidao_regularidade_fiscal(driver, request.documento)
        resultados["Certidão de Distribuição"] = certidao_distribuicao(driver, request.documento)
        resultados["Certidão de Protesto"] = certidao_protesto(driver, request.documento)
        resultados["Certidão de Ações Trabalhistas"] = certidao_acoes_trabalhistas(driver, request.documento)
        resultados["Certidão de Ações Cíveis"] = certidao_acoes_civeis(driver, request.documento)
        resultados["Certidão de Inexistência de Débitos"] = certidao_inexistencia_debitos(driver, request.documento)
        resultados["Certidão de Regularidade do FGTS"] = certidao_fgts(driver, request.documento)
        resultados["Certidão de Regularidade do INSS"] = certidao_inss(driver, request.documento)
        resultados["Certidão de Regularidade do Simples Nacional"] = certidao_simples_nacional(driver, request.documento)
        resultados["Certidão de Regularidade do ICMS"] = certidao_icms(driver, request.documento)
        resultados["Certidão de Regularidade do ISS"] = certidao_iss(driver, request.documento)
        resultados["Certidão de Regularidade do IPVA"] = certidao_ipva(driver, request.documento)
        resultados["Certidão de Regularidade do ITR"] = certidao_itr(driver, request.documento)
        resultados["Certidão de Cadastro Nacional"] = certidao_cadastro_nacional(driver, request.documento)
    except Exception as e:
        raise HTTPException(status_code=500, detail=str(e))
    finally:
        driver.quit()

    return {"status": "ok", "dados": resultados}
