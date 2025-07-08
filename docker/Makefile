.PHONY: oltp-up
compose-up:
	@docker compose up -d

.PHONY: inject-up
inject-up:
	@docker compose --profile inject up -d
	@echo "Inject service is up."

# Initialize adventureworks database
.PHONY: init-db
init-db:
	@cd ../adw14 && chmod +x adw14data.sh && ./adw14data.sh
	@cd ../docker

.PHONY: insert-data
insert-data:
	@docker exec -it inject-adw14 /bin/bash -c "./adw14data.sh"

.PHONY: all
all: compose-up insert-data
	@echo "All services are up and data has been inserted."