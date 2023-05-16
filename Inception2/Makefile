all: 
	mkdir -p /home/lunovill/data/mariadb
	mkdir -p /home/lunovill/data/wordpress
	docker compose -f ./srcs/docker-compose.yml build
	docker compose -f ./srcs/docker-compose.yml up -d


clean:
	docker container stop nginx mariadb wordpress

fclean: clean
	@sudo rm -rf /home/lunovill/data/mariadb/*
	@sudo rm -rf /home/lunovill/data/wordpress/*
	@docker system prune -af

re: fclean all

.Phony: all logs clean fclean