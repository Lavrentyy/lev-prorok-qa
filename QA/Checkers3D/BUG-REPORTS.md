\# Checkers 3D — Bug Reports



\## Bug Summary



| ID | Title | Severity | Priority | Status |

|---|---|---|---|---|

| BUG-001 | Player can skip a mandatory capture | Major | High | Open |

| BUG-002 | Player cannot control the subsequent path during multiple capture | Major | High | Open |



\---



\# BUG-001 — Player Can Skip a Mandatory Capture



\*\*Severity:\*\* Major

\*\*Priority:\*\* High

\*\*Status:\*\* Open

\*\*Type:\*\* Functional / Game Logic



\## Description



When a capture is available, the player is still able to choose a regular move instead of capturing the opponent's piece.



This allows the player to make a move that is not consistent with the mandatory capture rule.



\## Preconditions



\- A game is in progress.

\- The current player has an available capture.



\## Steps to Reproduce



1\. Start a game.

2\. Create a position where the current player can capture an opponent's piece.

3\. Select the player's piece.

4\. Choose a regular move instead of performing the available capture.



\## Expected Result



When a capture is available, the player should be forced to perform the capture and should not be able to make another regular move.



\## Actual Result



The player can skip the available capture and perform another move.



\## Impact



The defect allows players to perform moves that violate the intended game rules and can affect the outcome of the match.



\## Environment



\- \*\*Platform:\*\* Windows

\- \*\*Engine:\*\* Unreal Engine 5

\- \*\*Game Mode:\*\* Local Multiplayer

\- \*\*Players:\*\* 2



\---



\# BUG-002 — Player Cannot Control the Subsequent Path During Multiple Capture



\*\*Severity:\*\* Major

\*\*Priority:\*\* High

\*\*Status:\*\* Open

\*\*Type:\*\* Functional / Game Logic



\## Description



During a multiple capture, more than one continuation path can be available after a capture.



The player can choose the initial direction, but cannot choose the subsequent direction at each stage of the capture sequence. The remaining sequence is then performed automatically by the game.



\## Preconditions



\- A game is in progress.

\- The current player has a possible multiple capture.

\- After the initial capture, more than one continuation path is available.



\## Steps to Reproduce



1\. Start a game.

2\. Create a position where a multiple capture is possible.

3\. Perform the first capture.

4\. When multiple continuation directions are available, select one of them.

5\. Continue observing the capture sequence.



\## Expected Result



When multiple valid continuation paths are available, the player should be able to select the desired direction at each stage of the multiple capture.



\## Actual Result



The player can select the initial direction, but subsequent captures are performed automatically without allowing the player to choose the next direction.



\## Impact



The player loses control over the capture sequence. This can lead to an unintended capture path and an unexpected game outcome.



\## Environment



\- \*\*Platform:\*\* Windows

\- \*\*Engine:\*\* Unreal Engine 5

\- \*\*Game Mode:\*\* Local Multiplayer

\- \*\*Players:\*\* 2



\---



\# Bug Analysis



Both defects affect the core game logic.



\### BUG-001



The mandatory capture rule is not enforced when a capture is available.



\### BUG-002



The game does not provide player control over the complete multiple-capture decision path when multiple valid continuations exist.



Both defects can directly affect gameplay and therefore have \*\*Major severity\*\*.



\## Evidence



!\[BUG-001](screenshots/BUG-001-mandatory-capture.png)

!\[BUG-002](screenshots/BUG-002-mandatory-capture.png)

