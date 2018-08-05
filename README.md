# GrasshopperBake-with-Serial-Number  

ユニークな部材を管理するために、連番で名前をつけてファイル書き出しをする。  
手でいちいち Bake して、名前を付けてなんてやるのは面倒なので、自動化させる。  

ghpythonlib.components と、rs.Command() はめっちゃ便利。rhino と Grasshopper と Python のいいとこどりできる。  

---  

### index

- GrasshopperBake-with-Serial-Number.ghx  

  - ListItem  
    - ghpythonlib.components で ListItem コンポーネントを使ってみる  

  - List-Bake   
    - K個のオブジェクトを、0 から K まで、連番で数字を振って STL ファイルに書き出し  
    - For ループでまわす

  - Tree-Bake  
    - U x V 行列を、0_0 から N_M まで、ID を付けて STL ファイルに書き出し  
    - 2重の For ループでまわす  

    ```Python
    num_1, hoge = divmod(i, U)
    str_1 = str(num_1)
    str_2 = str(i%U)

    str_name = str_1 + "_" +str_2
    ```

- List-Bake   
  - 今回の 6x4 = 24で、0 ~ 24 の STL ファイル   

- Tree-Bake  
-   - 今回の 6x4 = 24で、(0, 0) ~ (3, 5) の STL ファイル   

---

### ref  

- [ghpythonlib.componentsをつかってコンポーネント機能をpythonからコール](http://am.d-xx.com/2015/06/04/ghpythonlib-components%E3%82%92%E3%81%A4%E3%81%8B%E3%81%A3%E3%81%A6%E3%82%B3%E3%83%B3%E3%83%9D%E3%83%BC%E3%83%8D%E3%83%B3%E3%83%88%E6%A9%9F%E8%83%BD%E3%82%92python%E3%81%8B%E3%82%89%E3%82%B3%E3%83%BC/)  

- 
