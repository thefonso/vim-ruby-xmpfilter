Support
* [rcodetools](http://rubygems.org/gems/rcodetools).
* [seeing_is_believing](https://github.com/JoshCheek/seeing_is_believing)

![Example](https://github.com/t9md/t9md/blob/master/img/vim-ruby-xmpfilter_anime.gif?raw=true)

###Installation

(after following the instructions for either of the tools listed above in "Support" ...)

cd ~/.vim

git clone https://github.com/t9md/vim-ruby-xmpfilter.git

now we will copy and past the contents of each folder plugin, docs and autoload into each corresponding folder in ~/.vim

type open .

after you have copied the files add the sample below to your .vimrc file...

### [help](https://github.com/t9md/vim-ruby-xmpfilter/blob/master/doc/xmpfilter.txt)

# .vimrc sample
==================================
vim-ruby-xmpfilter doesn't provide any default keymap.
See sample configuration below.

note: command+m <D-m> and command+r <D-r> ONLY work in [macvim](https://code.google.com/p/macvim/)

'xmpfilter' user

    autocmd FileType ruby nmap <buffer> <D-m> <Plug>(xmpfilter-mark)
    autocmd FileType ruby xmap <buffer> <D-m> <Plug>(xmpfilter-mark)
    autocmd FileType ruby imap <buffer> <D-m> <Plug>(xmpfilter-mark)

    autocmd FileType ruby nmap <buffer> <D-r> <Plug>(xmpfilter-run)
    autocmd FileType ruby xmap <buffer> <D-r> <Plug>(xmpfilter-run)
    autocmd FileType ruby imap <buffer> <D-r> <Plug>(xmpfilter-run)

'seeing_is_believing' user

    let g:xmpfilter_cmd = "seeing_is_believing"

    autocmd FileType ruby nmap <buffer> <D-m> <Plug>(seeing_is_believing-mark)
    autocmd FileType ruby xmap <buffer> <D-m> <Plug>(seeing_is_believing-mark)
    autocmd FileType ruby imap <buffer> <D-m> <Plug>(seeing_is_believing-mark)

    autocmd FileType ruby nmap <buffer> <D-c> <Plug>(seeing_is_believing-clean)
    autocmd FileType ruby xmap <buffer> <D-c> <Plug>(seeing_is_believing-clean)
    autocmd FileType ruby imap <buffer> <D-c> <Plug>(seeing_is_believing-clean)

    " xmpfilter compatible
    autocmd FileType ruby nmap <buffer> <D-r> <Plug>(seeing_is_believing-run_-x)
    autocmd FileType ruby xmap <buffer> <D-r> <Plug>(seeing_is_believing-run_-x)
    autocmd FileType ruby imap <buffer> <D-r> <Plug>(seeing_is_believing-run_-x)

    " auto insert mark at appropriate spot.
    autocmd FileType ruby nmap <buffer> <F5> <Plug>(seeing_is_believing-run)
    autocmd FileType ruby xmap <buffer> <F5> <Plug>(seeing_is_believing-run)
    autocmd FileType ruby imap <buffer> <F5> <Plug>(seeing_is_believing-run)
