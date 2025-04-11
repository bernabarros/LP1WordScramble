```mermaid

---
title: WordScramble
---
classDiagram

class WordProvider{
    -List words
    -Random random
    +string GetRandomWord()
    +string GetScrambledWord()
    }
Game -->"1"WordProvider
Game -->"1"GameResults
class Game{
    -WordProvider wordProvider;
    -GameResult[] gameStats;
    +void ShowMenu()
    -void StartGame()
    -void ShowGameStats()
}

class GameResults{
    +string Word
    +double TimeTaken
}
Program..>Game
class Program{
    -void Main()
}