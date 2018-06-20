---
title: Visio ファイル形式をプログラムによって操作します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5f5e2288-7539-41b8-916d-410be028ed9b
description: ''
ms.openlocfilehash: 92ef2c084409dbe017951ff7dfdbf93839ff4b51
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805546"
---
# <a name="manipulate-the-visio-file-format-programmatically"></a>Visio ファイル形式をプログラムによって操作します。

![方法トピック](media/mod_icon_howto.png)
  
Visio 2013 の新しいファイル形式のパッケージを読み取り、パッケージ内の部品を選択、一部のデータを変更および新しいパーツをパッケージに追加する、Visual Studio 2012 でソリューションを作成する方法について説明します。
  
|||
|:-----|:-----|
|**この資料に記載されて**         [Visio ファイル形式の操作の基礎](#vis15_ManipulateFF_Essentials)          [.Vsdx ファイルと新しい Visual Studio ソリューションを作成](#vis15_ManipulateFF_CreateFile)          [パッケージとして Visio 2013 ファイルを開く](#vis15_ManipulateFF_OpenPackage)          [選択しパッケージのパーツをパッケージからの読み取り](#vis15_ManipulateFF_SelectPart)          [選択しパッケージのパーツ内の XML データを変更します。](#vis15_ManipulateFF_ChangeXML)          [ファイル内のデータを再計算](#vis15_ManipulateFF_Recalculate)          [パッケージを新しいパッケージ パーツの追加](#vis15_ManipulateFF_AddNewPart)          [受信確認](#vis15_ManipulateFF_Ackn)          [その他のリソース](#vis15_ManipulateFF_Additional)||
   
## <a name="visio-file-format-manipulation-essentials"></a>Visio ファイル形式の操作の基本
<a name="vis15_ManipulateFF_Essentials"> </a>

Visio の以前のバージョンでは、独自のバイナリ ファイル形式 (.vsd) またはシングル ドキュメント Visio XML 図面ファイル形式 (.vdx) ファイルを保存します。 Visio 2013 には、XML と ZIP のアーカイブ ・ テクノロジーに基づいた新しいファイル形式 (.vsdx) が導入されています。 Visio の以前のバージョンと同様に、ファイルは 1 つのコンテナーに保存されます。 従来のファイルとは異なりただし、新しいファイル形式を開く、読み取り、更新、変更すると、Visio 2013 のアプリケーションを自動化することがなく構築します。 XML を操作することや、 [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx)名前空間の操作に慣れている開発者がすぐに始める新しいファイル形式をプログラムによって操作します。 以前のバージョンの Visio XML 図面形式を使用してきた開発者は、その形式の構造体の多く維持されていますが、新しいファイル形式を検索できます。 
  
この記事で考察プログラムで、Visio 2013 のファイル形式を使用する方法、Microsoft.NET Framework 4.5、C# または Visual Basic、および Visual Studio 2012 を使用します。 Visio 2013 ファイルを開く、ファイル内の文書パーツを選択して、パーツのデータを変更および新しい文書パーツを作成する方法を表示できます。
  
> [!NOTE]
> この資料のコード サンプルでは、 [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) 、 [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx)名前空間のクラスの基本的な知識があることを前提としています。 > この資料では、概念とオープンのパッケージ化規則の用語を理解することも想定しています。 パッケージ、文書パーツまたはパッケージのパーツおよびリレーションシップの概念をいくつかの知識が必要です。 詳細についてを参照してください[OPC: A 新しい標準的なパッケージのデータを](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx)。 > のコードでは、XML を選択するクエリを LINQ (統合言語クエリ) を作成する方法を示します。 多くのコード サンプルは、LINQ クエリの作成のクエリの構文を使用します。 必要な場合は、LINQ のメソッドの構文を使用して、コードで提供される LINQ クエリのいずれかを書き直すことができます。 LINQ クエリ構文とメソッド構文の詳細については、 [LINQ のクエリ構文](http://msdn.microsoft.com/en-us/library/bb397947.aspx)を参照してください > 表 1 は、この資料を使用する前にに精通している必要があります重要なトピックを示します。 
  
**表 1 です。Visio 2013 のファイル形式を操作するための中核となる概念**

|**記事のタイトル**|**説明**|
|:-----|:-----|
|[Visio ファイル形式 (.vsdx) の概要](introduction-to-the-visio-file-formatvsdx.md) <br/> |この概要では、Visio 2013 のファイル形式の主な機能のいくつかについて説明します。 Visio 2013 のファイル形式に適用されていると、開いているパッケージ化の規則 (OPC) を説明します。 また、いくつかの違いは、Visio 2013 のファイル形式と以前の Visio XML 図面ファイル形式 (.vdx) を一覧表示します。  <br/> |
|[OPC: データをパッケージ化するための新しい標準](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx) <br/> |この MSDN マガジンの記事は、Open Packaging Conventions の概念について説明します。  <br/> |
|[オープンなパッケージング規則の基礎](http://msdn.microsoft.com/en-us/library/ee361919.aspx) <br/> [Office (2007) オープン XML ファイル形式の概要](http://msdn.microsoft.com/en-us/library/aa338205.aspx) <br/> |これら 2 つの資料では、Microsoft Office ファイルを開くのパッケージ化の規則を適用されている方法について説明します。 関係のパッケージでの作業し、いくつかのコード サンプルも含まれての説明が含まれます。  <br/> |
   
## <a name="create-a-vsdx-file-and-a-new-visual-studio-solution"></a>.vsdx ファイルと新しい Visual Studio ソリューションを作成する
<a name="vis15_ManipulateFF_CreateFile"> </a>

この資料の手順での作業を開始する前に、Visio 2013 ファイルを開き、操作を作成する必要があります。 この資料のコード例で使用されている図面には、接続されている 2 つの図形で、[基本フローチャート] テンプレートから [開始/終了"の形をしている図形の 1 つで 1 つのページが含まれています。
  
この資料の残りの手順で使用するのに新しい Visio 2013 ファイルを作成するのにには、次の手順を使用します。
  
### <a name="to-create-new-file-in-visio-2013"></a>Visio 2013 で、新しいファイルを作成するには

1. Visio 2013 を開きます。
    
2. **作成**、**カテゴリ**、**フローチャート**、 **[基本フローチャート]** を選択して [基本フローチャート] テンプレートに基づいた新しい文書を作成します。
    
3. **[図形**] ウィンドウからの**開始/終了**図形をキャンバスにドラッグします。 
    
4. 描画キャンバス上の新しい開始/終了図形を選択し、' プロセスの開始] を入力します。
    
5. **[図形**] ウィンドウから **[処理**] 図形をキャンバスにドラッグします。 
    
6. 描画キャンバス上に、新規の [処理] 図形を選択し、いくつかのタスクを実行する' を入力します。
    
7. 開始/終了図形のショートカット メニューは、**ページの 1 つのコネクタを追加**を選択し、図 1 に示すように、カンバス上で、開始/終了プロセスの図形とコネクタを描画します。
    
    **図 1 です。Visio 2013 の簡単な描画**
    
     ![処理図形に接続されている開始/終了図形](media/vis15_SimpleFlowchart.png)
  
8. **ファイル**、**名前を付けて**、**コンピューター**、**デスクトップ**を選択して、ファイルをデスクトップに .vsdx ファイルとして保存します。
    
    **名前を付けて保存**] ダイアログ ボックスで、Visio のパッケージ**ファイル名**] ボックスで入力""を選択**Visio 図面 (\*.vsdx)** **ファイルの種類**の一覧、および [**保存**] ボタンを選択し。 
    
9. ファイルを閉じ、Visio 2013 を閉じます。
    
> [!TIP]
> Visio を開いてファイルが正常に、ファイルに問題がある場合にも。 Visio が通知するすべてのファイルの問題のためには、ファイルのパッケージのレベルでの Visio ファイルを操作するためのソリューションをテストする場合で、ファイル開くときの警告を有効にする必要があります。 > Visio 2013 年で、ファイルを開いている警告を有効にするにはは、**ファイル**、**オプション**の**詳細設定**を選択します。 [**保存/開く**]、[**ファイルを開いている警告を表示する**を選択します。 
  
これらの手順は、「Visio Package.vsdx」ファイルを操作する Windows コンソール アプリケーションを使用します。 Visual Studio 2012 で、新しい Windows コンソール アプリケーションを作成および設定するには、次の手順を使用します。
  
### <a name="to-create-a-new-solution-in-visual-studio-2012"></a>Visual Studio 2012 の新しいソリューションを作成するには

1. [**ファイル**] メニューの [**新規**作成]**プロジェクト**を選択します。
    
2. **新しいプロジェクト**] ダイアログ ボックスでは、 **Visual C#** または**Visual Basic**では、いずれかを展開し、 **Windows****コンソール アプリケーション**を選択し、します。
    
    [**名**] ボックスで、'VisioFileAccessor' を入力して、プロジェクトの場所を選択、 **[OK** ] を選択し。 
    
3. [ **プロジェクト**] メニューの [ **参照の追加**] を選択します。 
    
    **参照マネージャー**ダイアログ ボックスの [**アセンブリ**のでは、**フレームワーク**を選択し、 **System.Xml** 、 **WindowsBase**コンポーネントへの参照を追加します。 
    
4. Program.cs または Module1.vb ファイル、プロジェクトに、次の**using**ディレクティブ (Visual Basic では**Imports**ステートメント) を追加します。 
    
  ```cs
  using System.Xml;
  using System.Xml.Linq;
  using System.IO;
  using System.IO.Packaging;
  using System.Text;
  
  ```

  ```vb
  Imports System.Xml
  Imports System.Xml.Linq
  Imports System.IO
  Imports System.IO.Packaging
  Imports System.Text
  
  ```

5. Program.cs または Module1.vb ファイル (Visual Basic では**Module1** )**プログラム**のクラスの**Main**メソッドの末尾までのコンソール アプリケーションの実行を停止する次のコードを追加する前に、キーを押した。 
    
  ```cs
  // This code stops the execution of the console application
  // so you can read the output.
  Console.WriteLine("Press any key to continue ...");
  Console.ReadKey();
  
  ```

  ```vb
  ' This code stops the execution of the console application
  ' so you can read the output.
  Console.WriteLine("Press any key to continue ...")
  Console.ReadKey()
  ```

## <a name="open-a-visio-2013-file-as-a-package"></a>パッケージとして Visio 2013 ファイルを開く
<a name="vis15_ManipulateFF_OpenPackage"> </a>

ファイル内のデータのいずれかを操作することができます、前に、最初に、 [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx)名前空間内に含まれる[パッケージ](https://msdn.microsoft.com/library/System.IO.Packaging.Package.aspx)オブジェクト内でファイルを開く必要があります。 **パッケージ**オブジェクトは、全体として Visio ファイルを表します。 ファイルのパッケージ内の個々 の文書パーツを選択することを許可するメンバーを公開します。 具体的には、**パッケージ**のクラスは、パッケージとしてファイルを開くに使用する静的な[(文字列、FileMode、FileAccess) の Open](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Open.aspx)メソッドを公開します。 また、一度パッケージを閉じるための[Close()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Close.aspx)メソッドを公開処理を終了します。 
  
> [!TIP]
> 最善の方法としては、**パッケージ**オブジェクトの Visio ファイルを開き、それが終わったときに、ファイルのパッケージを明示的に閉じる必要はありません**を使用して**ブロックを使用します。 **Finally**ブロック内の**catch または finally**構築の**Package.Close**メソッドを明示的に呼び出すことができます。 
  
**Package.Open**メソッドに引数としてパスを渡す、呼び出し元のコードに、**パッケージ**オブジェクトを返す、 [FileInfo](https://msdn.microsoft.com/library/System.IO.FileInfo.aspx)オブジェクトを使用して、「Visio Package.vsdx」ファイルの完全パスを取得するには、次コードを使用します。 
  
### <a name="to-open-a-vsdx-file-as-a-package"></a>.vsdx ファイルをパッケージとして開くには

1. **メイン**の後は、**プログラム**クラス (または Visual Basic では**Module1** ) 内のメソッドは、次のコードを追加します。 
    
  ```cs
  private static Package OpenPackage(string fileName, 
      Environment.SpecialFolder folder)
  {
      Package visioPackage = null;
      // Get a reference to the location 
      // where the Visio file is stored.
      string directoryPath = System.Environment.GetFolderPath(
          folder);
      DirectoryInfo dirInfo = new DirectoryInfo(directoryPath);
      // Get the Visio file from the location.
      FileInfo[] fileInfos = dirInfo.GetFiles(fileName);
      if (fileInfos.Count() > 0)
      {
          FileInfo fileInfo = fileInfos[0];
          string filePathName = fileInfo.FullName;
          // Open the Visio file as a package with
          // read/write file access.
          visioPackage = Package.Open(
              filePathName,
              FileMode.Open,
              FileAccess.ReadWrite);
          }
          // Return the Visio file as a package.
          return visioPackage;
  }
  ```

  ```vb
  Private Function OpenPackage(fileName As String, _
      folder As Environment.SpecialFolder) As Package
      Dim visioPackage As Package = Nothing
      ' Get a reference to the location
      ' where the Visio file is stored.
      Dim directoryPath As String = System.Environment.GetFolderPath( _
          folder)
      Dim dirInfo As DirectoryInfo = New DirectoryInfo(directoryPath)
      ' Get the Visio file from the location.
      Dim fileInfos As FileInfo() = dirInfo.GetFiles(fileName)
      If (fileInfos.Count() > 0) Then
          Dim fileInfo As FileInfo = fileInfos(0)
          Dim filePathName As String = fileInfo.FullName
          ' Open the Visio file as a package 
          ' with read/write access.
          visioPackage = Package.Open( _
              filePathName,
              FileMode.Open,
              FileAccess.ReadWrite)
          End If
      ' Return the Visio file as a package.
      Return visioPackage
  End Function
  
  ```

2. **プログラム**クラス (または Visual Basic では**Module1** ) の**Main**メソッドに次のコードを追加します。 
    
  ```cs
  // Open the Visio file in a Package object.
  using (Package visioPackage = OpenPackage("Visio Package.vsdx", 
      Environment.SpecialFolder.Desktop))
  {
  }
  
  ```

  ```vb
  ' Open the Visio file in a Package object.
  Using visioPackage As Package = OpenPackage("Visio Package.vsdx", _
      Environment.SpecialFolder.Desktop)
  End Using
  
  ```

## <a name="select-and-read-package-parts-from-a-package"></a>パッケージからパッケージ パーツを選択して読み取る
<a name="vis15_ManipulateFF_SelectPart"> </a>

パッケージを開き、Visio 2013 ファイルを作成したら、 **System.IO.Packaging**名前空間に含まれている[PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx)クラスを使用してその中の文書パーツにアクセスできます。 **PackagePart**オブジェクトは、個別にまたはコレクションとしてインスタンス化することができます。 **パッケージ**のクラスでは、 [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx)メソッドと**パッケージ**からの**PackagePart**オブジェクトを取得するための[GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx)メソッドを公開します。 **Package.GetParts**メソッドを実装するその他のコレクションと同様に操作できますし、 [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx)クラスのインスタンスを取得する、 [IEnumerator\<T\>](https://msdn.microsoft.com/library/System.Collections.Generic.IEnumerator`1.aspx)インタ フェースです。 
  
コレクションと**パッケージ**から、 **PackagePartCollection**オブジェクトを取得、 **PackagePart**オブジェクトのコレクションを反復処理して、URI と各**PackagePart のコンテンツ タイプを作成、次の手順でコードを使用してください。** コンソールにします。 
  
### <a name="to-iterate-through-the-package-parts-in-a-package"></a>パッケージ内のパッケージ パーツを反復処理するには

1. 後、 `OpenPackage` **プログラム**クラス (または Visual Basic では**Module1** ) 内のメソッドは、次のコードを追加します。 
    
  ```cs
  private static void IteratePackageParts(Package filePackage)
  {
      
      // Get all of the package parts contained in the package
      // and then write the URI and content type of each one to the console.
      PackagePartCollection packageParts = filePackage.GetParts();
      foreach (PackagePart part in packageParts)
      {
          Console.WriteLine("Package part URI: {0}", part.Uri);
          Console.WriteLine("Content type: {0}", part.ContentType.ToString());
      }
  }
  
  ```

  ```vb
  Private Sub IteratePackageParts(filePackage As Package)
      ' Get all of the package parts contained in the package
      ' and then write the URI and content type of each one to the console.
      Dim packageParts As PackagePartCollection = filePackage.GetParts()
      For Each part In packageParts
          Console.WriteLine("Package part: {0}", part.Uri)
          Console.WriteLine("Content type: {0}", part.ContentType.ToString())
      Next
  End Sub 
  
  ```

2. (Visual Basic では、 **module1 という名前**の**メイン**メソッドの**Using**ブロック)**プログラム**のクラスの**Main**メソッド**を使用して**ブロック内の次のコードを追加します。 
    
  ```cs
  // Write the URI and content type of each package part to the console.
  IteratePackageParts(visioPackage);
  
  ```

  ```vb
  ' Write the URI and content type of each package part to the console.
  IteratePackageParts(visioPackage)
  
  ```

3. F5 キーを選択してソリューションをデバッグします。プログラムの実行が完了したら、任意のキーを選択して終了します。
    
コンソール アプリケーションは、次のような出力を生成します (簡潔にするため、出力の一部が省略されています)。
  
 `Package part URI: /docProps/app.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.extended-properties+xml`
  
 `Package part URI: /docProps/core.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.core-properties+xml`
  
 `Package part URI: /docProps/custom.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.custom-properties+xml`
  
 `Package part URI: /docProps/thumbnail.emv`
  
 `Content type: image/x-emf`
  
 `Package part URI: /visio/document.xml`
  
 `Content type: application/vnd.ms-visio.drawing.main+xml`
  
 `Package part URI: /visio/_rels/document.xml.rels`
  
 `Content type: application/vnd.openxmlformats-package.relationships+xml`
  
 `Package part URI: /_rels/.rels`
  
 `Content type: application/vnd.openxmlformats-package.relationships+xml`
  
 `Press any key to continue …`
  
ほとんどの場合、それらのすべてを反復処理することがなく 1 つの**PackagePart**を選択する必要があります。 **パッケージ**からの**PackagePart**オブジェクトを取得するには、**パッケージ**または別の**PackagePart**の関係を使用します。 Visio 2013 がファイル形式は、ドキュメント パーツの関係について説明する別個のエンティティのリレーションシップ ファイル パッケージまたは 2 つの文書パーツは、相互に関連します。 などの Visio 2013 ファイル パッケージ自体と、Visio 図面の一部に関係があるし、Visio 図面の一部が Windows の一部に関係を持っています。 [PackageRelationship](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationship.aspx)または[PackageRelationshipCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationshipCollection.aspx)のクラスのインスタンスとしては、これらの関係が表されます。 
  
**パッケージ**のクラスは、 **PackageRelationship**または**PackageRelationshipCollection**オブジェクトとして含まれている関係を取得するためのいくつかのメソッドを公開します。 [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx)メソッドを使用するには 1 つの特定の種類の**PackageRelationship**オブジェクトを格納する**PackageRelationshipCollection**オブジェクトをインスタンス化します。 もちろん、 **Package.GetRelationshipsByType**メソッドを使用する場合は、必要なリレーションシップの種類が既にわかっている必要があります。 関係タイプは、XML 名前空間の形式の文字列です。 Visio 文書パーツの関連付けの種類は、たとえば、 http://schemas.microsoft.com/visio/2010/relationships/document。 
  
**パッケージ**または別の**PackagePart**の**PackagePart**の関係さえわかっていれば (つまり、オブジェクトがある、 **PackageRelationship** **PackagePart**するを参照)、使用することができますその**PackagePart**の URI を取得する関係です。 **PackagePart**を返すために**Package.GetPart**メソッドに URI を渡すし。
  
> [!NOTE]
> すれば、特定の**PackagePart**への参照だけで、 **Package.GetPart**メソッドとの**PackagePart**では、URI を使用してパッケージを取得する、部品の関連手順をバイパスします。 ただし、Visio ファイルのパッケージのパッケージの一部は、パッケージ内の既定の場所以外の場所に保存できます。 パッケージの一部が常にすべてのファイルに対して同じ URI であるとは限りません。 > 代わりに、リレーションシップを使用して個々 の**PackagePart**オブジェクトにアクセスするベスト ・ プラクティスを勧めします。 
  
**PackagePart** (Visio 図面の一部) を取得するのに部分を参照する**パッケージ**の**PackageRelationship**を使用して、次の手順を使用します。 
  
### <a name="to-select-a-specific-package-part-in-the-package-by-relationship"></a>リレーションシップによりパッケージ内の特定のパッケージ パーツを選択するには

1. 後、 `IteratePackageParts` **プログラム**クラス (または Visual Basic では**Module1** ) 内のメソッドは、以下のメソッドを追加します。 
    
  ```cs
  private static PackagePart GetPackagePart(Package filePackage, 
      string relationship)
  {
      
      // Use the namespace that describes the relationship 
      // to get the relationship.
      PackageRelationship packageRel = 
          filePackage.GetRelationshipsByType(relationship).FirstOrDefault();
      PackagePart part = null;
      // If the Visio file package contains this type of relationship with 
      // one of its parts, return that part.
      if (packageRel != null)
      {
          // Clean up the URI using a helper class and then get the part.
          Uri docUri = PackUriHelper.ResolvePartUri(
              new Uri("/", UriKind.Relative), packageRel.TargetUri);
          part = filePackage.GetPart(docUri);
      }
      return part;
  }
  
  ```

  ```vb
  Private Function GetPackagePart(filePackage As Package, relationship As String) _
      As PackagePart
      ' Use the namespace that describes the relationship 
      ' to get the relationship.
      Dim packageRel As PackageRelationship = 
          filePackage.GetRelationshipsByType(relationship).FirstOrDefault()
      Dim part As PackagePart = Nothing
      ' If the Visio file package contains this type of relationship with 
      ' one of its parts, return that part.
      If Not IsNothing(packageRel) Then
          ' Clean up the URI using a helper class and then get the part.
          Dim docUri = PackUriHelper.ResolvePartUri( _
              New Uri("/", UriKind.Relative), packageRel.TargetUri)
          part = filePackage.GetPart(docUri)
      End If
      Return part
  End Function
  
  ```

2. **プログラム**のクラス (Visual Basic では、 **module1 という名前**の**メイン**メソッドの**Using**ブロック) の**Main**メソッド**を使用して**ブロック内のコードを次のコードに置き換えます。 
    
  ```cs
  // Get a reference to the Visio Document part contained in the file package.
  PackagePart documentPart = GetPackagePart(visioPackage, 
      "http://schemas.microsoft.com/visio/2010/relationships/document");
  
  ```

  ```vb
  ' Get a reference to the Visio Document part contained in the file package.
  Dim documentPart As PackagePart = GetPackagePart(visioPackage, _
      "http://schemas.microsoft.com/visio/2010/relationships/document")
  
  ```

前述のように、他の**PackagePart**オブジェクトとの関係を使用して**PackagePart**オブジェクトを取得することもできます。 **PackagePart**オブジェクトのほとんどの複雑な Visio 図面では、**パッケージ**との関係を持っていないために、このことが重要です。 たとえば、ファイル パッケージ (つまり、/visio/pages/page1.xml) 内の個々 のページのコンテンツ部品では、ファイルのパッケージ自体ではなく、ページのインデックスの一部 (つまり、/visio/pages/pages.xml) に関係があります。 個々 のページの正確な URI のパッケージをお持ちでない場合は、オブジェクトへの参照を取得するページのインデックスの一部の関係を使用できます。
  
**PackagePart**クラスは、 **PackageRelationship**オブジェクトの 1 つだけの種類を含む**PackageRelationshipCollection**オブジェクトを返すために使用できる[GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx)メソッドを公開します。 **PackageRelationshipCollection**を作成したら、 **PackageRelationship**コレクションから必要があるし、 **PackagePart**オブジェクトを参照することを選択できます。 
  
(からの**PackageRelationship**オブジェクトを取得) の関係を使用して、**パッケージ**からの**PackagePart**を取得する次のコードを使用して別の**PackagePart**。
  
### <a name="to-select-a-specific-package-part-through-its-relationship-to-another-package-part"></a>別のパッケージ パーツとのリレーションシップを利用して特定のパッケージ パーツを選択するには

1. 後、 `GetPackagePart` **プログラム**クラス (または Visual Basic では**Module1** ) 内のメソッドは、次のオーバー ロード メソッドを追加します。 
    
  ```cs
  private static PackagePart GetPackagePart(Package filePackage, 
      PackagePart sourcePart, string relationship)
  {
      // This gets only the first PackagePart that shares the relationship
      // with the PackagePart passed in as an argument. You can modify the code
      // here to return a different PackageRelationship from the collection.
      PackageRelationship packageRel = 
          sourcePart.GetRelationshipsByType(relationship).FirstOrDefault();
      PackagePart relatedPart = null;
      if (packageRel != null)
      {
          // Use the PackUriHelper class to determine the URI of PackagePart
          // that has the specified relationship to the PackagePart passed in
          // as an argument.
          Uri partUri = PackUriHelper.ResolvePartUri(
              sourcePart.Uri, packageRel.TargetUri);
          relatedPart = filePackage.GetPart(partUri);
      }
      return relatedPart;
  }
  
  ```

  ```vb
  Private Function GetPackagePart(filePackage As Package, 
      sourcePart As PackagePart, relationship As String) As PackagePart
      ' This gets only the first PackagePart that shares the relationship
      ' with the PackagePart passed in as an argument. You can modify the
      ' code to return a different PackageRelationship from the collection.
      Dim packageRel As PackageRelationship = sourcePart. _
          GetRelationshipsByType(relationship).FirstOrDefault()
      Dim relatedPart As PackagePart = Nothing
      If Not IsNothing(packageRel) Then
          ' Use the PackUriHelper class to determine the URI of the 
          ' PackagePart that has the specified relationship to the 
          ' PackagePart passed in as an argument.
          Dim partUri As Uri = PackUriHelper.ResolvePartUri( _
              sourcePart.Uri, packageRel.TargetUri)
          relatedPart = filePackage.GetPart(partUri)
      End If
      Return relatedPart
  End Function
  ```

2. 前の手順**を使用して**、 **Main**メソッド内のブロック コードの下にある**プログラム**のクラス (Visual Basic では、 **module1 という名前**の**メイン**メソッドの**Using**ブロック) に次のコードを追加します。 (前の手順で追加したコードを削除しない)。 
    
  ```cs
  // Get a reference to the collection of pages in the document, 
  // and then to the first page in the document.
  PackagePart pagesPart = GetPackagePart(visioPackage, documentPart, 
      "http://schemas.microsoft.com/visio/2010/relationships/pages");
  PackagePart pagePart = GetPackagePart(visioPackage, pagesPart, 
      "http://schemas.microsoft.com/visio/2010/relationships/page");
  
  ```

  ```vb
  ' Get a reference to the collection of pages in the document,
  ' and then to the first page in the document.
  Dim pagesPart As PackagePart = GetPackagePart(visioPackage, documentPart, _
      "http://schemas.microsoft.com/visio/2010/relationships/pages") 
  Dim pagePart As PackagePart = GetPackagePart(visioPackage, pagesPart, _
      "http://schemas.microsoft.com/visio/2010/relationships/page") 
  ```

ドキュメントの一部に含まれている XML に変更を行うことができます、前に、まず[XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx)クラスまたは[XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx)クラスを使用して、XML を読み取ることができるオブジェクトを XML ドキュメントをロードする必要があります。 両方のクラスは、XML ドキュメント内に含まれる XML 要素を選択するなどのタスクのメソッドを公開します。属性を書き込み、作成、読み取り、新しい XML 要素を文書に挿入します。 
  
、2 つの**XDocument**クラスでは、LINQ を使用して XML のクエリを実行できます。 LINQ では、簡単に選択する個々 の要素の XML ドキュメントからクエリの作成ではなく、コレクション内の要素のすべてを反復処理してテストに必要な要素の。 これらの理由から、この資料では、次の手順は、XML を操作するため、 **XDocument**クラスおよび**System.Xml.Linq**名前空間の他のクラスを使用します。 
  
次の手順を使用して、 **XDocument**オブジェクト内の XML ドキュメントとして、 **PackagePart**を開きます。 
  
### <a name="to-read-the-xml-in-a-package-part"></a>パッケージ パーツ内の XML を読み取るには

1. 最後のオーバー ロードした後、 `GetPackagePart` **プログラム**クラス (または Visual Basic では**Module1** ) 内のメソッドは、以下のメソッドを追加します。 
    
  ```cs
  private static XDocument GetXMLFromPart(PackagePart packagePart)
  {
      XDocument partXml = null;
      // Open the packagePart as a stream and then 
      // open the stream in an XDocument object.
      Stream partStream = packagePart.GetStream();
      partXml = XDocument.Load(partStream);
      return partXml;
  }
  ```

  ```vb
  Private Function GetXMLFromPart(packagePart As PackagePart) As XDocument
      Dim partXml As XDocument = Nothing
      ' Open the packagePart as a stream and then
      ' open the stream in an an XDocument object.
      Dim partStream As Stream = packagePart.GetStream()
      partXml = XDocument.Load(partStream)
      Return partXml
  End Function
  ```

2. 前の手順**を使用して**、 **Main**メソッド内のブロック コードの下にある**プログラム**のクラス (Visual Basic では、 **module1 という名前**の**メイン**メソッドの**Using**ブロック) に次のコードを追加します。 
    
  ```cs
  // Open the XML from the Page Contents part.
  XDocument pageXML = GetXMLFromPart(pagePart);
  ```

  ```vb
  ' Open the XML from the Page Contents part.
  Dim pageXML As XDocument = GetXMLFromPart(pagePart)
  ```

## <a name="select-and-change-xml-data-in-a-package-part"></a>パッケージ パーツ内の XML データを選択して変更する
<a name="vis15_ManipulateFF_ChangeXML"> </a>

**XDocument**オブジェクトへのドキュメントの一部をロードする XML 要素を選択し、XML ドキュメントに変更を加えるに LINQ を使用することができます。 XML データを変更、追加またはデータを削除して文書の一部に XML ドキュメントを保存できます。 
  
Visio ファイル形式を操作するための最も一般的なタスクを選択する特定の XML 要素または要素のコレクションのドキュメント。 **System.Xml.Linq**名前空間には、XML 要素を表す、 [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx)クラスが含まれています。 **XElement**クラスでは、(例) として **"入力規則"** の要素を個々 の**図形**要素より細かいレベルでの Visio ファイルに含まれるデータにアクセスできます。 
  
**XDocument** (ページの内容の一部を含む) からの**図形**要素を選択して、特定の**図形**要素を選択するのには、次のコードを使用します。 
  
### <a name="to-select-a-specific-element-in-a-package-part"></a>パッケージ パーツ内の特定の要素を選択するには

1. 後、 `GetXMLFromPart` **プログラム**クラス (または Visual Basic では**Module1** ) 内のメソッドは、以下のメソッドを追加します。 
    
  ```cs
  private static IEnumerable<XElement> GetXElementsByName(
      XDocument packagePart, string elementType)
  {
      // Construct a LINQ query that selects elements by their element type.
      IEnumerable<XElement> elements = 
          from element in packagePart.Descendants() 
          where element.Name.LocalName == elementType 
          select element;
      // Return the selected elements to the calling code.
      return elements.DefaultIfEmpty(null);
  }
  
  ```

  ```vb
  Private Function GetXElementsByName(partXML As XDocument, _
      elementType As String) As IEnumerable(Of XElement)
      ' Construct a LINQ query that selects elements by their element type.
      Dim elements As IEnumerable(Of XElement) =
          From element In partXML.Descendants()
          Where element.Name.LocalName = elementType
          Select element
      ' If there aren't any elements of the specified type
      ' in the document, return Nothing to the calling code.
      Return elements.DefaultIfEmpty(Nothing)
  End Function
  ```

2. 後、`GetXElementsByName`から前の手順では、**プログラム**のクラス (または Visual Basic では**Module1** ) 内のメソッドは、以下のメソッドを追加します。 
    
  ```cs
  private static XElement GetXElementByAttribute(IEnumerable<XElement> elements,
      string attributeName, string attributeValue) 
  {
      // Construct a LINQ query that selects elements from a group
      // of elements by the value of a specific attribute.
      IEnumerable<XElement> selectedElements = 
          from el in elements
          where el.Attribute(attributeName).Value == attributeValue
          select el;
      // If there aren't any elements of the specified type
      // with the specified attribute value in the document,
      // return null to the calling code.
      return selectedElements.DefaultIfEmpty(null).FirstOrDefault();
  }
  ```

  ```vb
  Private Function GetXElementByAttribute(elements As IEnumerable(Of XElement), _
      attributeName As String, attributeValue As String) As XElement
      ' Construct a LINQ query that selects elements from a group
      ' of elements by the value of a specific attribute.
      Dim selectedElements As IEnumerable(Of XElement) =
          From el In elements
          Where el.Attribute(attributeName).Value = attributeValue
          Select el
      ' If there aren't any elements of the specified type 
      ' with the specified attribute value in the document,
      ' return Nothing to the calling code.
      Return selectedElements.DefaultIfEmpty(Nothing).FirstOrDefault()
  End Function
  
  ```

3. 前の手順**を使用して**、 **Main**メソッド内のブロック コードの下にある**プログラム**のクラス (Visual Basic では、 **module1 という名前**の**メイン**メソッドの**Using**ブロック) に次のコードを追加します。 
    
  ```cs
  // Get all of the shapes from the page by getting
  // all of the Shape elements from the pageXML document.
  IEnumerable<XElement> shapesXML = GetXElementsByName(pageXML, "Shape");
  // Select a Shape element from the shapes on the page by 
  // its name. You can modify this code to select elements
  // by other attributes and their values.
  XElement startEndShapeXML = 
      GetXElementByAttribute(shapesXML, "NameU", "Start/End");
  
  ```

  ```vb
  ' Get all of the shapes from the page by getting
  ' all of the Shape elements from the pageXML document.
  Dim shapesXML As IEnumerable(Of XElement) = GetXElementsByName( _
      pageXML, "Shape")
  ' Select a Shape element from the shapes on the page by
  ' its name. You can modify this code to select elements
  ' by other attributes and their values.
  Dim startEndShapeXML As XElement = GetXElementByAttribute( _
      shapesXML, "NameU", "Start/End")
  ```

**XDocument**オブジェクト内に含まれる**XElement**オブジェクトへの参照を受けた場合は、いったんその他の XML データと同じように操作して、Visio ファイルに含まれるデータを変更できるため、します。 などの図形は、Visio で開いたときにテキストを持つ、対応する**図形**要素には少なくとも 1 つの**テキスト**要素が含まれます。 その**テキスト**要素の値を変更すると、Visio でファイルを表示したときに図形のテキストが変更されます。 
  
「プロセスの開始」から開始/終了図形内テキストを変更するには、**プログラム**のクラス (Visual Basic では、 **module1 という名前**の**メイン**メソッドの**Using**ブロック) の**Main**メソッド**を使用して**ブロックを次のコードを追加します。スタート] ボタンを処理します。 
  
```cs
// Query the XML for the shape to get the Text element, and
// return the first Text element node.
IEnumerable<XElement> textElements = from element in startEndShapeXML.Elements()
                               where element.Name.LocalName = "Text"
                               select element;
XElement textElement = textElements.ElementAt(0);
// Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process");

```

```vb
' Query the XML for the shape to get the Text element, and
' return the first Text element node.
Dim textElements As IEnumerable(Of XElement) =
    From element In startEndShapeXML.Elements()
    Where element.Name.LocalName = "Text"
    Select element
Dim textElement As XElement = textElements.ElementAt(0)
' Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process")

```

> [!CAUTION]
> 前のコード例では、既存の図形のテキストと置換に使用する文字列の文字の同じ数であります。 LINQ クエリが返される要素をこのケースでは、テキスト ノード) の最後の子ノードの値を変更することにも注意してください。 これは、は、**テキスト**要素の子である**cp**要素の設定を変更することを避けるために行われます。 > が不安定になるファイル**のテキスト**要素のすべての子を上書きすることによって図形のテキストをプログラムで変更する場合に考えられる。 上記の例のようには、テキストの書式設定は、ファイル内の**テキスト**要素の下で**cp**要素によって表されます。 書式設定の定義は、親**セクション**要素に格納されます。 これら 2 つの情報に不整合が生じる、し、ファイルは正常に動作しない可能性があります。 Visio は、多くの矛盾を回復させますが、ファイルの最終的な動作を制御することができるように、プログラムで変更が矛盾がないことを確認することをお勧めします。 
  
ドキュメント パーツの XML に変更を加える場合、その変更内容はメモリ内のみに存在します。ファイル内に変更を保持するには、ドキュメント パーツに XML を戻して保存する必要があります。
  
パッケージの一部に戻る、XML を記述するのに[XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx)クラスと[XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx)クラスを使用するコードを次にします。 [Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx)メソッドを使用するには、一部では、 **XmlWriter**に XML を保存すると、 **XmlWriterSettings**クラスを使用するエンコードの種類を指定するなど、出力をより細かく制御します。 **XDocument**クラスでは、 **XmlWriter**オブジェクトを取得し、XML をストリームに書き込むための[WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx)メソッドを公開します。 
  
Visio のページからページの内容の一部に XML を保存するのにには、次の手順を使用します。
  
### <a name="to-save-the-changed-xml-back-to-the-package"></a>変更した XML をパッケージに戻して保存するには

1. 後、`GetXElementByAttribute`から前の手順では、**プログラム**のクラス (または Visual Basic では**Module1** ) 内のメソッドは、以下のメソッドを追加します。 
    
  ```cs
  private static void SaveXDocumentToPart(PackagePart packagePart, 
      XDocument partXML)
  {
      
      // Create a new XmlWriterSettings object to 
      // define the characteristics for the XmlWriter
      XmlWriterSettings partWriterSettings = new XmlWriterSettings();
      partWriterSettings.Encoding = Encoding.UTF8;
      // Create a new XmlWriter and then write the XML
      // back to the document part.
      XmlWriter partWriter = XmlWriter.Create(packagePart.GetStream(),
          partWriterSettings);
      partXML.WriteTo(partWriter);
      // Flush and close the XmlWriter.
      partWriter.Flush();
      partWriter.Close();
  }
  ```

  ```vb
  Private Sub SaveXDocumentToPart(packagePart As PackagePart, _
      partXML As XDocument)
      ' Create a new XmlWriterSettings object to 
      ' define the characteristics for the XmlWriter.
      Dim partWriterSettings As XmlWriterSettings = New XmlWriterSettings()
      partWriterSettings.Encoding = Encoding.UTF8
      ' Create a new XmlWriter and then write the XML
      ' back to the document part.
      Dim partWriter As XmlWriter = XmlWriter.Create(packagePart.GetStream())
      partXML.WriteTo(partWriter)
      ' Flush and close the XmlWriter.
      partWriter.Flush()
      partWriter.Close()
  End Sub
  ```

2. 前の手順**を使用して**、 **Main**メソッド内のブロック コードの下にある**プログラム**のクラス (Visual Basic では、 **module1 という名前**の**メイン**メソッドの**Using**ブロック) に次のコードを追加します。 
    
  ```cs
  // Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML);
  
  ```

  ```vb
  ' Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML)
  
  ```

3. F5 キーを選択してソリューションをデバッグします。プログラムの実行が完了したら、任意のキーを選択して終了します。
    
4. Visio 2013 では、Visio の Package.vsdx ファイルを開きます。 
    
この時点で開始/終了図形にテキスト「Start process」が含まれているはずです。
  
## <a name="recalculate-data-in-the-file"></a>ファイル内のデータを再計算する
<a name="vis15_ManipulateFF_Recalculate"> </a>

ファイル内のデータをいくつかの変更には、Visio ファイルを開くときにドキュメントを再計算が必要です。 Visio では、図については、図形の関係の特に多くのロジックが用意されています (つまりと 1 つの図形に依存別) の図形を接続するとします。 カスタム ロジックに基づいて、データのいずれかが変更された場合、Visio はすべてのファイルに影響を受ける集計データに変更を反映する必要があります。 
  
Visio 2013 のファイル形式には、ファイル内のデータを再計算するために使用できる技術のいくつかが含まれています。 3 種類の Visio のファイルとそれを行う方法を再計算する必要があるかどうかを決定する際に考慮する必要があるシナリオがあります。
  
- データへの変更は、ファイル形式でその他の値には影響しません。 Visio ドキュメントを再計算するために、追加の手順を追加する必要はありません。 既に示したように、ドキュメントを再計算することがなく多くの場合、図形のテキストを変更できます。
    
- データへの変更は、XML 内のシェイプ シート セルの値を変更して、このデータに依存するその他のシェイプ シートの値があります。 この例では、XML 処理命令が ( [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx)のクラスを使用する) に変更されている**セル**要素を追加する必要があります。 たとえば、図形の**ThemeIndex**セルでは、図形に含まれているいくつか他のシェイプ シート セルの値に影響します。 ファイル自体 ("ThemeIndex"の**N**値を持つ**セル**要素など) に**ThemeIndex**のセルを変更する場合は、従属変数の値が更新されるように**セル**要素に処理命令を追加する必要があります。. 
    
- データへの変更には、コネクタまたは接続ポイントの位置が影響します。 別の状況は、[シェイプ シートのデータに多くの変更がありますし (それぞれの変更については、個々 の処理を追加するのではなく) 1 つの命令で文書全体を再計算するときです。 ここで開いたときにドキュメント全体を再計算するのには Visio に指示できます。 カスタム ファイル プロパティ パーツに**RecalcDocument**プロパティを追加することによってこれを行う (または docProps/custom.xml) の Visio のパッケージです。 位置または接続されている図で図形のサイズを調整することは、この種のシナリオの例です。 
    
    パフォーマンスの観点からは、このシナリオが最もコストがかかるオプションであることに留意してください。
    
同じ**図形**の場合は、他の**セル**要素の新しい値が再計算する必要があるか、**図形**の要素に**セル**要素を挿入するのには次の手順を使用します。 新しい**セル**要素には、いくつかローカルの再計算を実行する必要のある Visio に通知するために、子要素として処理命令が含まれています。 
  
### <a name="to-recalculate-values-for-a-single-shape"></a>1 つの図形の値を再計算するには

1. 前の 2 つの例のコードに置き換えます (図形のテキストとの呼び出しを変更する`SaveXDocumentToPart`) ( **Using**ブロックで、 **module1 という名前**の**Main**メソッドの**プログラム**のクラスの**Main**メソッド**を使用して**ブロックでVisual Basic) で次のコードにします。 
    
  ```cs
  // Insert a new Cell element in the Start/End shape that adds an arbitrary
  // local ThemeIndex value. This code assumes that the shape does not 
  // already have a local ThemeIndex cell.
  startEndShapeXML.Add(new XElement("Cell",
      new XAttribute("N", "ThemeIndex"),
      new XAttribute("V", "25"),
      new XProcessingInstruction("NewValue", "V")));
  // Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML);
  
  ```

  ```vb
  ' Insert a new Cell element in the shape that adds an arbitrary local
  ' ThemeIndex value. This code assumes that the shape does not
  ' alrady have a local ThemeIndex cell.
  startEndShapeXML.Add(New XElement("Cell", _
      New XAttribute("N", "ThemeIndex"),
      New XAttribute("V", "25"),
      New XProcessingInstruction("NewValue", "V")))
  ' Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML)
  
  ```

2. F5 キーを選択してソリューションをデバッグします。プログラムの実行が完了したら、任意のキーを選択して終了します。
    
3. Visio 2013 では、Visio の Package.vsdx ファイルを開きます。 開始/終了図形の塗りつぶしの色ができました。
    
図形の色は、 **ThemeIndex**のセルの値に依存しています: アクティブなテーマの形状を継承することを決定します。 前の例では、図形 ( **ThemeIndex**セルは、「25」の値に設定されます)、別のテーマを継承するように設定されています。 処理命令では、図形のテキストの色を使用しないかどうかは- **ThemeIndex**セルでも影響を受けるが、再計算されていません。 図形の塗りつぶしの色を白に変更は、そのテキストは白のまま、テキストを読み取り不可能なままです。 また、処理命令は、それがないこと Visio が図形の更新後で、図形の書式設定の値を予期しない更新することが不安定な状態に残します。 
  
(たとえば、接続されている図形の位置を変更して、そのため、強制的に再ルーティングするコネクタなど)、ドキュメントを再計算するのには Visio が必要なファイル内のデータを変更する場合は、Visio ファイルに再命令を追加する必要があります。 命令を作成するには、Visio ファイルのパッケージのファイルのプロパティをカスタム部分の XML を"RecalcDocument"の**名前**の属性値を持つ**プロパティ**要素を追加します。 最善の方法としては、"RecalcDocument"の命令がファイルに登録されていない既にことを確認するカスタム ファイル プロパティの一部を参照してください。 
  
前の例と、[開始/終了] 図形の **[piny]** セルの値を変更するのにには、次のコードを使用します。 コードは、 **N**属性の値を使用しての**XElement**オブジェクトとして **[piny]** セルのデータを含む**セル**要素を選択します。 コードは、Visio ファイルのカスタム ファイル プロパティ パーツにし、再計算の命令を追加します。 
  
> [!NOTE]
> このコードに依存しています、`GetPackagePart`と`SaveXDocumentToPart`メソッドが以前に作成します。 
  
### <a name="to-recalculate-the-entire-document-when-it-is-opened"></a>ドキュメントが開いている場合にそのドキュメント全体を再計算するには

1. 後、`SaveXDocumentToPart`から前の手順では、**プログラム**のクラス (または Visual Basic では**Module1** ) 内のメソッドは、以下のメソッドを追加します。 
    
  ```cs
  private static void RecalcDocument(Package filePackage)
  {
      // Get the Custom File Properties part from the package and
      // and then extract the XML from it.
      PackagePart customPart = GetPackagePart(filePackage, 
          "http://schemas.openxmlformats.org/officeDocument/2006/relationships/" + 
          "custom-properties");
      XDocument customPartXML = GetXMLFromPart(customPart);
      // Check to see whether document recalculation has already been 
      // set for this document. If it hasn't, use the integer
      // value returned by CheckForRecalc as the property ID.
      int pidValue = CheckForRecalc(customPartXML);
      if (pidValue > -1)
      {
          XElement customPartRoot = customPartXML.Elements().ElementAt(0);
          // Two XML namespaces are needed to add XML data to this 
          // document. Here, we're using the GetNamespaceOfPrefix and 
          // GetDefaultNamespace methods to get the namespaces that 
          // we need. You can specify the exact strings for the 
          // namespaces, but that is not recommended.
          XNamespace customVTypesNS = customPartRoot.GetNamespaceOfPrefix("vt");
          XNamespace customPropsSchemaNS = customPartRoot.GetDefaultNamespace();
          // Construct the XML for the new property in the XDocument.Add method.
          // This ensures that the XNamespace objects will resolve properly, 
          // apply the correct prefix, and will not default to an empty namespace.
          customPartRoot.Add(
              new XElement(customPropsSchemaNS + "property",
                  new XAttribute("pid", pidValue.ToString()),
                  new XAttribute("name", "RecalcDocument"),
                  new XAttribute("fmtid", 
                      "{D5CDD505-2E9C-101B-9397-08002B2CF9AE}"),
                  new XElement(customVTypesNS + "bool", "true")
              ));
      }
      // Save the Custom Properties package part back to the package.
      SaveXDocumentToPart(customPart, customPartXML);
  }
  ```

  ```vb
  Private Sub RecalcDocument(filePackage As Package)
          ' Get the Custom File Properties part from the package and
          ' then extract the XML from it.
          Dim customPart As PackagePart = GetPackagePart(filePackage, _
              "http://schemas.openxmlformats.org/officeDocument/2006/" + _
              "relationships/custom-properties")
          Dim customPartXML As XDocument = GetXMLFromPart(customPart)
          ' Check to see whether document recalculation has already been
          ' set for this document. If it hasn't, use the integer
          ' value returned by CheckForRecalc as the property ID.
          Dim pidValue As Integer = CheckForRecalc(customPartXML)
          If (pidValue > 1) Then
              Dim customPartRoot As XElement = _
                  customPartXML.Elements().ElementAt(0)
              ' Two XML namespaces are needed to add XML data to this 
              ' document. Here, we're using the GetNamespaceOfPrefix and
              ' GetDefaultNamespace methods to get the namespaces that
              ' we need. You can specify the exact strings for the 
              ' namespaces, but that is not recommended.
              Dim customVTypesNS As XNamespace = _
                  customPartRoot.GetNamespaceOfPrefix("vt")
              Dim customPropsSchemaNS As XNamespace = _
                  customPartRoot.GetDefaultNamespace()
              ' Contruct the XML for the new property in the XDocument.Add
              ' method. This ensures that the XML namespaces resolve 
              ' properly, apply the correct prefix, and do not default to 
              ' an empty namespace.
              customPartRoot.Add( _
                  New XElement(customPropsSchemaNS + "property", _
                      New XAttribute("pid", pidValue.ToString()), _
                      New XAttribute("name", "RecalcDocument"), _
                      New XAttribute("fmtid", _
                          "{D5CDD505-2E9C-101B-9397-08002B2CF9AE}"), _
                      New XElement(customVTypesNS + "bool", "true") _
              ))
          ' Save the Custom Properties package part back to the package.
          SaveXDocumentToPart(customPart, customPartXML)
          End If
      End Sub
  ```

2. 後、`RecalcDocument`から前の手順では、**プログラム**のクラス (または Visual Basic では**Module1** ) 内のメソッドは、以下のメソッドを追加します。 
    
  ```cs
  private static int CheckForRecalc(XDocument customPropsXDoc) 
  {
      
      // Set the inital pidValue to -1, which is not an allowed value.
      // The calling code tests to see whether the pidValue is 
      // greater than -1.
      int pidValue = -1;
      // Get all of the property elements from the document. 
      IEnumerable<XElement> props = GetXElementsByName(
          customPropsXDoc, "property");
      // Get the RecalcDocument property from the document if it exists already.
      XElement recalcProp = GetXElementByAttribute(props, 
          "name", "RecalcDocument");
      // If there is already a RecalcDocument instruction in the 
      // Custom File Properties part, then we don't need to add another one. 
      // Otherwise, we need to create a unique pid value.
      if (recalcProp != null)
      {
          return pidValue;
      }
      else
      {
          // Get all of the pid values of the property elements and then
          // convert the IEnumerable object into an array.
          IEnumerable<string> propIDs = 
              from prop in props
              where prop.Name.LocalName == "property"
              select prop.Attribute("pid").Value;
          string[] propIDArray = propIDs.ToArray();
          // Increment this id value until a unique value is found.
          // This starts at 2, because 0 and 1 are not valid pid values.
          int id = 2;
          while (pidValue == -1)
          {
              if (propIDArray.Contains(id.ToString()))
              {
                  id++;
              }
              else
              {
                  pidValue = id;
              }
          }
      }
      return pidValue;
  }
  
  ```

  ```vb
  Private Function CheckForRecalc(customPropsXDoc As XDocument) As Integer
      ' Set the initial pidValue to -1, which is not an allowed value. 
      ' The calling code test to see whether the pidValue is
      ' greater than -1.
      Dim pidValue As Integer = -1
      ' Get all of the property elements from the document.
      Dim props As IEnumerable(Of XElement) = GetXElementsByName( _
          customPropsXDoc, "property")
      ' Get the RecalcDocument property from the document if 
      ' it exists already.
      Dim recalcProp As XElement = GetXElementByAttribute(props, _
          "name", "RecalcDocument")
      ' If there is already a RecalcDocument instruction in the 
      ' Custom File Properties part, then we don't need another one.
      ' Otherwise, we need to create a unique pid value.
      If Not IsNothing(recalcProp) Then
          Return pidValue
      Else
          ' Get all of the pid values of the proeprty elements and then
          ' convert the IEnumerable object into an array.
          Dim propIDs As IEnumerable(Of String) = _
          From prop In props
          Where prop.Name.LocalName = "property"
          Select prop.Attribute("pid").Value
          Dim propIDArray As String() = propIDs.ToArray()
          ' Increment this id value until a unique value is found.
          ' This starts at 2, because 0 and 1 are not valid pid values.
          Dim id As Integer = 2
          While (pidValue = -1)
              If (propIDArray.Contains(id.ToString())) Then
                  id = id + 1
              Else
                  pidValue = id
              End If
          End While
      End If
      Return pidValue
  End Function
  ```

3. (Visual Basic では、 **module1 という名前**の**メイン**メソッドの**Using**ブロック)、**プログラム**のクラスの**Main**メソッド内に、 **using**ブロックの前の例のコードを次のコードに置き換えます。 
    
  ```cs
  // Change the shape's horizontal position on the page 
  // by getting a reference to the Cell element for the PinY 
  // ShapeSheet cell and changing the value of its V attribute.
  XElement pinYCellXML = GetXElementByAttribute(
      startEndShapeXML.Elements(), "N", "PinY");
  pinYCellXML.SetAttributeValue("V", "2");
  // Add instructions to Visio to recalculate the entire document
  // when it is next opened.
  RecalcDocument(visioPackage);
  // Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML);
  
  ```

  ```vb
  ' Change the shape's horizontal position on the page
  ' by getting a reference to the Cell element for the PinY
  ' ShapeSheet cell and changing the value of its V attribute.
  Dim pinYCellXML As XElement = GetXElementByAttribute(
      startEndShapeXML.Elements(), "N", "PinY")
  pinYCellXML.SetAttributeValue("V", "2")
  ' Add instructions to Visio to recalculate the entire document
  ' when it is next opened.
  RecalcDocument(visioPackage)
  ' Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML)
  
  ```

4. F5 キーを選択してソリューションをデバッグします。プログラムの実行が完了したら、任意のキーを選択して終了します。
    
5. Visio 2013 では、Visio の Package.vsdx ファイルを開きます。 
    
開始/終了図形には、図面の下端からの 2 インチがはずです。 開始/終了図形と、[処理] 図形間のコネクタは、レイアウトの変更に対応するために再ルーティングがある必要があります。 **RecalcDocument**プロパティは、ファイルに追加されていませんが、図形の位置が変更されていること、ですが、コネクタは図形の新しい場所に再ルーティングがありません。 
  
## <a name="add-a-new-package-part-to-a-package"></a>新しいパッケージ パーツをパッケージに追加する
<a name="vis15_ManipulateFF_AddNewPart"> </a>

新しいドキュメント パーツをパッケージに追加ファイルのパッケージを変更するための最も一般的なシナリオの 1 つです。 たとえば、パッケージにコンテンツを追加することで図面にページを追加する場合は、ページの内容の一部をパッケージに追加する必要があります。 
  
次のように、パッケージに新しいパーツを追加するプロセスは簡単です。 
  
1. **PackagePart**のデータを使用して XML ドキュメントを作成します。 XML 名前空間を作成する XML ドキュメントの特定の種類のスキーマを管理するには特に注意する必要があります。
    
2. XML が含まれているし、**パッケージ**内の場所にファイルを保存する新しいファイルを作成するとします。
    
3. 新しい**PackagePart**や**パッケージ**またはその他の**PackagePart**オブジェクトの間で必要な関係を作成します。 
    
4. 新しいパーツを参照する必要がある既存のパーツを更新します。たとえば、新しいページ コンテンツ パーツ (新しいページ) をファイルに追加する場合は、ページ インデックス パーツ (/visio/pages/pages.xml ファイル) を更新し、新しいページに関する正しい情報を組み込む必要もあります。
    
Visio ファイルに新しいリボン機能拡張パーツを作成するのにには、次の手順を使用します。 新しいリボンの機能拡張の一部は、1 つのボタンを含む 1 つのグループを使用して新しいタブをリボンに追加します。
  
### <a name="to-create-a-new-package-part"></a>新しいパッケージ パーツを作成するには

1. 後、`CheckForRecalc`から前の手順では、**プログラム**のクラス (または Visual Basic では**Module1** ) 内のメソッドは、以下のメソッドを追加します。 
    
  ```cs
  private static XDocument CreateCustomUI()
  {
      // Add a new Custom User Interface document part to the package.
      // This code adds a new CUSTOM tab to the ribbon for this
      // document. The tab has one group that contains one button.
      XNamespace customUINS = 
          "http://schemas.microsoft.com/office/2006/01/customui";
      XDocument customUIXDoc = new XDocument(
          new XDeclaration("1.0", "utf-8", "true"),
          new XElement(customUINS + "customUI",
              new XElement(customUINS + "ribbon",
                  new XElement(customUINS + "tabs",
                      new XElement(customUINS + "tab",
                          new XAttribute("id", "customTab"),
                          new XAttribute("label", "CUSTOM"),
                          new XElement(customUINS + "group",
                              new XAttribute("id", "customGroup"),
                              new XAttribute("label", "Custom Group"),
                              new XElement(customUINS + "button",
                                  new XAttribute("id", "customButton"),
                                  new XAttribute("label", "Custom Button"),
                                  new XAttribute("size", "large"),
                                  new XAttribute("imageMso", "HappyFace")
                              )
                          )
                      )
                  )
              )
          )
      );
      return customUIXDoc;
  }
  ```

  ```vb
  Private Function CreateCustomUI() As XDocument
      ' Add a new Custom User Interface document part to the package.
      ' This code adds a new CUSTOM tab to the ribbon for this
      ' document. The tab has one group that contains one button.
      Dim customUINS As XNamespace = _
          "http://schemas.microsoft.com/office/2006/01/customui"
      Dim customUIXML = New XDocument( _
          New XDeclaration("1.0", "utf-8", "true"), _
          New XElement(customUINS + "customUI", _
              New XElement(customUINS + "ribbon",
                  New XElement(customUINS + "tabs",
                      New XElement(customUINS + "tab",
                          New XAttribute("id", "customTab"),
                          New XAttribute("label", "CUSTOM"),
                          New XElement(customUINS + "group",
                              New XAttribute("id", "customGroup"),
                              New XAttribute("label", "Custom Group"),
                              New XElement(customUINS + "button",
                                  New XAttribute("id", "customButton"),
                                  New XAttribute("label", "Custom Button"),
                                  New XAttribute("size", "large"),
                                  New XAttribute("imageMso", "HappyFace")
                              )
                          )
                      )
                  )
              )
          )
      )
      Return customUIXML
  End Function
  ```

2. 後、`CreateCustomUI`から前の手順では、**プログラム**のクラス (または Visual Basic では**Module1** ) 内のメソッドは、以下のメソッドを追加します。 
    
  ```cs
  private static void CreateNewPackagePart(Package filePackage, 
      XDocument partXML, Uri packageLocation, string contentType, 
      string relationship)
  {
      // Need to check first to see whether the part exists already.
      if (!filePackage.PartExists(packageLocation))
      {
          // Create a new blank package part at the specified URI 
          // of the specified content type.
          PackagePart newPackagePart = filePackage.CreatePart(packageLocation,
              contentType);
          // Create a stream from the package part and save the 
          // XML document to the package part.
          using (Stream partStream = newPackagePart.GetStream(FileMode.Create,
              FileAccess.ReadWrite))
          {
              partXML.Save(partStream);
          }
      }
      // Add a relationship from the file package to this
      // package part. You can also create relationships
      // between an existing package part and a new part.
      filePackage.CreateRelationship(packageLocation,
          TargetMode.Internal,
          relationship);
  }
  ```

  ```vb
  Private Sub CreateNewPackagePart(filePackage As Package, _
      partXML As XDocument, packageLocation As Uri, contentType As String, _
      relationship As String)
      ' Need to check first to see whether the part exists already.
      If Not (filePackage.PartExists(packageLocation)) Then
          ' Create a new blank package part at the specified URI
          ' of the specified content type.
          Dim newPart As PackagePart = filePackage.CreatePart(packageLocation, _
              contentType)
          ' Create a stream from the package part and save the
          ' XML document to the package part.
          Using partStream As Stream = newPart.GetStream(FileMode.Create, _
              FileAccess.ReadWrite)
              partXML.Save(partStream)
          End Using
          ' Add a relationship from the file package to this
          ' package part. You can also create relationships
          ' between an existing package part and a new part.
          filePackage.CreateRelationship(packageLocation, _
              TargetMode.Internal, relationship)
      End If
  End Sub
  ```

3. 次のコード**を使用して**コードをブロックする (Visual Basic では、 **module1 という名前**の**メイン**メソッドの**Using**ブロック)、**プログラム**のクラスの**Main**メソッド内のすべてを交換してください。 
    
  ```cs
  // Create a new Ribbon Extensibility part and add it to the file.
  XDocument customUIXML = CreateCustomUI();
  CreateNewPackagePart(visioPackage, customUIXML, 
      new Uri("/customUI/customUI1.xml", UriKind.Relative),
      "application/xml",
      "http://schemas.microsoft.com/office/2006/relationships/ui/extensibility");
  ```

  ```vb
  ' Create a new Ribbon Extensibility part and add it to the file.
  Dim customUIXML As XDocument = CreateCustomUI()
  CreateNewPackagePart(visioPackage, customUIXML, _
      New Uri("/customUI/customUI1.xml", UriKind.Relative), _
      "application/xml", _
      "http://schemas.microsoft.com/office/2006/relationships/ui/extensibility")
  ```

4. F5 キーを選択してソリューションをデバッグします。プログラムの実行が完了したら、任意のキーを選択して終了します。
    
5. Visio 2013 年に Package.vsdx の Visio ファイルを開くし、[**ユーザー設定**] タブを選択します。 
    
カスタム リボンは、Visio 2013 でファイルを開いたときに、図 2 のように見えます。
  
 **図 2 になります。Visio 2013 のリボンの [カスタム] タブ**
  
![リボンのカスタム タブ](media/vis15_CustomRibbonTab.PNG)
  
によって作成された、XML、`CreateCustomUI`メソッドは、次のようになります。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<customUI xmlns="http://schemas.microsoft.com/office/2006/01/customui">
  <ribbon>
    <tabs>
      <tab id="customTab" label="CUSTOM">
        <group id="customGroup" label="Custom Group">
          <button id="customButton" label="Custom Button" size="large"
              imageMso="HappyFace" />
        </group>
      </tab>
    </tabs>
  </ribbon>
</customUI>
```

## <a name="acknowledgements"></a>謝辞
<a name="vis15_ManipulateFF_Ackn"> </a>

貢献し、この技術情報に含まれているコード例を作成するのには、Visio の MVP **Al Edlund**の入力を認識しております。 Al は、Visio XML 図面 (.vdx) 形式と新しい Visio ファイル形式 (.vsdx) の両方を含め、Visio のファイル形式を操作するときに認識されているエキスパートです。 Al は、プログラムで、Visio のファイル形式を表示するプロジェクトが作成し、内部構造を公開します。 
  
Visio ファイル形式での作業の詳細については、以下については、ここにリンクを参照してください。
  
## <a name="see-also"></a>関連項目
<a name="vis15_ManipulateFF_Additional"> </a>

- Al Edlund 提供:
    
  - CodePlex で[pkgVisio の Visio 2013 の XML の操作](http://pkgvisio.codeplex.com/documentation)のプロジェクトです。 
    
  - [pkgVisio_pt1](http://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) YouTube のビデオです。 
    
  - [pkgVisio_pt2](http://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) YouTube のビデオです。 
    
- [Visio デベロッパー センター](http://msdn.microsoft.com/en-us/office/aa905478.aspx)
    
- [Office オープン XML 形式のドキュメントを操作します。](http://msdn.microsoft.com/en-us/library/aa982683%28v=office.12%29.aspx)
    
- [名前空間 (C#) (LINQ to XML) ドキュメントを作成します。](http://msdn.microsoft.com/en-us/library/bb387075.aspx)
    
- [Microsoft Office を起動することがなく、ドキュメントにカスタム XML 部分を追加します。](http://msdn.microsoft.com/en-us/library/bb608597%28VS.90%29.aspx)
    

