// C++ code
//

int ativado = 0;
int LeituraPIR = 0;
int const PIR = 8;
const int buzzer = 5;
const int Led = 7;

void setup()
{
  pinMode(Led, OUTPUT);
  pinMode(buzzer, OUTPUT);
  pinMode(PIR, INPUT);
  
  Serial.begin(9600);
}

void loop()
{
  LeituraPIR = digitalRead(PIR);
  Serial.print("Valor do Sensor PIR: ");
  Serial.print(LeituraPIR);
   Serial.print(" Sistema Ativado? ");
  Serial.println(ativado);
  int botao = digitalRead(6);
  
  if(botao == HIGH && ativado == 0){
	ativado = 1;
    delay(1500);
  }else if(botao == HIGH && ativado == 1){
    ativado = 0;
    delay(1500);
  }
  
  if(ativado == 1 && LeituraPIR == 1){
   digitalWrite(Led, HIGH);
    tone(buzzer, 700);
    delay(500);
    digitalWrite(Led, LOW);
    noTone(buzzer);
    delay(250);
  }
  
}
