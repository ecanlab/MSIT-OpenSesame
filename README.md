# Multi-Source Interference Task (MSIT)

An OpenSesame implementation of the Multi-Source Interference Task (MSIT), designed to measure cognitive interference and attentional control during functional magnetic resonance imaging (fMRI).

## Task Description

Participants are presented with three digits (0, 1, 2, or 3), where one digit differs from the other two. The objective is to identify the unique digit (1, 2, or 3) using the corresponding response button, regardless of its position.

The task consists of two conditions:

- **Control:** The target digit appears in its corresponding position, while the remaining digits are zeros (e.g., `100`, `020`, `003`).
- **Interference:** The target digit appears in a position that does not correspond to its value, and the distractors are nonzero digits (e.g., `212`, `311`).

The task is designed to induce cognitive interference by introducing conflict between the target digit, its position, and the surrounding distractors.

## Language

The experiment contains Swedish text, including participant instructions.

## Task Duration

The task consists of four control blocks and four interference blocks, each lasting 42 seconds and containing 24 trials. Each trial lasts 1,750 ms.

A fixation dot is presented for 15 seconds at the beginning and end of the task.

The total duration is approximately 6 minutes and 6 seconds.

## Hardware

- [NordicNeuroLab SyncBox](https://github.com/nordicneurolab)
- [Black Box Toolkit USB TTL](https://www.blackboxtoolkit.com/usbttl.html)

## Configuration

The experiment can be configured to run with or without MRI-compatible response hardware. The following settings control the available input devices and experimental conditions.

| Setting        | Default | Description                                                |
| -------------- | ------- | ---------------------------------------------------------- |
| `ttl`          | `True`  | Enables TTL trigger communication.                         |
| `syncbox`      | `True`  | Enables the NordicNeuroLab SyncBox.                        |
| `controll`     | `True`  | Enables the control condition.                             |
| `interference` | `True`  | Enables the interference condition.                        |
| `use_keyboard` | `False` | Uses keyboard input instead of the SyncBox response grips for testing outside the MRI environment |
