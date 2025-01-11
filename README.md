# Number Guessing Game

C# console game where players guess a randomly generated number.

## Features
- Random number generation
- Difficulty levels
- Score tracking
- Hint system
- Game statistics

## Implementation
```csharp
public class GuessingGame
{
    private readonly Random _random = new();
    private int _targetNumber;
    private int _attempts;
    
    public void StartNewGame(Difficulty difficulty)
    {
        _targetNumber = GenerateNumber(difficulty);
        _attempts = 0;
    }
    
    public GuessResult CheckGuess(int guess)
    {
        _attempts++;
        if (guess == _targetNumber) return GuessResult.Correct;
        return guess < _targetNumber ? GuessResult.TooLow : GuessResult.TooHigh;
    }
}
```

## Structure
```
GuessingNumberGame/
├── Program.cs
├── GuessingGame.cs
├── Enums/
│   ├── Difficulty.cs
│   └── GuessResult.cs
└── Models/
    └── GameStats.cs
```

## Features
- Multiple difficulty levels
- Attempt tracking
- High score system
- Hint mechanism
- Progress statistics

## Usage
```bash
dotnet run
```

## License
MIT License
