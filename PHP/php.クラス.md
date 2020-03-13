#class
```
プロパティ
class内で持たせる変数
```
```
メソッド
class内で作成した関数
```
```
コンストラクタ
クラスからオブジェクトがnewによって作成される時に自動的に呼び出されるメソッド
コンストラクタの定義は __construct()でする
```
```
<?php
 class Goblin {
 //プロパティ
  public $hp;
  public $mp;
  public $name;
  
  //コンストラクタ
  public function __construct($name) {
    $this->name = "ゴブリン" . $name;
    $this->hp = rand(1,20);
    $this->mp = rand(1,5);
    }
  //メソッド
  public function kougeki() {
    echo "{$this->name}は勇者を攻撃";
  }
 }
$gob1 = new Goblin("A");
 
echo $gob1->name;
echo "<br>";
echo $gob1->hp;
echo "<br>";
echo $gob1->mp;
echo "<br>";
echo $gob1->kougeki();
echo "<br>";
 
?>
#=> ゴブリンA
    17
    3
    ゴブリンAは勇者を攻撃
```
```
class Slime {
  //プロパティ
  public $hp;
  public $mp;
  public $name;
 
  //コンストラクタ
  public function __construct($name) {
    $this->name = $name;
    $this->hp = rand(1,20);
    $this->mp = rand(1,5);
  }
 
  //メソッド
  public function kougeki() {
    echo "{$this->name}は勇者を攻撃";
  }
 
  public function nigeru() {
    echo "{$this->name}は逃げ出した";
  }
 
}
 
$slime1 = new Slime("スライム");
 
echo $slime1->kougeki();
echo "<br>";
echo $slime1->nigeru();
echo "<br>";
#=> スライムは勇者を攻撃
    スライムは逃げ出した
    
----継承----

class HoimiSlime extends Slime {
  public function hoimi() {
    echo "{$this->name}はホイミを使った";
  }
 
  //親クラスのメソッドを上書き（オーバーライド）
  public function nigeru() {
    echo "{$this->name}は飛んで逃げた";
  }
}
 
 
$hslime1 = new HoimiSlime("ホイミスライム");
 
echo $hslime1->kougeki();
echo "<br>";
echo $hslime1->hoimi();
echo "<br>";
echo $hslime1->nigeru();
echo "<br>";
?>
#=> ホイミスライムは勇者を攻撃
    ホイミスライムはホイミを使った
    ホイミスライムは飛んで逃げた
```

