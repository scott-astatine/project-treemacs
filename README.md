<h1 align="center">Project Treemacs</h1>
<hr>
<p align="center">
Simple treemacs backend for project.el:

* Projects in Treemacs map to project.el projects
* Workspaces in Treemacs map to project.el external roots
* `project-find-file`, `project-switch-to-buffer`, `project-find-regexp` et al operate on the current treemacs project.
* `project-or-external-find-file`, `project-or-external-find-regexp` operate on the current treemacs workspace.
</p>
<hr>

# Usage
For the moment, the project-treemacs backend depends on the treemacs side panel being visible. 

Use treemacs as you normally would, creating workspaces, projects, etc. 

Use project.el commands as you normally would, with your project spaces defined by the current treemacs project, and the current treemacs workspace.
# Examples
![treemacs-project-search](https://github.com/cmccloud/project-treemacs/blob/master/examples/project-search.gif?raw=true)
Using `project-find-file` to search for files within the current treemacs project.
<hr>

![treemacs-workspace-search](https://github.com/cmccloud/project-treemacs/blob/master/examples/workspace-search.gif?raw=true)
Using `project-or-external-find-file` to search for files within the current treemacs workspace.
# Installing
Clone this repository and install using `use-package`, then enable with by calling `project-treemacs-mode`.

``` emacs-lisp
(use-package project-treemacs
  :demand t
  :after treemacs
  :load-path "path/to/project-treemacs-repository"
  :init (project-treemacs-mode))
```
# User Options
* `project-treemacs-ignores` - list of patterns to add to `project-ignores`.
* `project-treemacs-prefer-backend` - Whether or not to prefer the project-treemacs backend over others. See the commentary in project.el for more information, and the documentation for `project-find-functions` in particular.

# Links
* [Working with Projects - Emacs Manual](https://www.gnu.org/software/emacs/manual/html_node/emacs/Projects.html)

* [project.el at Emacs Mirror](https://github.com/emacs-mirror/emacs/blob/master/lisp/progmodes/project.el)



