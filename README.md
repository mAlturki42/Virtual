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


