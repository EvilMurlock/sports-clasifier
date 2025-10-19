Odevzdání úloh v rámci žádosti o pozici AI trainee

Autor: Samuel Juraj Koprda

---Generování reportu z odehraného zápasu---
Řešení této úlohy naleznete v dokumentu "Generování reportu z odehraného zápasu.pdf"
Dokončení této úlohy mi zabralo 30 minut


---Vytvořte klasifikátor textů---
Kód této úlohy je uložen ve formě jupiter notebooku v souboru "klasifikátor zpráv.ipynb". Použitý python virtual environment je v souboru ".venv"
Finální model je: "sports_model_finetuned"
F1 scére modelu je: 0.868

Čas strávený nad úlohou: ~15 hodin

Model jsem trénoval několikrát s různými parametry abych našle nejlepší řešení.
Pokud vynecháme čekání na trénink a budeme počítat pouze čas strávený debugováním,
psaním kódu a čtením dokumentací etc. tak je čas strávený nad úlohou ~4 hodin.

Klasifikační model používá předtrénovaný model "bert" z Hugging Face "transformers" libary, na který jsem zavěsil vlastní klasifikační vrstvu s jednou skrytou vrstvou.
Model nejprve 5 epoch trénuje hlavu, a poté 5 epoch finetuninguje celý model.
Zkoušel jsem různé kombinace parametrů, vyžší learning rate než je nyní směřoval k overfitingu (přetrénování).
5 a 5 epoch u mě trvá natrénovat 1.5 hodin, takže jsem více epoch nezkoušel, výsledek by se pravděpodobně ještě chvíli zlepšoval, ale ne o moc. 3 a 3 epochy měli f1 scóre 0.845, což je relativně malý rozdíl.
