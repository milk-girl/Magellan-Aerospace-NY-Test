Put the PostgreSQL script of Part 1 here.

CREATE DATABASE Part;

CREATE TABLE item
(
id INTEGER NOT NULL,
item_name VARCHAR(50) NOT NULL,
parent_item INTEGER REFERENCES item(id),
cost INTEGER NOT NULL,
req_date DATE NOT NULL,
PRIMARY KEY (id)
);

INSERT INTO item (id, item_name, parent_item, cost, req_date) VALUES
(1, 'Item1', null, 500, '02-20-2024'), (2, 'Sub1', 1, 200, '02-10-2024'),
(3, 'Sub2', 1, 300, '01-05-2024'), (4, 'Sub3', 2, 300, '01-02-2024'),
(5, 'Sub4', 2, 400, '01-02-2024'), (6, 'Item2', null, 600, '03-15-2024'),
(7, 'Sub1', 6, 200, '02-25-2024');

