# workspace

MATLAB workspace-management utilities.

Part of the Prerau Lab [`utils`](https://github.com/preraulab/utils) meta-repository. Can also be used standalone.

## When to use which

| Task | Use |
|---|---|
| Clear all / close all figures / clear command window | `ccc` |
| Clear all variables *except* a specified list | `clear_all_except` |
| Bundle a function + every file it calls into a folder | `packagecode` |

> ⚠️ `ccc` mutates the caller's workspace and closes figures. Intended for interactive sessions, not scripts or functions that other code depends on.

## Examples

```matlab
% At top of an interactive script
ccc;

% Keep two variables while clearing the rest
clear_all_except({'data', 'Fs'});

% Package a function + all its dependencies
packagecode('my_analysis', './my_analysis_pkg');
```

## Function list

`ccc`, `clear_all_except`, `packagecode`

See `help <function>` at the MATLAB prompt for the full docstring of each.

## Install

```matlab
addpath('/path/to/workspace');
```

## Dependencies

MATLAB R2020a+. No required toolboxes.

## License

BSD 3-Clause. See [`LICENSE`](LICENSE).
