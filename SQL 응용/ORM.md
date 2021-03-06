# ORM(Object-Relational Mapping)

- 객체와 관계형 데이터베이스의 데이터를 연결하는 기술
- OMR은 객체지향 프로그래밍에서 사용할 수 있는 가상의 객체지향 데이터베이스를 만들어 프로그래밍 코드와 데이터를 연결한다
- ORM으로 생성된 가상의 객체지향 데이터베이스는 프로그래밍 코드 또는 데이터베이스와 독립적이므로 재사용 및 유지보수가 용이하다



**파이썬으로 작성한 코드를 관계형 DB의 SQL 쿼리로 자동변환 시켜 개발자가 따로 SQL쿼리를 작성할 필요 없이 파이썬 코드 작성만으로 DB를 조작할 수 있게 해주는 것 ( 파이썬은 예시 )**



### ORM 프레임워크

- ORM을 구현하기 위한 구조와 구현을 위해 필요한 여러 기능들을 제공하는 프레임 워크

  | 기반 언어 | 프레임워크                                         |
  | --------- | -------------------------------------------------- |
  | JAVA      | JPA, HIBERNATE, ECLIPSELINK, DATANUCLEUS, EBEAN 등 |
  | C++       | ODB, QXORM 등                                      |
  | Python    | Django, SQLAlchemy,Storm 등                        |
  | .NET      | NHibernate,DatabaseObjects,Dapper 등               |
  | PHP       | Doctrine,Propel,RedBean 등                         |

  

### ORM의 한계

- 프레임워크가 자동으로 SQL을 작성하기 때문에 의도대로 SQL이 작성되었는지 확인해야 한다
- 객체지향적인 사용을 고려하고 설계된 데이터베이스가 아닌 경우 프로젝트가 크고 복잡해 질수록 ORM 기술을 적용하기 어렵다
- ORM을 고려하지 않은 데이터베이스를 사용하고 있기 때문에 ORM에 적합하게 변환하려면 많은 시간과 노력이 필요하다

