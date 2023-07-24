# Virtual
INSERT into heroes
    (name, alias, superPower, powerRanking)
values
    ('Bruce Wayne', 'Batman', 'Martial Arts', 3),
    ('Clark Kent', 'Superman', 'Flight', 5),
    ('Jay Garrick', 'The Flash', 'Super-speed', 3),
    ('Alan Scott', 'Green Lantern', 'Ring Creation', 4),
    ('Helena Bertenelli', 'The Huntress', 'Crossbow Archery', 3),
    ('Dr. Harleen Quinzel', 'Harley Quinn', 'Hammer-fighting', 3),
    ('Floyd Lawton', 'Deadshot', 'Marksmaship', 2),
    ('Cecil Adams', 'Count Vertigo', 'Drug-dealing', 2),
    ('Damian Wayne', 'Robin', 'Swordsmanship', 2),
    ('Dick Grayson', 'Nightwing', 'Acrobatics', 3)
;



select * from heroes;

select name, alias from heroes;

select name as "Hero Name", alias from heroes;

select * from heroes where powerranking > 3;
select * from heroes where powerranking > 2 and powerranking < 5 ;
select * from heroes where powerranking >= 2 and powerranking < 5 ;
select * from heroes where name like '%el%';

select * from heroes;

update heroes
set superpower = 'Flight and strength of steel'
where alias='Superman';

update heroes
set superpower = 'Flight, strength of steel, and laser in eyes',
powerranking=4
where alias='Superman';

select * from heroes where name like '%el%';

update heroes
set powerranking=1
where name like '%el%';

select * from heroes;

delete from heroes 
where name like '%el%';


QL-4)

drop table heroes;

create table heroes /* creates a new table called heroes */
(
    id int AUTO_INCREMENT PRIMARY KEY,       /* Adds field id that is an integer that auto increments and PK */
    name varchar (50) not null,               /* Adds field name that is a none-null varchar of length 50 */
    alias varchar (50) not null,             /* Adds field alias that is a none-null varchar of length 50 */
    superPower varchar (70) not null,        /* Adds field SuperPower that is a none-null varchar of length 70 */
    powerRanking int not null
);    


QL-5)

drop table heroes;

create table teams
(
    id int auto_increment PRIMARY KEY,
    name varchar (50) not null,
    objectives varchar (100) not null
);

create table heroes /* creates a new table called heroes */
(
    id int AUTO_INCREMENT PRIMARY KEY,            /* Adds field id that is an integer that auto increments and PK */
    name varchar (50) not null,                   /* Adds field name that is a none-null varchar of length 50 */
    alias varchar (50) not null,                  /* Adds field alias that is a none-null varchar of length 50 */
    superPower varchar (70) not null,             /* Adds field SuperPower that is a none-null varchar of length 70 */
    powerRanking int not null,
    team_id int not null,                         /* Adds TeamID name that is a none-null int */
    FOREIGN key (team_id) REFERENCES teams (id)   /* Makes a reference to the field id in the team table as TeamID is a foreign key */
);     

insert into teams
    (id, name, objectives)
values
    ('JSA', 'Defeat the Nazis'),
    ('Birds of Prey', 'Fight crime(without men)'),
    ('Task Force X', 'Follow Waller\''s orders or die'),
    ('Teen Titans', 'Teach young superheroes to be their best'),
    ('Wayne Family', 'Protect the legacy of the Wayne name');
;

