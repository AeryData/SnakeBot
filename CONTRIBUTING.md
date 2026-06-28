# Contributing to SnakeBot

Thank you for your interest in contributing to SnakeBot! We appreciate your help in making this project better.

---

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How to Contribute](#how-to-contribute)
- [Development Setup](#development-setup)
- [Coding Standards](#coding-standards)
- [Pull Request Process](#pull-request-process)
- [Reporting Issues](#reporting-issues)
- [Contact & Support](#contact--support)

---

## Code of Conduct

By participating in this project, you agree to:
- Be respectful and inclusive to all contributors
- Focus on constructive feedback
- Report harassment or inappropriate behavior
- Follow all applicable laws and regulations

---

## How to Contribute

### 1. **Report a Bug**
If you find a bug, please open an issue with:
- A clear, descriptive title
- Steps to reproduce the problem
- Expected vs. actual behavior
- Your environment (Python version, OS, etc.)

### 2. **Suggest an Enhancement**
We love feature requests! Please include:
- Use case and motivation
- Proposed implementation approach (if you have ideas)
- Alternative solutions considered

### 3. **Submit Code Changes**
- Fork the repository
- Create a feature branch (`git checkout -b feature/YourFeatureName`)
- Make your changes following our coding standards
- Commit with clear messages
- Push and open a Pull Request

### 4. **Improve Documentation**
- Update README.md for clarity
- Add docstrings to new functions
- Create tutorials or guides for complex features

---

## Development Setup

### Prerequisites
- Python 3.x
- pip

### Local Setup
```bash
# Clone the repository
git clone https://github.com/AeryData/SnakeBot.git
cd SnakeBot

# Install dependencies
pip install pygame

# Run the game
python robo_snake.py
```

### Testing Your Changes
Always test your code before submitting a PR:
```bash
python robo_snake.py  # Visual testing
```

---

## Coding Standards

### Python Style Guide
- Follow **PEP 8** style guidelines
- Use descriptive variable and function names
- Write clear comments for complex logic
- Keep functions focused and modular

### Example:
```python
def is_tail_inside(self, virtual_board):
    """
    Verify if the snake's tail is reachable from its head position.
    
    Args:
        virtual_board: Simulated board state for testing
        
    Returns:
        bool: True if tail is reachable, False otherwise
    """
    # Implementation here
    pass
```

### Documentation
- Add docstrings to all classes and methods
- Update README.md if adding new features
- Include examples for complex functionality

---

## Pull Request Process

1. **Create a descriptive title**: Reference issue numbers when applicable
   - ✅ `Add genetic algorithm optimization for AI decision making (#42)`
   - ❌ `fix stuff`

2. **Write a clear description**:
   - What problem does this solve?
   - How does it work?
   - Any breaking changes?

3. **Ensure your code**:
   - Follows PEP 8 standards
   - Doesn't introduce new dependencies without discussion
   - Includes appropriate comments/documentation

4. **Link related issues**: Use "Closes #issue-number" in PR description

5. **Be responsive**: Engage with reviewers on feedback

### PR Template
```markdown
## Description
Brief explanation of changes

## Related Issue
Closes #(issue number)

## Changes Made
- Change 1
- Change 2
- Change 3

## Testing
How was this tested?

## Screenshots/Demo
(If applicable)
```

---

## Reporting Issues

### Before Submitting
- Search existing issues to avoid duplicates
- Check the documentation
- Try the latest code version

### Issue Template
```markdown
## Description
Clear explanation of the problem

## Environment
- Python version: 3.x
- OS: Windows/macOS/Linux
- Pygame version: x.x.x

## Steps to Reproduce
1. Step 1
2. Step 2
3. See error...

## Expected Behavior
What should happen?

## Actual Behavior
What actually happens?

## Additional Context
Screenshots, error logs, etc.
```

---

## Project Areas

### AI Improvements 🧠
- Machine learning implementations
- Genetic algorithms
- Neural network-based pathfinding
- Performance optimizations

### Features 🎮
- New game modes
- Multiplayer options
- Difficulty settings
- Statistics tracking

### Code Quality 🔧
- Performance improvements
- Refactoring
- Test coverage
- Documentation

### Documentation 📚
- Tutorials
- Architecture guides
- API documentation
- Video walkthroughs

---

## Branch Naming Convention

Use descriptive branch names:
- `feature/neural-network-ai` for new features
- `bugfix/collision-detection` for bug fixes
- `docs/update-readme` for documentation
- `refactor/optimize-pathfinding` for refactoring

---

## Commit Message Guidelines

```
[type] Brief description (50 chars max)

More detailed explanation if needed. Wrap at 72 characters.
Reference issues with #number when applicable.

[types]: feat, fix, docs, style, refactor, test, chore
```

Examples:
```
feat: Add minimax algorithm for AI decision making
fix: Resolve snake head collision detection bug
docs: Add neural network architecture explanation
refactor: Improve BFS performance with caching
```

---

## Contact & Support

### Get Help
- 💬 Open an issue with tag `question`
- 🤝 Join community discussions
- 📧 Email [AeryData](https://github.com/AeryData)
- 🏢 Contact [GMBSells Organization](https://github.com/gmbsells)

### Community Resources
- 📖 [SnakeBot Documentation](README.md)
- 🐍 [Python Official Docs](https://docs.python.org/)
- 🎮 [Pygame Documentation](https://www.pygame.org/docs/)
- 🧠 [Algorithm References](https://en.wikipedia.org/wiki/Breadth-first_search)

---

## Recognition

Contributors will be recognized in:
- README.md Contributors section
- Release notes
- Special mentions

---

## Questions?

Feel free to ask! We're here to help. Open an issue or reach out to:
- **GitHub**: [AeryData](https://github.com/AeryData)
- **Organization**: [GMBSells](https://github.com/gmbsells)

---

<div align="center">

**Thank you for contributing to SnakeBot! 🙏**

**Together, we're building smarter AI! 🤖✨**

</div>
