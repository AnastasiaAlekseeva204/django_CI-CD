http://djangoci-cd-production.up.railway.app/docs/api/
 ab -n 10000 -c 1000 https://djangoci-cd-production.up.railway.app/api/products - test 
ab -n 10000 -c 1000 https://djangoci-cd-production.up.railway.app/products-django/ - ляжет не ляжет

wrk -t4 -c200 -d30s https://djangoci-cd-production.up.railway.app/api/products
wrk -t4 -c200 -d30s https://djangoci-cd-production.up.railway.app/products-django/