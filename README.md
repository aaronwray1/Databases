# World Exercises

1) all cities
* SElECT DISTINCT COUNT(Name) FROM city WHERE
* 4079

US cities
SELECT COUNT(*) FROM city WHERE CountryCode = "USA";

2)
* SELECT LifeExpectancy FROM country WHERE Name="Argentina";
* 75.1

3)
* SELECT name, LifeExpectancy, Population FROM country WHERE LifeExpectancy IS NOT NULL ORDER BY LifeExpectancy DESC LIMIT 3;
* +------------+----------------+------------+
  | name       | LifeExpectancy | Population |
  +------------+----------------+------------+
  | Andorra    |           83.5 |      78000 |
  | Macao      |           81.6 |     473000 |
  | San Marino |           81.1 |      27000 |
  +------------+----------------+------------+

4)
* Select city.Name From city INNER JOIN country ON city.ID = country.Capital WHERE country.Name = "Spain";
* Madrid

5)
* Select Language From countrylanguage INNER JOIN country ON countrylanguage.CountryCode = country.Code WHERE country.Region="Southeast Asia";

6)

7)
* Select COUNT(city.Name) From city INNER JOIN country ON city.CountryCode = country.Code WHERE country.Name = "China";
* 363

8)
* Select Name, Population FROM country WHERE population IS NOT NULL ORDER BY population ASC Limit 3;
* Antartica

9)

10)
* Select Name, Population FROM country WHERE population IS NOT NULL ORDER BY population DESC Limit 10;
* +--------------------+------------+
  | Name               | Population |
  +--------------------+------------+
  | China              | 1277558000 |
  | India              | 1013662000 |
  | United States      |  278357000 |
  | Indonesia          |  212107000 |
  | Brazil             |  170115000 |
  | Pakistan           |  156483000 |
  | Russian Federation |  146934000 |
  | Bangladesh         |  129155000 |
  | Japan              |  126714000 |
  | Nigeria            |  111506000 |
  +--------------------+------------+

11)
* Select city.Name, city.Population FROM city INNER JOIN country ON city.CountryCode = country.Code WHERE country.Name = "Japan" AND city.population IS NOT NULL Order By city.population DESC LIMIT 5;
* +---------------------+------------+
  | Name                | Population |
  +---------------------+------------+
  | Tokyo               |    7980230 |
  | Jokohama [Yokohama] |    3339594 |
  | Osaka               |    2595674 |
  | Nagoya              |    2154376 |
  | Sapporo             |    1790886 |
  +---------------------+------------+

12)
  * Select country.name, country.code From Country WHERE country.HeadOfState = "Elisabeth II";
  * +----------------------------------------------+------+
    | name                                         | code |
    +----------------------------------------------+------+
    | Anguilla                                     | AIA  |
    | Antigua and Barbuda                          | ATG  |
    | Australia                                    | AUS  |
    | Bahamas                                      | BHS  |
    | Belize                                       | BLZ  |
    | Bermuda                                      | BMU  |
    | Barbados                                     | BRB  |
    | Canada                                       | CAN  |
    | Cocos (Keeling) Islands                      | CCK  |
    | Cook Islands                                 | COK  |
    | Christmas Island                             | CXR  |
    | Cayman Islands                               | CYM  |
    | Falkland Islands                             | FLK  |
    | United Kingdom                               | GBR  |
    | Gibraltar                                    | GIB  |
    | Grenada                                      | GRD  |
    | Heard Island and McDonald Islands            | HMD  |
    | British Indian Ocean Territory               | IOT  |
    | Jamaica                                      | JAM  |
    | Saint Kitts and Nevis                        | KNA  |
    | Saint Lucia                                  | LCA  |
    | Montserrat                                   | MSR  |
    | Norfolk Island                               | NFK  |
    | Niue                                         | NIU  |
    | New Zealand                                  | NZL  |
    | Pitcairn                                     | PCN  |
    | Papua New Guinea                             | PNG  |
    | South Georgia and the South Sandwich Islands | SGS  |
    | Saint Helena                                 | SHN  |
    | Solomon Islands                              | SLB  |
    | Turks and Caicos Islands                     | TCA  |
    | Tokelau                                      | TKL  |
    | Tuvalu                                       | TUV  |
    | Saint Vincent and the Grenadines             | VCT  |
    | Virgin Islands, British                      | VGB  |
    +----------------------------------------------+------+

13)
* Select country.name, (country.population / country.SurfaceArea) AS ratio From country Order By ratio DESC LIMIT 10;
* +-------------------------------+--------------+
  | name                          | ratio        |
  +-------------------------------+--------------+
  | Macao                         | 26277.777778 |
  | Monaco                        | 22666.666667 |
  | Hong Kong                     |  6308.837209 |
  | Singapore                     |  5771.844660 |
  | Gibraltar                     |  4166.666667 |
  | Holy See (Vatican City State) |  2499.999963 |
  | Bermuda                       |  1226.415094 |
  | Malta                         |  1203.164557 |
  | Maldives                      |   959.731544 |
  | Bangladesh                    |   896.922179 |
  +-------------------------------+--------------+
