# GrasshopperBake-with-Serial-Number  

ユニークな部材を管理するために、連番で名前をつけてファイル書き出しをする。  
手でやるのは面倒なので、自動化させる。  


### index

- GrasshopperBake-with-Serial-Number.ghx  

  - ListItem  
    - ghpythonlib.components で ListItem コンポーネントを使ってみる  

  - List-Bake   
    - K個のオブジェクトを、0 から K まで、連番で数字を振って STL ファイルに書き出し  
    - For ループでまわす

  - TreeBake  
    - U x V 行列を、0_0 から N_M まで、ID を付けて STL ファイルに書き出し  
    ```Python
    num_1, hoge = divmod(i, U)
    str_1 = str(num_1)
    str_2 = str(i%U)

    selMesh = ghpc.ListItem(Array,i)

    str_name = str_1 + "_" +str_2
    ```


---

### ref  

[ghpythonlib.componentsをつかってコンポーネント機能をpythonからコール](http://am.d-xx.com/2015/06/04/ghpythonlib-components%E3%82%92%E3%81%A4%E3%81%8B%E3%81%A3%E3%81%A6%E3%82%B3%E3%83%B3%E3%83%9D%E3%83%BC%E3%83%8D%E3%83%B3%E3%83%88%E6%A9%9F%E8%83%BD%E3%82%92python%E3%81%8B%E3%82%89%E3%82%B3%E3%83%BC/)
