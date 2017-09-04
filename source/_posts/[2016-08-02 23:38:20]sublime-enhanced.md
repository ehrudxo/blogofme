---
title: "sublime-enhanced"
date: 2016-08-02 23:38:20
tags: github, github-trend, tech-trend 
---


sublime Text 의 플러그인들의 모음입니다.

2016/08/02 Editor's choice

[**shagabutdinov/sublime-enhanced**  
_sublime-enhanced - Set of plugins for beloved sublime text editor_github.com][anchor0][][anchor1]

gh-ost 를 리뷰할 생각이었으나 gh-ost는 앞으로 며칠간 수위권을 장식할 예정이라 간단하게 플러그인들의 모음을 모아 놓은 사이트만 공유합니다.

3가지의 목표를 가지고 만든 프로젝트입니다.

1. Mouseless usage of sublime
2. Navigation (in code and files) improvement
3. Common micro-tasks automation

마우스 없이 쓰고 코드와 파일간을 쉽게 컨트롤 하고 공통적으로 행해지는 작업들을 자동화 한다는 군요.

데모로 보이는 페이지에는 method를 작성하면 기본적으로 skeleton 코드를 만들어 주는

[**shagabutdinov/sublime-method**  
_sublime-method - Sublime plugin that allows to manipulate methods in file_github.com][anchor2][][anchor3]

프로젝트로 시작해 아래와 같이 많은 프로젝트들을 기본 세팅해서 사용할 수 있습니다.
    
    git clone git@github.com:shagabutdinov/sublime-align-cursors.git AlignCursors;  
    git clone git@github.com:shagabutdinov/sublime-align-hash-table.git AlignHashTable;  
    git clone git@github.com:shagabutdinov/sublime-append-selection.git AppendSelection;  
    git clone git@github.com:shagabutdinov/sublime-autocompletion.git Autocompletion;  
    git clone git@github.com:shagabutdinov/sublime-clone-file.git CloneFile;  
    git clone git@github.com:shagabutdinov/sublime-close-other.git CloseOther;  
    git clone git@github.com:shagabutdinov/sublime-context.git Context;  
    git clone git@github.com:shagabutdinov/sublime-devastate-mini.git DevastateMini;  
    git clone git@github.com:shagabutdinov/sublime-duplicate-lines-enhanced.git DuplicateLinesEnhanced;  
    git clone git@github.com:shagabutdinov/sublime-eval-selection.git EvalSelection;  
    git clone git@github.com:shagabutdinov/sublime-delayed-save-all.git DelayedSaveAll;  
    git clone git@github.com:shagabutdinov/sublime-expression.git Expression;  
    git clone git@github.com:shagabutdinov/sublime-file-dialog.git FileDialog;  
    git clone git@github.com:shagabutdinov/sublime-file-list.git FileList;  
    git clone git@github.com:shagabutdinov/sublime-file-util.git FileUtil;  
    git clone git@github.com:shagabutdinov/sublime-folder-files.git FolderFiles;  
    git clone git@github.com:shagabutdinov/sublime-full-undo.git FullUndo;  
    git clone git@github.com:shagabutdinov/sublime-goto-anything-enhanced.git GotoAnythingEnhanced;  
    git clone git@github.com:shagabutdinov/sublime-goto-character.git GotoCharacter;  
    git clone git@github.com:shagabutdinov/sublime-goto-definition-enhanced.git GotoDefinitionEnhanced;  
    git clone git@github.com:shagabutdinov/sublime-goto-last-edit-enhanced.git GotoLastEditEnhanced;  
    git clone git@github.com:shagabutdinov/sublime-goto-line-enhanced.git GotoLineEnhanced;  
    git clone git@github.com:shagabutdinov/sublime-indentation-navigation.git IndentationNavigation;  
    git clone git@github.com:shagabutdinov/sublime-join-assignment.git JoinAssignment;  
    git clone git@github.com:shagabutdinov/sublime-join-chain-call.git JoinChainCall;  
    git clone git@github.com:shagabutdinov/sublime-join-lines-enhanced.git JoinLinesEnhanced;  
    git clone git@github.com:shagabutdinov/sublime-join-statement.git JoinStatement;  
    git clone git@github.com:shagabutdinov/sublime-keymap-enhanced.git KeymapEnhanced;  
    git clone git@github.com:shagabutdinov/sublime-keyword.git Keyword;  
    git clone git@github.com:shagabutdinov/sublime-local-variable.git LocalVariable;  
    git clone git@github.com:shagabutdinov/sublime-method.git Method;  
    git clone git@github.com:shagabutdinov/sublime-named-mark.git NamedMark;  
    git clone git@github.com:shagabutdinov/sublime-nested-snippet.git NestedSnippet;  
    git clone git@github.com:shagabutdinov/sublime-nesting-snippet.git NestingSnippet;  
    git clone git@github.com:shagabutdinov/sublime-open-path.git OpenPath;  
    git clone git@github.com:shagabutdinov/sublime-project-files.git ProjectFiles;  
    git clone git@github.com:shagabutdinov/sublime-quick-search-enhanced.git QuickSearchEnhanced;  
    git clone git@github.com:shagabutdinov/sublime-remove-selection.git RemoveSelection;  
    git clone git@github.com:shagabutdinov/sublime-repeat-command.git RepeatCommand;  
    git clone git@github.com:shagabutdinov/sublime-scope-context.git ScopeContext;  
    git clone git@github.com:shagabutdinov/sublime-scroll-enhanced.git ScrollEnhanced;  
    git clone git@github.com:shagabutdinov/sublime-search-panel-enhanced.git SearchPanelEnhanced;  
    git clone git@github.com:shagabutdinov/sublime-semicolon.git Semicolon;  
    git clone git@github.com:shagabutdinov/sublime-shell-status.git ShellStatus;  
    git clone git@github.com:shagabutdinov/sublime-snippet-caller.git SnippetCaller;  
    git clone git@github.com:shagabutdinov/sublime-snippet-manager.git SnippetManager;  
    git clone git@github.com:shagabutdinov/sublime-statement.git Statement;  
    git clone git@github.com:shagabutdinov/sublime-status-message.git StatusMessage;  
    git clone git@github.com:shagabutdinov/sublime-enhanced.git SublimeEnhanced;  
    git clone git@github.com:shagabutdinov/sublime-terminal-project-folder.git TerminalProjectFolder;  
    git clone git@github.com:shagabutdinov/sublime-toggle-wrap.git ToggleWrap;  
    git clone git@github.com:shagabutdinov/sublime-utilities.git Utilities;  
    git clone git@github.com:shagabutdinov/sublime-wrap-statement.git WrapStatement

By [Keen Dev][anchor4] on [August 2, 2016][anchor5].

Exported from [Medium][anchor6] on May 31, 2017\.


[anchor0]: https://github.com/shagabutdinov/sublime-enhanced "https://github.com/shagabutdinov/sublime-enhanced"
[anchor1]: https://github.com/shagabutdinov/sublime-enhanced
[anchor2]: https://github.com/shagabutdinov/sublime-method "https://github.com/shagabutdinov/sublime-method"
[anchor3]: https://github.com/shagabutdinov/sublime-method
[anchor4]: https://medium.com/@keendev
[anchor5]: https://medium.com/p/a165c2f033b0
[anchor6]: https://medium.co