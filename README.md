http://djangoci-cd-production.up.railway.app/docs/api/
 ab -n 100 -c 10 https://djangoci-cd-production.up.railway.app/api/products
ab -n 100 -c 10 https://djangoci-cd-production.up.railway.app/products-django/

wrk -t4 -c200 -d30s https://djangoci-cd-production.up.railway.app/api/products
wrk -t4 -c200 -d30s https://djangoci-cd-production.up.railway.app/products-django/