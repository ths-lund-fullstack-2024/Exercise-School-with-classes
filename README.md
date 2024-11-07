# Exercise School with classes

Denna uppgift är identiskt med den förra skoluppgiften fast ni ska ni skapa den med klasser istället.

Ni ska skapa en skola, som kommer att innehålla lärare som undervisar i kurser som läses utav studenter, så lite olika klasser innehållandes olika typer av egenskaper och även metoder för att de olika typer av klasser ska kunna interagera med varandra.

Ni kan välja att skriva allt i en och samma js-fil eller så ka ni använda import-syntaxen men då måste ni använda modul-attributet på den filen som läses in i er index.html.

```js
<script src="index.js" type="module"></script>
```

1. Börja med att skapa en skola som en klass. Skolan ska innehålla egenskaperna: name, address, zipcode, city, students med värdet av en tom array och teachers som en tom array. Skapa sen en instans av klassen med ett namn som du väljer.

```js
class School {
  constructor(name) {
    this.name = name;
    this.students = [];
    this.teachers = [];
    /* skolans övriga egenskaper ß*/
  }
}
```

2. Skapa tre stycken olika ämnen. För att göra det så behöver du en klass för ämne. Ett ämne ska ha name, students som en tom array och teacher som null till en början.

```js
class Subject = {
  /* ämnets egenskaper här */
};
```

3.  Skapa en klass för `Student` och sen fem instanser av den klassen. Egenskaperna ska vara name, age och subjects som en tom array.

4.  Skapa en klass i `Teacher` där egenskaperna är name och subjects som en tom array.

5.  Skapa en metod i `Teacher` som lägger till ett ämne i en lärares ämnesarray.

6.  Skapa en metod i `Subject` som lägger till en `Student` i ett ämnes studentarray.

7.  Som tidigare så ska vi lägga till en koppling på båda sidorna när vi lägger till saker. Ska vi till exempel lägga till en ett ämne som en lärare utbildar i så måste vi lägga till en referens till ämnet i lärarens ämnesarray och en referens till läraren i ämnesklassen.

    Då har vi en referens på båda sidorna.

    **Egentligen är detta något som kallas för en cirkulär referens vilket vi helst vill undvika när vi programmerar, då kan orsaka krashar i vissa fall, men i syftet för uppgiften så är det ingen fara.**

    Skapa nu en fristående funktion som heter _addSubjectToTeacher_ som tar emot ett ämne och en lärare, och parar ihop dessa. Returnera sen läraren så du kan se förändringen i lärarens ämnesarray.

8.  Varför ha en fristående funktion som lägger till ämne till en lärare? Varför inte bara lägga till en funktion (alltså en metod eftersom funktionen då är kopplad till ett specifikt objekt) i lärarnas objekt som en egenskap? Prova denna nya metod i konsolen.

9.  Skapa följande metoder och lägg in de i rätt klass: _addTeacher_, _enlistToSubject_, _addStudent_, _addSubject_.

10. Prova att leka runt med alla de skapade metoderna i konsolen och försöka lägga till i de olika instanserna. Skriv ut instansen hela tiden och inspektera dem. Tänk dig nu ett adminprogram för en skola där en admin till exempel skriver ut en lista på alla ämnen för att se vilka respektive lärare som är ansvariga för respektive kurs. Klasser och metoder som vi har skapat hittils skulle kunna existera i ett sådant program.

11. Skapa fler metoder, _quitSubject_, _removeTeacher_, _relegateStudent_, _fireTeacher_. I vilka klasser hör dessa metoder hemma? Och om vi till exempel sparkar en lärare, så måste vi ju ta bort lärarens koppling med skolan, och ämnet/ämnerna som läraren undervisar i. Hur löser vi detta i våra metoder, nu får vi börja tänka oss för lite.

12. Lek runt med dessa metoder i konsolen. Lägg till lite här och ta bort lite där. Rätt smidigt va?

13. Ny bygger vi på det lite. För att undvika att behöva anropa massa metoder i konsolen när vi startar om programmet (vilket händer vid varje redigering av script-filen) så kan vi längst ner i script-filen skapa _( alltså den koden läses in sist hela tiden )_ logik för att koppla några studenter till skolan, några ämnen till studenterna och några lärare till ämnena och så vidare. Skapa sån logik nu.

14. Skapa en fristående funktion _displayAllStudents_ som tar emot en skola och loopar igenom skolans alla studenter och skriver ut alla studenterna i konsolen.

15. Skapa nu fler fristående funktioner, _displayAllSubjectsOfStudent(student)_, _displayAllStudentsEnlistedToSubject(subject)_, _displayAllTeachers_. Varje funktion bör ha något returvärde.

16. Bygg ut med ett ytterligare typ av klasser, lägg till klass som handlar om betyg. Vilka egenskaper ska dessa ha? Vilka metoder kan behövas i denna betygsklass? Hur ska relationen mellan de andra klasserna vara? Vilka metoder bör finnas i de andra typerna av klasser som behandlar betyg? Försöka lösa detta och inspektera och lek runt med det i konsolen.
