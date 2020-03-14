symfony
```
アプリケーションの作成
composer create-project symfony/website-skeleton プロジェクト名　（規模が大きい、一般的）
composer create-project symfony/skeleton プロジェクト名 (規模が小さい、あまり一般的でない）
```
``` 
アプリケーションの実行
php bin/console server:run
```
```
コントローラーの作成
cd プロジェクト名
php bin/console make:controller
→コントローラー名を記入　ex)HelloController
```
```
HelloController.php
<?php
namespace App\Controller;


use Symfony\Component\HttpFoundation\Response;


class HelloController
{
    public function index()
    {
        return new Response('Hello Symfony!');
        #=>
    }
}

ルーティングの設定
routes.yamlに記述
hello:
  path: /hello
  controller: App\Controller\HelloController::index
 
 #=> Hello Symfony!
```
```
ルーティングの設定
アノテーション(routes.yamlに記述しない）
<?php
namespace App\Controller;


use Symfony\Component\HttpFoundation\Response;
use Symfony\Component\Routing\Annotation\Route; //ここ追記


class HelloController
{
    /**
     * @Route("/hello", name="hello")
     */
    public function index()
    {
        return new Response('Hello Symfony!');
    }
}
```
```
routeアノテーションとは
＠で始まるコメント文
メソッドやクラスの前に記述する
useで記述が必要！！
/**
 *  @Route(アドレス , name = 名前)
 */
 一行での書き方、冒頭/**末尾*/にないとNG!
 ```
 ```
 HTMLの表示方法
 <?php
namespace App\Controller;


use Symfony\Component\HttpFoundation\Response;
use Symfony\Component\Routing\Annotation\Route;


class HelloController
{
    /**
     * @Route("/hello", name="hello")
     */
    public function index()
    {
        $result = <<< EOM
        <html>
        <head><title>Hello</title></head>
        <body>
        <h1>Hello Symfony!</h1>
        <p>this is Symfony sample page.</p>
        </body>
        </html>
EOM;
        return new Response($result);
    }
}
```
```
抽象クラスの継承（こちらの方が一般的）
AbstractControllerにはよく利用される便利な機能が組み込まれている
<?php
namespace App\Controller;


use Symfony\Bundle\FrameworkBundle\Controller\AbstractController;
use Symfony\Component\HttpFoundation\Response;
use Symfony\Component\Routing\Annotation\Route;


class HelloController extends AbstractController
{
    /**
     * @Route("/hello", name="hello")
     */
    public function index()
    {
        $result = <<< EOM
        <html>
        <head><title>Hello</title></head>
        <body>
        <h1>Hello Symfony!</h1>
        <p>this is Symfony sample page.</p>
        </body>
        </html>
EOM;
        return new Response($result);
    }
}
```
