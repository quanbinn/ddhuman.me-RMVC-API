# ddhuman.me-RMVC-API

**Router-Model+View+Controller-API**

## **User**

|                 |    Router    |  Model   |     View     |  Controller  |
| :-------------: | :----------: | :------: | :----------: | :----------: |
| **C**(register) | [R_register] |    \     | [V_register] | [C_register] |
| **R**(login)    |  [R_login]   | [M_User] |  [V_login]   |  [C_login]   |
|**Session**logout|  [R_logout]  |    /     |              |  [C_logout]  |

[R_register]: /chapters/user/register/R_register.md
[V_register]: /chapters/user/register/V_register.md
[C_register]: /chapters/user/register/C_register.md
[R_login]: /chapters/user/login/R_login.md
[V_login]: /chapters/user/login/V_login.md
[C_login]: /chapters/user/login/C_login.md
[R_logout]: /chapters/user/logout/R_logout.md
[C_logout]: /chapters/user/logout/C_logout.md
[M_User]: /chapters/user/M_User.md

## **Experiment**

|                 |     Router      |     Model      |      View       |   Controller    |
| :-------------: | :-------------: | :------------: | :-------------: | :-------------: |
| 	   **C**	  | [R_createAnExp] |      \         | [V_createAnExp] | [C_createAnExp] |
| 	   **R**	  |  [R_showExps]   |       \        |  [V_showExps]   |  [C_showExps]   |
| 	   **R**	  |  [R_showAnExp]  | [M_Experiment] |  [V_showAnExp]  |  [C_showAnExp]  |
| 	   **U**	  |  [R_editAnExp]  |       /        |  [V_editAnExp]  |  [C_editAnExp]  |
| 	   **D**	  |  [R_deleteAnExp]|      /         |                 |  [C_deleteAnExp]|

[R_createAnExp]: /chapters/experiment/showAnExp/R_createAnExp.md
[V_createAnExp]: /chapters/experiment/showAnExp/V_createAnExp.md
[C_createAnExp]: /chapters/experiment/showAnExp/C_createAnExp.md
[R_showExps]: /chapters/experiment/showExps/R_showExps.md
[V_showExps]: /chapters/experiment/showExps/V_showExps.md
[C_showExps]: /chapters/experiment/showExps/C_showExps.md
[R_showAnExp]: /chapters/experiment/showAnExp/R_showAnExp.md
[V_showAnExp]: /chapters/experiment/showAnExp/V_showAnExp.md
[C_showAnExp]: /chapters/experiment/showAnExp/C_showAnExp.md
[R_editAnExp]: /chapters/experiment/editAnExp/R_editAnExp.md
[V_editAnExp]: /chapters/experiment/editAnExp/V_editAnExp.md
[C_editAnExp]: /chapters/experiment/editAnExp/C_editAnExp.md
[R_deleteAnExp]: /chapters/experiment/deleteAnExp/R_deleteAnExp.md
[C_deleteAnExp]: /chapters/experiment/deleteAnExp/C_deleteAnExp.md
[M_Experiment]: /chapters/experiment/M_Experiment.md

## **Goods**

|                  |      Router      |       Model      |       View       |    Controller    |
| :--------------: | :--------------: | :--------------: | :--------------: | :--------------: |
| 	   **C**	   | [R_createAGoods] |         \        | [V_createAGoods] | [C_createAGoods] |
| 	   **R**	   | [R_showAGoods]   |    [M_Goods]     | [V_showAGoods]   | [C_showAGoods]   |
| 	   **U**	   | [R_editAGoods]   |        /         | [V_editAGoods]   | [C_editAGoods]   |
| 	   **D**	   | [R_deleteAGoods] |       /          | [V_deleteAGoods] | [C_deleteAGoods] |

[R_createAGoods]: /chapters/goods/createAGoods/R_createAGoods.md
[V_createAGoods]: /chapters/goods/createAGoods/V_createAGoods.md
[C_createAGoods]: /chapters/goods/createAGoods/C_createAGoods.md
[R_showAGoods]: /chapters/goods/showAGoods/R_showAGoods.md
[V_showAGoods]: /chapters/goods/showAGoods/V_showAGoods.md
[C_showAGoods]: /chapters/goods/showAGoods/C_showAGoods.md
[R_editAGoods]: /chapters/goods/editAGoods/R_editAGoods.md
[V_editAGoods]: /chapters/goods/editAGoods/V_editAGoods.md
[C_editAGoods]: /chapters/goods/editAGoods/C_editAGoods.md
[R_deleteAGoods]: /chapters/goods/deleteAGoods/R_deleteAGoods.md
[V_deleteAGoods]: /chapters/goods/deleteAGoods/V_deleteAGoods.md
[C_deleteAGoods]: /chapters/goods/deleteAGoods/C_deleteAGoods.md
[M_Goods]: /chapters/goods/M_Goods.md

## **Course**

|                  |      Router      |       Model      |       View       |    Controller    |
| :--------------: | :--------------: | :--------------: | :--------------: | :--------------: |
| 	   **C**	   | [R_createACourse]|         \        | [V_createACourse]| [C_createACourse]|
| 	   **R**	   | [R_showACourse]  |    [M_Course]    | [V_showACourse]  | [C_showACourse]  |
| 	   **U**	   | [R_editACourse]  |         /         | [V_editACourse]  | [C_editACourse]  |
| 	   **D**	   | [R_deleteACourse]|        /          | [V_deleteACourse]| [C_deleteACourse]|

[R_createACourse]: /chapters/course/createACourse/R_createACourse.md
[V_createACourse]: /chapters/course/createACourse/V_createACourse.md
[C_createACourse]: /chapters/course/createACourse/C_createACourse.md
[R_showACourse]: /chapters/course/showACourse/R_showACourse.md
[V_showACourse]: /chapters/course/showACourse/V_showACourse.md
[C_showACourse]: /chapters/course/showACourse/C_showACourse.md
[R_editACourse]: /chapters/course/editACourse/R_editACourse.md
[V_editACourse]: /chapters/course/editACourse/V_editACourse.md
[C_editACourse]: /chapters/course/editACourse/C_editACourse.md
[R_deleteACourse]: /chapters/course/deleteACourse/R_deleteACourse.md
[V_deleteACourse]: /chapters/course/deleteACourse/V_deleteACourse.md
[C_deleteACourse]: /chapters/course/deleteACourse/C_deleteACourse.md
[M_Course]: /chapters/course/M_Course.md

## **Static webpage**

|          |  Router  | Model |   View   | Controller |
| :------: | :------: | :---: | :------: | :--------: |
| **home** | [R_home] |       | [V_home] |  [C_home]  |

[R_home]: /chapters/static_webpage/home/R_home.md
[V_home]: /chapters/static_webpage/home/V_home.md
[C_home]: /chapters/static_webpage/home/C_home.md

## Role and Permission

|            |               |                 |
| :--------: | :------------:| :-------------: | 
| [if_admin] | [if_paiduser] | [if_commonuser] | 

[if_admin]: /chapters/role_and_permission/if_admin.md
[if_paiduser]: /chapters/role_and_permission/if_paiduser.md
[if_commonuser]: /chapters/role_and_permission/if_commonuser.md

## 附录

- Mongoose
	- [用mongoose操控MongoDB](/chapters/附录/mongoose_CRUD_collections/用mongoose操控MongoDB.md)
	- [移植MongoDB中documents的原理](/chapters/附录//mongoose_CRUD_collections/移植MongoDB中documents的原理.md)

|                 |    Create    |    Read    |    Update    |    Delete    |
| :-------------: | :----------: | :--------: | :----------: | :----------: |
|    **users**    |[userCreate] | [userRead] | [userUpdate]|[userDelete] |
|**experiments**|[experimentCreate]|[experimentRead]|[experimentUpdate]|  [experimentDelete]|

[userCreate]: /chapters/附录/mongoose_CRUD_collections/userCreate.md
[userRead]: /chapters/附录/mongoose_CRUD_collections/userRead.md
[userUpdate]: /chapters/附录/mongoose_CRUD_collections/userUpdate.md
[userDelete]: /chapters/附录/mongoose_CRUD_collections/userDelete.md
[experimentCreate]: /chapters/附录/mongoose_CRUD_collections/experimentCreate.md
[experimentRead]: /chapters/附录/mongoose_CRUD_collections/experimentRead.md
[experimentUpdate]: /chapters/附录/mongoose_CRUD_collections/experimentUpdate.md
[experimentDelete]: /chapters/附录/mongoose_CRUD_collections/experimentDelete.md

- POST
    - [提交form发送post请求的原理](/chapters/附录/提交form发送post请求的原理.md)
  
- Roles based access control
    - [基于role的access控制系统的核心逻辑](/chapters/附录/基于role的access控制系统的核心逻辑.md)

- Session和cookies
  - [理解在session中用cookies存储用户名和密码的原理](/chapters/附录/理解在session中用cookies存储用户名和密码的原理.md)


