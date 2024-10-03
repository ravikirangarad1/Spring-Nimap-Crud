create the table in database 
CREATE TABLE Category (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL
);
CREATE TABLE Product (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    price DOUBLE NOT NULL,
    category_id BIGINT,
    FOREIGN KEY (category_id) REFERENCES Category(id) ON DELETE CASCADE
);
