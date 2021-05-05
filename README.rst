EMACS
=================================================================================

.. contents:: **Daftar Isi**

Install di Ubuntu
---------------------------------------------------------------------------------

::

    $ sudo snap install emacs --classic

**Referensi**

- `linuxhint.com <https://linuxhint.com/ubuntu_emacs_installation/>`_

Tutorial
---------------------------------------------------------------------------------

- Buka Emacs kemudian pilih Emacs Tutorial. 
- `cestlaz.github.io <https://cestlaz.github.io/stories/emacs/>`_


Org Mode
---------------------------------------------------------------------------------

- `the org manual <https://orgmode.org/manual/index.html#SEC_Contents>`_
- `org-mode tutorials <http://pragmaticemacs.com/org-mode-tutorials/>`_

Cheatsheet
---------------------------------------------------------------------------------

- `washington.edu
  <https://courses.cs.washington.edu/courses/cse351/16wi/sections/1/Cheatsheet-emacs.pdf>`_
- `gnu.org <https://www.gnu.org/software/emacs/refcards/pdf/refcard.pdf>`_  
- `opensource.com
  <https://www.devguide.at/wp-content/uploads/2021/01/cheat_sheet_emacs.pdf>`_

init.el
---------------------------------------------------------------------------------

::

    (setq inhibit-startup-message t)

    (require 'package)
    (setq package-enable-at-startup nil)
    (add-to-list 'package-archives
             '("melpa" . "https://melpa.org/packages/"))

    (package-initialize)

    (unless (package-installed-p 'use-package)
      (package-refresh-contents)
      (package-install 'use-package))

    (use-package try
      :ensure t)

    (use-package which-key
      :ensure t
      :config (which-key-mode))

    (custom-set-variables
     ;; custom-set-variables was added by Custom.
     ;; If you edit it by hand, you could mess it up, so be careful.
     ;; Your init file should contain only one such instance.
     ;; If there is more than one, they won't work right.
     '(package-selected-packages '(use-package)))
    (custom-set-faces
     ;; custom-set-faces was added by Custom.
     ;; If you edit it by hand, you could mess it up, so be careful.
     ;; Your init file should contain only one such instance.
     ;; If there is more than one, they won't work right.
     )

**Referensi**

- `cestlaz.github.io - package manager
  <https://cestlaz.github.io/posts/using-emacs-1-setup/>`_

Run Emacs di Terminal
---------------------------------------------------------------------------------

::

   $ emacs -nw filename.extension
