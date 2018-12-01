# sql
Examples of sql

TERADATA

SELECT TOP 12 sku, saledate, orgprice, sprice, (orgprice - sprice) as margin
FROM trnsact
WHERE saledate = '2004-08-01'
ORDER BY margin DESC;

SELECT TOP 10 sku, register, saledate, orgprice, sprice, amt
FROM trnsact
WHERE saledate BETWEEN '2004-08-01' AND '2004-08-10'
ORDER BY orgprice DESC, sprice DESC;

SELECT DISTINCT brand
FROM skuinfo
WHERE brand LIKE '%liz%';

SELECT TOP 10 *
FROM store_msa
WHERE city IN ('little rock', 'memphis', 'tulsa')
ORDER BY store;
