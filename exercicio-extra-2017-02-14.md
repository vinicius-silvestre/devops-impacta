Modificações:
APACHE HTTP SERVER
+%{_libdir}/httpd/modules/mod_proxy_hcheck.so
Adicionou uma verificação do proxy.

NGINX
if [ $HTTP_MIRROR = YES ]; then
 +        ngx_module_name=ngx_http_mirror_module
 +        ngx_module_incs=
 +        ngx_module_deps=
 +        ngx_module_srcs=src/http/modules/ngx_http_mirror_module.c
 +        ngx_module_libs=
 +        ngx_module_link=$HTTP_MIRROR
 +
 +        . auto/module
 +    fi
 Consertou um bug na verificação do requerimento PCRE
 
 WORDPRESS
 
