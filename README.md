# ddhuman.me-RMVC-API

**Router-Model+View+Controller-API**

## **User**

|              |    Router    |  Model   |     View     |  Controller  |
| :----------: | :----------: | :------: | :----------: | :----------: |
| **register** | [R_register] |    \     | [V_register] | [C_register] |
|  **login**   |  [R_login]   | [M_User] |  [V_login]   |  [C_login]   |
|  **logout**  |  [R_logout]  |    /     |              |  [C_logout]  |

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
| **createAnExp** | [R_createAnExp] |       \        | [V_createAnExp] | [C_createAnExp] |
|  **showExps**   |  [R_showExps]   | [M_Experiment] |  [V_showExps]   |  [C_showExps]   |
|  **showAnExp**  |  [R_showAnExp]  |       /        |  [V_showAnExp]  |  [C_showAnExp]  |

[R_createAnExp]: /chapters/experiment/showAnExp/R_createAnExp.md
[V_createAnExp]: /chapters/experiment/showAnExp/V_createAnExp.md
[C_createAnExp]: /chapters/experiment/showAnExp/C_createAnExp.md
[R_showExps]: /chapters/experiment/showExps/R_showExps.md
[V_showExps]: /chapters/experiment/showExps/V_showExps.md
[C_showExps]: /chapters/experiment/showExps/C_showExps.md
[R_showAnExp]: /chapters/experiment/showAnExp/R_showAnExp.md
[V_showAnExp]: /chapters/experiment/showAnExp/V_showAnExp.md
[C_showAnExp]: /chapters/experiment/showAnExp/C_showAnExp.md
[M_Experiment]: /chapters/experiment/M_Experiment.md
## **Equipment**

|              |    Router    |    Model     |     View     |  Controller  |
| :----------: | :----------: | :----------: | :----------: | :----------: |
| **learnEquip** | [R_learnEquip] | [M_learnEquip] | [V_learnEquip] | [C_learnEquip] |
| **workEquip**  | [R_workEquip]  | [M_workEquip]  | [V_workEquip]  | [C_workEquip]  |
| **exerEquip** | [R_exerEquip] | [M_exerEquip] | [V_exerEquip] | [C_exerEquip] |

[R_learnEquip]: /chapters/equipment/learnEquip/R_learnEquip.md
[M_learnEquip]: /chapters/equipment/learnEquip/M_learnEquip.md
[V_learnEquip]: /chapters/equipment/learnEquip/V_learnEquip.md
[C_learnEquip]: /chapters/equipment/learnEquip/C_learnEquip.md
[R_workEquip]: /chapters/equipment/workEquip/R_workEquip.md
[M_workEquip]: /chapters/equipment/workEquip/M_workEquip.md
[V_workEquip]: /chapters/equipment/workEquip/V_workEquip.md
[C_workEquip]: /chapters/equipment/workEquip/C_workEquip.md
[R_exerEquip]: /chapters/equipment/exerEquip/R_exerEquip.md
[M_exerEquip]: /chapters/equipment/exerEquip/M_exerEquip.md
[V_exerEquip]: /chapters/equipment/exerEquip/V_exerEquip.md
[C_exerEquip]: /chapters/equipment/exerEquip/C_exerEquip.md

## **Static webpage**

|          |  Router  | Model |   View   | Controller |
| :------: | :------: | :---: | :------: | :--------: |
| **home** | [R_home] |       | [V_home] |  [C_home]  |

[R_home]: /chapters/static_webpage/home/R_home.md
[V_home]: /chapters/static_webpage/home/V_home.md
[C_home]: /chapters/static_webpage/home/C_home.md

## Role and Permission

|                |      |      |      |      |
| :------------: | :--: | :--: | :--: | :--: |
|   **ADMIN**    |  []  |  []  |  []  |  []  |
| **PAID_USER**  |      |      |      |      |
| **BASIC_USER** |      |      |      |      |

## 附录

- Mongoose
	- [用mongoose操控MongoDB](/chapters/附录/mongoose_CRUD_collections/用mongoose操控MongoDB.md)
	- [移植MongoDB中documents的原理](/chapters/附录//mongoose_CRUD_collections/移植MongoDB中documents的原理.md)

|                 |    C     |    R     |    U     |    D     |
| :-------------: | :------: | :------: | :------: | :------: |
|    **users**    | [usersC] | [usersR] | [usersR] | [usersD] |
| **experiments** |    []    |    []    |    []    |    []    |

[usersC]: /chapters/附录/mongoose_CRUD_collections/usersC.md
[usersR]: /chapters/附录/home/mongoose_CRUD_collections/usersR.md
[usersR]: /chapters/附录/home/mongoose_CRUD_collections/usersR.md
[usersD]: /chapters/附录/home/mongoose_CRUD_collections/usersD.md

- POST
    - [提交form发送post请求的原理](/chapters/附录/提交form发送post请求的原理.md)
  
- Roles based access control
    - [基于role的access控制系统的核心逻辑](/chapters/附录/基于role的access控制系统的核心逻辑.md)
  
- CSS和Rresponsive layout
  - [实现responsive layout中各网页元素的width占比](/chapters/附录/CSS_Rresponsive_layout/实现responsive_layout中各网页元素的width占比.md)
  - [iphone和laptop的显示屏幕的像素尺寸和实体尺寸](/chapters/附录/CSS_Rresponsive_layout/iphone和laptop的显示屏幕的像素尺寸和实体尺寸.md)
  - [计算出iphone和laptop中image和video渲染前自适应高度的公式](/chapters/附录/CSS_Rresponsive_layout/计算出iphone和laptop中image和video渲染前自适应高度的公式.md)
  - [确定iphone和laptop中text渲染后的实体尺寸](/chapters/附录/CSS_Rresponsive_layout/确定iphone和laptop中text渲染后的实体尺寸.md)
  - [计算出iphone和laptop中text渲染时的实际像素值的公式](/chapters/附录/CSS_Rresponsive_layout/计算出iphone和laptop中text渲染时的实际像素值的公式.md)


|                 |     |    |    |    |
| :-------------: | :--: | :--: | :--: | :--: |
|    **Element1**    |  [body]  |  [column]  |  [image]  |  [video]  |

[body]: /chapters/附录/CSS_Rresponsive_layout/body.md
[column]: /chapters/附录/CSS_Rresponsive_layout/column.md
[image]: /chapters/附录/CSS_Rresponsive_layout/image.md
[video]: /chapters/附录/CSS_Rresponsive_layout/video.md

- Session和cookies
  - [理解在session中用cookies存储用户名和密码的原理](/chapters/附录/理解在session中用cookies存储用户名和密码的原理.md)


