
# Rapport

Först skapades tre olika komponenter i activity_main.xml: EditText, Button och TextView. 

Dessa omslöts i en LinearLayout med en vertical orientation. För att få ett indrag med 16 punkter från kanterna användes padding attributen som tilldelades värdet 16dp. 

Efter det initierades komponenterna som tidigare skapades i xml-filen, som privata variabler i main activity java-filen.

```
private EditText editText;
private Button buttonDisplayText;
private TextView textView;
```

Dessa populerades därefter genom funktionen `findById()`:

```
editText = findViewById(R.id.edit_text);
buttonDisplayText = findViewById(R.id.button_display_text);        
textView = findViewById(R.id.final_text_view);
```


För att knappen ska uppdatera texten i TextViewen behöver den lyssna på att användaren klickar på den. Detta implementerades med koden nedan: 

```
buttonDisplayText.setOnClickListener(new View.OnClickListener() {
    @Override
    public void onClick(View view) {
        textView.setText(editText.getText());
    }
});
```

När användaren trycker på knappen uppdateras texten i TextViewen med värdet i EditText.
