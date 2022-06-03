# Objetos-Inteligentes
Codigo do trabalho

//definição do pino de saída do sensor PIR 
#define PIN_SENSOR 24
//definição do pino de entrada do Buzzer
#define PIN_BUZZER 22
void setup() {
Serial.begin(9600);
  //abaixo vamos confirar cada um dos pinos como entrada ou saída de dados
  pinMode(PIN_SENSOR, INPUT);
  pinMode(PIN_BUZZER, OUTPUT);
}
void loop() { 

  //faz a leitura do sensor de presença (retorna HIGH ou LOW)
  int sinal = digitalRead(PIN_SENSOR); 
Serial.println(sinal);
  //HIGH : movimento detectado
  if(sinal == HIGH){
    //aciona o Buzzer
    digitalWrite(PIN_BUZZER, HIGH);
  }
  //LOW : nenhum movimento detectado
  else{
    //desativa o buzzer
    digitalWrite(PIN_BUZZER, LOW);
  }

}
