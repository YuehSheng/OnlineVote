
schema

CREATE TABLE vote_items (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL
);

CREATE TABLE vote_records (
    voter_id VARCHAR(10),
    voter_name VARCHAR(20),
    item_id INT,
    PRIMARY KEY (voter_id, item_id),
    FOREIGN KEY (item_id) REFERENCES vote_item(id)
);

