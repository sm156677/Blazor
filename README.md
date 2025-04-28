# Blazor

Wie erstelle ich eine Blazor Webassembly(wasm) app mit Beispielcode:

Um eine Blazor WebAssembly (WASM) App zu erstellen, folgen Sie diesen Schritten:

1. .NET SDK installieren
Stellen Sie sicher, dass das .NET SDK installiert ist. Überprüfen Sie dies mit dem folgenden Befehl im Terminal:

dotnet --version

Falls nicht installiert, laden Sie das SDK von der offiziellen Microsoft .NET-Website herunter.

2. Neues Blazor WebAssembly-Projekt erstellen
Führen Sie den folgenden Befehl im Terminal aus, um ein neues Blazor WebAssembly-Projekt zu erstellen:

dotnet new blazorwasm -o BlazorApp --no-https

blazorwasm: Vorlage für eine Blazor WebAssembly App.
-o BlazorApp: Erstellt ein Verzeichnis namens BlazorApp für das Projekt.
3. Projektverzeichnis betreten
Wechseln Sie in das neu erstellte Projektverzeichnis:

cd BlazorApp

4. Projekt starten
Starten Sie die Anwendung mit:

dotnet run

Die Anwendung wird standardmäßig unter http://localhost:5000 oder https://localhost:5001 verfügbar sein.

5. Beispielcode hinzufügen
Öffnen Sie die Datei Pages/Index.razor und fügen Sie Beispielcode hinzu. Zum Beispiel:

@page "/"

<h1>Hallo Blazor!</h1>

<p>Dies ist eine einfache Blazor WebAssembly App.</p>

<button @onclick="KlickMich">Klick mich!</button>

<p>@nachricht</p>

@code {
    private string nachricht = "Noch kein Klick.";

    private void KlickMich()
    {
        nachricht = "Button wurde geklickt!";
    }
}

6. Änderungen anzeigen
Speichern Sie die Datei und aktualisieren Sie die Webseite im Browser, um die Änderungen zu sehen.
