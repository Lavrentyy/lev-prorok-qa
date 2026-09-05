\# Checkers 3D — Test Cases



\## Test Environment



| Parameter | Value |

|---|---|

| Project | Checkers 3D |

| Engine | Unreal Engine 5 |

| Platform | Windows |

| Game Mode | Local Multiplayer |

| Players | 2 |

| Testing Type | Manual / Functional |



\---



\## TC-001 — Game Launch



\*\*Priority:\*\* High

\*\*Type:\*\* Functional



\### Preconditions

The game application is installed on the PC.



\### Steps

1\. Launch the game.

2\. Wait for the game scene to load.



\### Expected Result

The game launches successfully and the game board is displayed.



\### Status

\*\*PASS\*\*



\---



\## TC-002 — Game Board Display



\*\*Priority:\*\* High

\*\*Type:\*\* Functional



\### Steps

1\. Launch the game.

2\. Wait for the game scene to load.



\### Expected Result

The game board and its elements are displayed correctly.



\### Status

\*\*PASS\*\*



\---



\## TC-003 — Player Piece Selection



\*\*Priority:\*\* High

\*\*Type:\*\* Functional



\### Steps

1\. Start a game.

2\. Select a piece belonging to the current player.



\### Expected Result

The selected piece can be used to perform a move.



\### Status

\*\*PASS\*\*



\---



\## TC-004 — Valid Piece Movement



\*\*Priority:\*\* High

\*\*Type:\*\* Functional



\### Steps

1\. Select a piece belonging to the current player.

2\. Select a valid destination cell.

3\. Perform the move.



\### Expected Result

The piece moves to the selected cell.



\### Status

\*\*PASS\*\*



\---



\## TC-005 — Turn Switching



\*\*Priority:\*\* High

\*\*Type:\*\* Functional



\### Steps

1\. Perform a valid move.

2\. Attempt to make another move.



\### Expected Result

The turn is passed to the second player.



\### Status

\*\*PASS\*\*



\---



\## TC-006 — Capturing an Opponent's Piece



\*\*Priority:\*\* High

\*\*Type:\*\* Functional



\### Steps

1\. Create a situation where an opponent's piece can be captured.

2\. Select the current player's piece.

3\. Perform the capture.



\### Expected Result

The current player's piece moves over the opponent's piece and the captured piece is removed from the board.



\### Status

\*\*PASS\*\*



\---



\## TC-007 — Invalid Movement



\*\*Priority:\*\* High

\*\*Type:\*\* Functional



\### Steps

1\. Select a piece belonging to the current player.

2\. Attempt to move it to an invalid cell.



\### Expected Result

The invalid move is rejected.



\### Status

\*\*TODO — Requires additional verification\*\*



\---



\## TC-008 — Mandatory Capture



\*\*Priority:\*\* High

\*\*Type:\*\* Functional



\### Preconditions

A capture is available.



\### Steps

1\. Select a piece that can capture an opponent's piece.

2\. Attempt to perform a regular move instead of the capture.



\### Expected Result

The player is forced to perform the available capture.



\### Actual Result

The player can choose not to capture and perform another move.



\### Status

\*\*FAIL\*\*



\*\*Related Bug:\*\* BUG-001



\---



\## TC-009 — Multiple Capture



\*\*Priority:\*\* High

\*\*Type:\*\* Functional



\### Steps

1\. Create a situation where multiple captures are possible.

2\. Perform the first capture.

3\. Continue the capture sequence.



\### Expected Result

The player can perform multiple captures during the same turn.



\### Status

\*\*PASS\*\*



\---



\## TC-010 — Multiple Capture Direction Selection



\*\*Priority:\*\* High

\*\*Type:\*\* Functional



\### Preconditions

After a capture, multiple continuation directions are available.



\### Steps

1\. Perform the first capture.

2\. Select one of the available directions.

3\. Continue the capture sequence.

4\. Check whether the player can select the next available direction.



\### Expected Result

The player can select the desired continuation path at each stage when multiple options are available.



\### Actual Result

After the initial direction is selected, the subsequent capture sequence is performed automatically. The player cannot select the next direction.



\### Status

\*\*FAIL\*\*



\*\*Related Bug:\*\* BUG-002



\---



\## TC-011 — Removal of Captured Pieces



\*\*Priority:\*\* High

\*\*Type:\*\* Functional



\### Steps

1\. Perform a capture.

2\. Observe the captured opponent's piece.



\### Expected Result

The captured piece is removed from the board.



\### Status

\*\*PASS\*\*



\---



\## TC-012 — Multiple Captured Pieces



\*\*Priority:\*\* High

\*\*Type:\*\* Functional



\### Steps

1\. Create a situation where several opponent pieces can be captured sequentially.

2\. Perform the capture sequence.

3\. Observe the captured pieces.



\### Expected Result

Each captured piece is removed from the board.



\### Status

\*\*PASS\*\*



\---



\## TC-013 — End of Capture Sequence



\*\*Priority:\*\* High

\*\*Type:\*\* Functional



\### Steps

1\. Perform a multiple capture.

2\. Complete the available capture sequence.

3\. Observe the game state.



\### Expected Result

The capture sequence ends and the turn is passed to the other player.



\### Status

\*\*TODO — Requires additional verification\*\*



\---



\## TC-014 — Game End After Last Piece Is Captured



\*\*Priority:\*\* Medium

\*\*Type:\*\* Functional



\### Steps

1\. Continue the game until one player loses all pieces.

2\. Capture the last remaining piece.



\### Expected Result

The game detects the end of the match and determines the winner.



\### Actual Result

The game continues without displaying a game-end state or winner.



\### Status

\*\*NOT IMPLEMENTED\*\*



\---



\## TC-015 — King Promotion



\*\*Priority:\*\* Medium

\*\*Type:\*\* Functional



\### Steps

1\. Move a regular piece to the opponent's final row.

2\. Observe the piece.



\### Expected Result

The piece is promoted to a king according to the game rules.



\### Actual Result

The piece remains a regular piece.



\### Status

\*\*NOT IMPLEMENTED\*\*



\# Test Summary



\### Total Test Cases: 15



| Status | Count |

|---|---:|

| PASS | 8 |

| FAIL | 2 |

| TODO | 2 |

| NOT IMPLEMENTED | 3 |



\### Failed Test Cases



\- \*\*TC-008\*\* — Mandatory Capture

\- \*\*TC-010\*\* — Multiple Capture Direction Selection



\### Not Implemented



\- \*\*TC-014\*\* — Game End After Last Piece Is Captured

\- \*\*TC-015\*\* — King Promotion

\- Game restart functionality



\### Requires Additional Verification



\- \*\*TC-007\*\* — Invalid Movement

\- \*\*TC-013\*\* — End of Capture Sequence

