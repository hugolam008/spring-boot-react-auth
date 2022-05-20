# spring-boot-react-auth

首次运行前请执行：
INSERT INTO roles(name) VALUES('ROLE_USER');
INSERT INTO roles(name) VALUES('ROLE_MODERATOR');
INSERT INTO roles(name) VALUES('ROLE_ADMIN');

#运行server
mvn spring-boot:run

#运行react（react-jwt-auth目录下）
npm start
