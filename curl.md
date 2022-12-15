curl  -vvvv --cert 1000005601.crt:1966 --key 1000005601.key  --location --request POST 'https://tli-mercury-lcp.stoloto.su/fprov/fcgi_mercury_pos' --header 'Content-Type: application/xml' --data-raw '<?xml version="1.0" encoding="utf-8"?><ticketInfo><terminal>1000005601</terminal><number>5150499000400391</number></ticketInfo>'

curl  -vvvv -ufcgi_games:fcgi_games --location --request POST 'https://tfi-mercury-lcp-basic.stoloto.su/fprov/fcgi_mercury_pos' --header 'Content-Type: application/xml' --data-raw '<?xml version="1.0" encoding="utf-8"?><ticketInfo><terminal>1000005601</terminal><number>5150499000400391</number></ticketInfo>'

