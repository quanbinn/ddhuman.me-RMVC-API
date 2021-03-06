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

## **Lesson**

|                  |      Router      |       Model      |       View       |    Controller    |
| :--------------: | :--------------: | :--------------: | :--------------: | :--------------: |
| 	   **C**	   | [R_createALesson]|         \        | [V_createALesson]| [C_createALesson]|
| 	   **R**	   | [R_showALesson]  |    [M_Lesson]    | [V_showALesson]  | [C_showALesson]  |
| 	   **U**	   | [R_editALesson]  |         /         | [V_editALesson]  | [C_editALesson]  |
| 	   **D**	   | [R_deleteALesson]|        /          | [V_deleteALesson]| [C_deleteALesson]|

[R_createALesson]: /chapters/lesson/createALesson/R_createALesson.md
[V_createALesson]: /chapters/lesson/createALesson/V_createALesson.md
[C_createALesson]: /chapters/lesson/createALesson/C_createALesson.md
[R_showALesson]: /chapters/lesson/showALesson/R_showALesson.md
[V_showALesson]: /chapters/lesson/showALesson/V_showALesson.md
[C_showALesson]: /chapters/lesson/showALesson/C_showALesson.md
[R_editALesson]: /chapters/lesson/editALesson/R_editALesson.md
[V_editALesson]: /chapters/lesson/editALesson/V_editALesson.md
[C_editALesson]: /chapters/lesson/editALesson/C_editALesson.md
[R_deleteALesson]: /chapters/lesson/deleteALesson/R_deleteALesson.md
[V_deleteALesson]: /chapters/lesson/deleteALesson/V_deleteALesson.md
[C_deleteALesson]: /chapters/lesson/deleteALesson/C_deleteALesson.md
[M_Lesson]: /chapters/lesson/M_Lesson.md

## **Order**

|                  |      Router      |       Model      |       View       |    Controller    |
| :--------------: | :--------------: | :--------------: | :--------------: | :--------------: |
| 	   **C**	   | [R_createAnOrder]|         \        | [V_createAnOrder]| [C_createAnOrder]|
| 	   **R**	   | [R_showAnOrder]  |     [M_Order]    | [V_showAnOrder]  | [C_showAnOrder]  |

[R_createAnOrder]: /chapters/order/createAnOrder/R_createAnOrder.md
[V_createAnOrder]: /chapters/order/createAnOrder/V_createAnOrder.md
[C_createAnOrder]: /chapters/order/createAnOrder/C_createAnOrder.md
[R_showAnOrder]: /chapters/order/showAnOrder/R_showAnOrder.md
[V_showAnOrder]: /chapters/order/showAnOrder/V_showAnOrder.md
[C_showAnOrder]: /chapters/order/showAnOrder/C_showAnOrder.md
[M_Order]: /chapters/order/M_Order.md

## **Static webpage**

|          |  Router  | Model |   View   | Controller |
| :------: | :------: | :---: | :------: | :--------: |
| **home** | [R_home] |       | [V_home] |  [C_home]  |

[R_home]: /chapters/static_webpage/home/R_home.md
[V_home]: /chapters/static_webpage/home/V_home.md
[C_home]: /chapters/static_webpage/home/C_home.md

## Role and Permission

|  超级管理员   |   管理员    |   付费用户    |   普通用户   |
| :---------:  | :-------:  | :-----------:| :---------: | 
|[if_超级管理员]| [if_管理员] | [if_付费用户] |[if_普通用户] | 

[if_超级管理员]: /chapters/role_and_permission/if_超级管理员.md
[if_管理员]: /chapters/role_and_permission/if_管理员.md
[if_付费用户]: /chapters/role_and_permission/if_付费用户.md
[if_普通用户]: /chapters/role_and_permission/if_普通用户.md

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


