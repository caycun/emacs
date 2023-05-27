(setq inhibit-startup-message t)

(tool-bar-mode 0)
(menu-bar-mode 0)
(scroll-bar-mode 0)
(column-number-mode 1)
(show-paren-mode 1)

(set-face-attribute 'default nil :font "Iosevka" :height 120)

(load-theme 'gruber-darker t)



;; Make ESC quit prompts
(global-set-key (kbd "<escape>") 'keyboard-escape-quit) ;

;; Initialize package sources
(require 'package)

(setq package-archives '(("melpa" . "https://melpa.org/packages/")
                         ("org" . "https://orgmode.org/elpa/")
                         ("elpa" . "https://elpa.gnu.org/packages/")))

(package-initialize)
(unless package-archive-contents
 (package-refresh-contents))

;; Relative


;; Download Evil
(unless (package-installed-p 'evil)
  (package-install 'evil))

(unless (package-installed-p 'projectile)
  (package-install 'projectile))

(use-package projectile

  :config (projectile-mode 1)
  (setq projectile-project-search-path'("~/development"))

  (setq projectile-enable-caching t
	projectile-completion-system 'ivy
	projectile-indexing-method- 'alien
 ) 

  (define-key projectile-mode-map (kbd "C-c p") 'projectile-commander)
  (define-key projectile-mode-map (kbd "C-c C-p") 'projectile-commander)

  )

(use-package hydra :ensure t)
(use-package json-mode :ensure t)

(use-package magit
  :ensure t)

(setq magit-auto-revert-mode nil)

(global-set-key (kbd "C-c m s") 'magit-status)
(global-set-key (kbd "C-c m l") 'magit-log)

(use-package smex
  :ensure t
  :config
  (smex-initialize)
  (global-set-key (kbd "M-x") 'smex)
  (global-set-key (kbd "M-X") 'smex-major-mode-commands)
  )


;; Enable Evil
(require 'evil)
(evil-mode 1)

(require 'linum-relative)
(linum-relative-mode)

(require 'rust-mode)

(custom-set-variables
 ;; custom-set-variables was added by Custom.
 ;; If you edit it by hand, you could mess it up, so be careful.
 ;; Your init file should contain only one such instance.
 ;; If there is more than one, they won't work right.
 '(package-selected-packages
   '(smex magit rust-mode linum-relative evil use-package ivy gruber-darker-theme doom-modeline command-log-mode)))
(custom-set-faces
 ;; custom-set-faces was added by Custom.
 ;; If you edit it by hand, you could mess it up, so be careful.
 ;; Your init file should contain only one such instance.
 ;; If there is more than one, they won't work right.
 )
