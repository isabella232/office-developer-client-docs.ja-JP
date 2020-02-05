---
title: プログラムを使用して Visio ファイル形式を操作する
manager: lindalu
ms.date: 04/17/2019
ms.audience: Developer
ms.topic: overview
ms.assetid: 5f5e2288-7539-41b8-916d-410be028ed9b
description: Visio 2013 での新しいファイル形式パッケージを読み取り、パッケージ内のパーツを選択しその中のデータを変更して、パッケージに新しいパーツを追加するソリューションをVisual Studio 2012で作成します。
localization_priority: Priority
ms.openlocfilehash: 36a621856e5d53e7b3355a39edd7b7a03636b15d
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773744"
---
# <a name="manipulate-the-visio-file-format-programmatically"></a>プログラムを使用して Visio ファイル形式を操作する

![操作手順のトピック](media/mod_icon_howto.png)
  
Visio 2013 での新しいファイル形式パッケージを読み取り、パッケージ内のパーツを選択しその中のデータを変更して、パッケージに新しいパーツを追加するソリューションをVisual Studio 2012で作成する方法を説明します。
   
## <a name="visio-file-format-manipulation-essentials"></a>Visio ファイル形式の操作の基本
<a name="vis15_ManipulateFF_Essentials"> </a>

Visio の以前のバージョンでは、独自のバイナリ ファイル形式 (.vsd) またはシングル ドキュメント Visio XML 図面ファイル形式 (.vdx) でファイルを保存していました。 Visio 2013 では、XML と ZIP のアーカイブ テクノロジに基づく新しいファイル形式 (.vsdx) が導入されています。 以前のバージョンの Visio と同じように、ファイルは 1 つのコンテナーに保存されます。 しかし、従来のファイルとは違って、新しいファイル形式は Visio 2013 アプリケーションを自動化することなく、開いたり、読み取ったり、更新したり、変更したり、構築したりできます。 XML の操作や [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8) 名前空間の処理に精通している開発者は、プログラムによる新しいファイル形式ですぐに仕事を始められます。 以前のバージョンから Visio XML 図面形式を処理していた開発者は、以前の形式の構造の多くが新しいファイル形式でも保持されていることに気づかれるでしょう。 
  
この記事では、Microsoft .NET Framework 4.5 や C#、Visual Basic、 Visual Studio 2012 を使用して、Visio 2013 でファイル形式をプログラムによって操作する方法を検証します。 Visio 2013 ファイルを開き、ファイル内のドキュメント パーツを選択し、パーツ内のデータを変更し、新しいドキュメント パーツを作成する方法が記載されています。
  
> [!NOTE]
> この記事のコード サンプルは、読者が [System.Xml.Linq](https://docs.microsoft.com/dotnet/api/system.xml.linq?view=netframework-4.8) と [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8) の名前空間内のクラスに関する基本的な知識があることを想定しています。 > この記事では、読者が Open Packaging Conventions の概念と用語を理解していることも想定しています。 パッケージ、文書パーツまたはパッケージ パーツ、およびリレーションシップの概念を理解している必要があります。 詳しくは、[OPC: データのパッケージ化のための新しい標準](https://docs.microsoft.com/archive/msdn-magazine/2007/august/opc-a-new-standard-for-packaging-your-data)をご覧ください。 > コードは、統合言語クエリ (LINQ: Language-Integrated Query) を作成して XML を選択する方法を示しています。 コード サンプルのほとんどでは、クエリ構文を使用して LINQ クエリを構築しています。 必要に応じて、LINQ メソッド構文を使用して、コード内にある LINQ クエリを書き換えることができます。 LINQ クエリの構文とメソッドの構文の詳細については、次を参照してください。[LINQ クエリ構文とメソッドの構文 (C#)](https://docs.microsoft.com/dotnet/csharp/programming-guide/concepts/linq/query-syntax-and-method-syntax-in-linq)> 表 1 は、この記事を読み進める前に精通しておく必要のある重要なトピックを示しています。 
  
**表 1. Visio 2013 ファイル形式の操作に関する中心的概念**

|**記事のタイトル**|**説明**|
|:-----|:-----|
|[Visio ファイル形式 (.vsdx) の概要](introduction-to-the-visio-file-formatvsdx.md) <br/> |この概説では、Visio 2013 ファイル形式の主な機能の一部を説明しています。 Visio 2013 ファイル形式に適用されている Open Packaging Conventions (OPC) について解説しています。 また、Visio 2013 ファイル形式と以前の Visio XML 図面ファイル形式 (.vdx) との違いを抜粋して一覧表示しています。  <br/> |
|[OPC: データのパッケージ化のための新しい標準](https://docs.microsoft.com/archive/msdn-magazine/2007/august/opc-a-new-standard-for-packaging-your-data) <br/> |この MSDN マガジンの記事では、Open Packaging Conventions の概念について説明します。  <br/> |
|[Open Packaging Conventions の基本](https://docs.microsoft.com/en-us/previous-versions/office/office-12/ee361919(v=office.12)) <br/> [Office (2007) Open XML ファイル形式の概要](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa338205(v=office.12)) <br/> |これら 2 つの記事では、Open Packaging Conventions を Microsoft Office ファイルに適用する方法について解説します。 パッケージ内でのリレーションシップの働きについて説明し、コード例もいくつか記述されています。  <br/> |
   
## <a name="create-a-vsdx-file-and-a-new-visual-studio-solution"></a>.vsdx ファイルと新しい Visual Studio ソリューションを作成する
<a name="vis15_ManipulateFF_CreateFile"> </a>

この記事の手順で作業を開始する前に、操作の対象となる Visio 2013 ファイルを作成する必要があります。 この記事のコード例で使用されている図面には 1 つのページがあり、そこに 2 つの接続された図形が含まれます。そのうちの 1 つは「基本フローチャート」テンプレートからの「開始/終了」図形になります。
  
次の手順を使用して、この記事の残りの手順で使用する Visio 2013 のファイルを新しく作成してください。
  
### <a name="to-create-new-file-in-visio-2013"></a>Visio 2013 の新しいファイルを作成するには

1. Visio 2013 を開きます。
    
2. **[カテゴリ]**、**[フローチャート]**、**[基本フローチャート]**、**[作成]** を選択して、基本フローチャート テンプレートに基づいて新しいドキュメントを作成します。
    
3. **[図形]**  ウィンドウから、**[開始/終了]** 図形をキャンバス上にドラッグします。 
    
4. 図面キャンバス上で新しい開始/終了図形を選択し、「処理の開始」と入力します。
    
5. **[図形]** ウィンドウから、**[処理]** 図形をキャンバス上にドラッグします。 
    
6. 図面キャンバス上で新しい処理図形を選択 し、「タスクの実行」と入力します。
    
7. 開始/終了図形のショートカット メニューで、**[ページに 1 つのコネクタを追加]** を選択してから、図 1 のように、キャンバス上の開始/終了図形と処理図形の間にコネクタを描画します。
    
    **図 1。Visio 2013 の簡単な描画**
    
     ![処理図形に接続されている開始/終了図形](media/vis15_SimpleFlowchart.png)
  
8. **[ファイル]**、**[名前を付けて保存]**、**[コンピューター]**、**[デスクトップ]** を選択して、ファイルをデスクトップに .vsdx ファイルとして保存します。
    
    **[名前を付けて保存]** ダイアログ ボックスで、**[ファイル名]** ボックスに「Visio パッケージ」と入力し、**[ファイルの種類]\*リストで **[Visio 図面 (**.vsdx)]** を選択してから、**[保存]** ボタンを選択します。 
    
9. ファイルを閉じてから、Visio 2013 を閉じます。
    
> [!TIP]
> Visio では問題のあるファイルが正常に開かれることがあります。 Visio からファイルの問題が確実に通知されるようにするには、ファイル パッケージ レベルで Visio ファイルを操作するソリューションをテストする際に、ファイルを開くときの警告を有効にする必要があります。 > ファイルを開くときの警告を有効にするには、Visio 2013 で、**[ファイル]**、**[オプション]**、**[詳細設定]** を選択します。 **[保存/開く]** から、**[ファイルを開くときの警告を表示する]** を選択します。 
  
これらの手順では、"Visio Package.vsdx"ファイルを操作するのに Windows コンソール アプリケーションを使用します。 Visual Studio 2012 で新しい Windows コンソール アプリケーションを作成してセットアップするには、次の手順に従ってください。
  
### <a name="to-create-a-new-solution-in-visual-studio-2012"></a>Visual Studio 2012 で新しいソリューションを作成します。

1. **[ファイル]** メニューで、**[新規作成]**、**[プロジェクト]** を選択します。
    
2. **[新しいプロジェクト]** ダイアログ ボックスで、**[Visual C#]** または **[Visual Basic]** を展開してから、**[Windows]**、**[コンソール アプリケーション]** を選択します。
    
    **[名前]** ボックスで、「VisioFileAccessor」と入力し、プロジェクトの場所を選択してから、**[OK]** ボタンを選択します。 
    
3. [ **プロジェクト**] メニューの [ **参照の追加**] を選択します。 
    
    **[参照マネージャー]** ダイアログ ボックスで、**[アセンブリ]** の下の **[フレームワーク]** を選択してから、参照を **[System.Xml]** コンポーネントと **[WindowsBase]** コンポーネントに追加します。 
    
4. プロジェクトの Program.cs または Module1.vb ファイル内に、次の**使用している** ディレクティブ (Visual Basic の **Imports** ステートメント) を追加します。 
    
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

5. 同様に、Program.cs または Module1.vb ファイル内の、**Program** クラス (Visual Basic では **Module1**) の **Main** メソッドの末尾の前に、ユーザーがキーを押すまでコンソール アプリケーションの実行を停止する次のコードを追加します。 
    
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

## <a name="open-a-visio-2013-file-as-a-package"></a>Visio 2013 ファイルをパッケージとして開く
<a name="vis15_ManipulateFF_OpenPackage"> </a>

ファイル内のデータを操作するには、その前に [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging.package?view=netframework-4.8) 名前空間に含まれる [Package](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8) オブジェクト内のファイルを開く必要があります。 **Package** オブジェクトは Visio ファイルを全体として表します。 ファイル パッケージ内の個々の文書パーツの選択を許可しているメンバーが表示されます。 特に、**Package** クラスは、ファイルをパッケージとして開くのに使用する静的[Open(String, FileMode, FileAccess)](https://docs.microsoft.com/dotnet/api/system.io.packaging.package.open?view=netframework-4.8) メソッドを公開します。 また、作業が終了したらパッケージを閉じるための [Close()](https://docs.microsoft.com/dotnet/api/system.io.packaging.package.close?view=netframework-4.8) メソッドも公開します。 
  
> [!TIP]
> 最善の方法としては、**using** ブロックを使用して **Package** オブジェクト内の Visio ファイルを開くと、作業終了時にファイル パッケージを明示的に閉じる必要がなくなります。 また、**try/catch/finally** 構造の **Finally** ブロックで **Package.Close** メソッドを明示的に呼び出すこともできます。 
  
[FileInfo](https://docs.microsoft.com/dotnet/api/system.io.fileinfo?view=netframework-4.8) オブジェクトを使用して「Visio Package.vsdx」ファイルの完全パスを取得し、そのパスを引数として **Package.Open** メソッドに渡してから、呼び出し側のコードに **Package** オブジェクトを返すには、次のコードを使用してください。 
  
### <a name="to-open-a-vsdx-file-as-a-package"></a>.vsdx ファイルをパッケージとして開くには

1. **Program** クラス (または Visual Basic の **Module1**) 内の **メイン** メソッドの後に、次のコードを追加します。 
    
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

2. **Program** クラス (または Visual Basic の **Module1**) 内の **メイン** メソッドで、次のコードを追加します。 
    
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

パッケージとして Visio 2013 のファイルを開いたら、**System.IO.Packaging**名前空間に含まれている[PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx)クラスを使用して、ファイルの中のドキュメント パーツにアクセスできます。 **PackagePart**オブジェクトは、個別またはコレクションとしてインスタンス化することができます。 **Package** クラスは、 [Package](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) から [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx) オブジェクトを取得するための **GetParts()** メソッドと **GetPart(Uri)** メソッドを公開します。 **Package.GetParts** メソッドは[PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx) クラスのインスタンスを返します。それにより [IEnumerator\< T\> ](https://docs.microsoft.com/dotnet/api/system.collections.generic.ienumerator-1?redirectedfrom=MSDN&view=netframework-4.7.2)インターフェースを実行するほかのコレクションを操作することができます。 
  
**PackagePartCollection** オブジェクトを **Package** からコレクションとして取得し、コレクション内で **PackagePart** オブジェクトを反復処理し、各 **PackagePart** の URI とコンテンツ タイプをコンソールに書き込むには、次の手順のコードを使用してください。 
  
### <a name="to-iterate-through-the-package-parts-in-a-package"></a>パッケージ内のパッケージ パーツを反復処理するには

1. **Program** クラス (または Visual Basic の **Module1**) 内の `OpenPackage` メソッドの後に、次のコードを追加します。 
    
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

2. **Program** クラスの **Main** メソッド内の **using** ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) 内に、次のコードを追加します。 
    
    ```cs
    // Write the URI and content type of each package part to the console.
    IteratePackageParts(visioPackage);
    
    ```

    ```vb
    ' Write the URI and content type of each package part to the console.
    IteratePackageParts(visioPackage)
    
    ```

3. F5 キーを選択してソリューションをデバッグします。 プログラムの実行が完了したら、任意のキーを選択して終了します。
    
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
  
ほとんどの場合、**PackagePart**のいずれかを選択するだけでよく、それらすべてを反復処理する必要はありません。 **Package** または他の **PackagePart** とのリレーションシップを使用して、**Package**から**PackagePart** オブジェクトを取得することができます。 Visio 2013 ファイル形式のリレーションシップは、ドキュメント パーツとファイル パッケージの関係や 2 つのドキュメント パーツの相互の関係を記述した個別のエンティティです。 たとえば、Visio 2013 ファイル パッケージ自体には Visio ドキュメント パーツとのリレーションシップがあり、Visio ドキュメント パーツには Windows のパーツとのリレーションシップがあります。 これらのリレーションシップは、[PackageRelationship](https://docs.microsoft.com/dotnet/api/system.io.packaging.packagerelationship?view=netframework-4.8) または [PackageRelationshipCollection](https://docs.microsoft.com/dotnet/api/system.io.packaging.packagerelationshipcollection?view=netframework-4.8) クラスのインスタンスとして表されます。 

**Package**クラスは、**PackageRelationship**または**PackageRelationshipCollection**オブジェクトとして含まれているリレーションシップを取得するいくつかの方法を公開します。 [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx) メソッドを使用して、1 つの特定の種類の **PackageRelationship** オブジェクトを含む **PackageRelationshipCollection** オブジェクトをインスタンス化できます。 もちろん、 **Package.GetRelationshipsByType**メソッドを使用するには、必要なリレーションシップの種類が既にわかっている必要があります。 リレーションシップの種類は、XML 名前空間の形式の文字列です。 たとえば、Visio の文書パーツのリレーションシップの種類はhttps://schemas.microsoft.com/visio/2010/relationships/documentです。 
  
**PackagePart** と **Package** または別の **PackagePart** とのリレーションシップが分かったら (つまり、目的の **PackagePart** を参照する **PackageRelationship** オブジェクトがある場合)、このリレーションシップを使用して、その **PackagePart** の URI を取得できます。 **PackagePart**を返すための**Package.GetPart** メソッドにURIを渡します。
  
> [!NOTE]
> パッケージ パーツのリレーションシップを取得するステップを迂回し、**Package.GetPart** メソッドと **PackagePart** の URI のみを使用して特定の **PackagePart** への参照を取得することもできます。 しかし、Visio ファイル パッケージ内のパッケージ パーツの一部が、パッケージ内の既定以外の場所に保存されることがあります。 パッケージ パーツが常にすべてのファイルに対して同じ URI にあるとは限りません。 > その代わりに、リレーションシップを使用して個々 の **PackagePart** オブジェクトにアクセスする方法が最善です。 
  
パーツを参照する**Package**から **PackageRelationship** を使用して**PackagePart** (Visio ドキュメント パーツ) を取得するには、次の手順を使用します。 
  
### <a name="to-select-a-specific-package-part-in-the-package-by-relationship"></a>リレーションシップによりパッケージ内の特定のパッケージ パーツを選択するには

1. `IteratePackageParts`Program** クラス (または Visual Basic の **Module1 **) 内の **メソッドの後に、次のメソッドを追加します。 
    
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

2. **Program** クラスの **Main** メソッド内の **using** ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) 内のコードを、次のコードで置き換えます。 
    
    ```cs
    // Get a reference to the Visio Document part contained in the file package.
    PackagePart documentPart = GetPackagePart(visioPackage, 
        "https://schemas.microsoft.com/visio/2010/relationships/document");
    
    ```

    ```vb
    ' Get a reference to the Visio Document part contained in the file package.
    Dim documentPart As PackagePart = GetPackagePart(visioPackage, _
        "https://schemas.microsoft.com/visio/2010/relationships/document")
    
    ```

前述のように、他の**PackagePart**オブジェクトとのリレーションシップを使って**PackagePart**オブジェクトを取得することもできます。 Visio ドキュメントの場合、複雑さにかかわらずほとんどの **PackagePart** オブジェクトは **Package** とのリレーションシップがないので、この点は重要です。 たとえば、ファイル パッケージ内の個々 のページ コンテンツ パーツ (つまり/visio/pages/page1.xml) には、ページ インデックス パーツ (つまり /visio/pages/pages.xml) とのリレーションシップはありますが、ファイル パッケージ自体とのリレーションシップはありません。 パッケージ内の個々 のページの正確な URI がわからない場合は、ページ インデックス パーツとのリレーションシップを使用してそのページへの参照を取得できます。
  
**PackagePart** クラスは、1つの種類の[ PackageRelationship](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx)オブジェクトだけを含む **PackageRelationshipCollection** オブジェクトを返すために使用できる **GetRelationshipsByType(String)** メソッドを公開します。 **PackageRelationshipCollection** を取得したら、コレクションから必要な **PackageRelationship** を選び、**PackagePart** オブジェクトを参照できます。 
  
別の **PackagePart** との（**PackageRelationship** オブジェクトから取得する）リレーションシップによって **Package** から ** PackagePart** を取得するには、次のコードを使用します。
  
### <a name="to-select-a-specific-package-part-through-its-relationship-to-another-package-part"></a>別のパッケージ パーツとのリレーションシップを利用して特定のパッケージ パーツを選択するには

1. `GetPackagePart`Program** クラス (または Visual Basic の **Module1 **) 内の **メソッドの後に、次のオーバーロード メソッドを追加します。 
    
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

2. **Program** クラスの **Main** メソッド内の **using**  ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) の、前の手順のコードの下に、次のコードを追加します。 (前の手順で追加したコードを削除しないでください。) 
    
    ```cs
    // Get a reference to the collection of pages in the document, 
    // and then to the first page in the document.
    PackagePart pagesPart = GetPackagePart(visioPackage, documentPart, 
        "https://schemas.microsoft.com/visio/2010/relationships/pages");
    PackagePart pagePart = GetPackagePart(visioPackage, pagesPart, 
        "https://schemas.microsoft.com/visio/2010/relationships/page");
    
    ```

    ```vb
    ' Get a reference to the collection of pages in the document,
    ' and then to the first page in the document.
    Dim pagesPart As PackagePart = GetPackagePart(visioPackage, documentPart, _
        "https://schemas.microsoft.com/visio/2010/relationships/pages") 
    Dim pagePart As PackagePart = GetPackagePart(visioPackage, pagesPart, _
        "https://schemas.microsoft.com/visio/2010/relationships/page") 
    ```

ドキュメント パーツに含まれている XML に変更を加えるには、その前にまず [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) クラスか [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx) クラスを使用して、その XML を閲覧できるようにするオブジェクト内に XML ドキュメントを読み込む必要があります。 両方のクラスとも、XML ドキュメント内に含まれる XML 要素の選択、属性の作成と読み書き、新しい XML 要素のドキュメント内への挿入などのタスクに関するメソッドを公開します。 
  
2 つの**XDocument**クラスでは、LINQ を使用して XML をクエリすることができます。 LINQ を使用すると、コレクション内のすべての要素を反復処理して必要な要素をテストしたりしなくても、クエリを作成することにより個々の要素を XML ドキュメントから簡単に選択できます。 この理由で、この記事の次の手順では **XDocument** クラスと **System.Xml.Linq** 名前空間の他のクラスを使用して XML を処理します。 
  
**XDocument** オブジェクト内の XML ドキュメントとして **PackagePart** を開くには、次の手順を使用します。 
  
### <a name="to-read-the-xml-in-a-package-part"></a>パッケージ パーツ内の XML を読み取るには

1. **Program** クラス (Visual Basic では **Module1**) 内の`GetPackagePart`メソッドの最後のオーバー ロードの後に、次のメソッドを追加します。 
    
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

2. **Program** クラスの **Main** メソッド内の **using**  ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) の、前の手順のコードの下に、次のコードを追加します。 
    
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

**XDocument** オブジェクト内にドキュメント パーツを読み込み終えたら、LINQ を使用して、XML 要素を選択し、XML ドキュメントに変更を加えることができます。 XML データを変更、追加またはデータを削除することができます。その後、文書パーツに XML ドキュメントを保存できます。 
  
Visio ファイル形式の操作に関する最も一般的なタスクは、ドキュメント内の特定の XML 要素か要素のコレクションを選択することです。 **System.Xml.Linq** 名前空間には、XML 要素を表す [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx) クラスが含まれています。 **XElement** クラスは、 Visio ファイルに含まれるデータにきめ細かいレベルで (たとえば、個々の **Shape** 要素から **ValidationRule** 要素に至るまで) アクセスできるようにします。 
  
**Shape** 要素を **XDocument** (ページ コンテンツ パーツを含む) から選択してから、特定の **Shape** 要素を選択するには、次のコードを使用してください。 
  
### <a name="to-select-a-specific-element-in-a-package-part"></a>パッケージ パーツ内の特定の要素を選択するには

1. `GetXMLFromPart`Program** クラス (または Visual Basic の **Module1 **) 内の **メソッドの後に、次のメソッドを追加します。 
        
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

2. 前のステップの **Program** クラス (Visual Basic では **Module1**) 内の `GetXElementsByName` メソッドの後に、次のメソッドを追加します。 
    
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

3. **Program** クラスの **Main** メソッド内の **using**  ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) の、前の手順のコードの下に、次のコードを追加します。 
    
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

**XDocument** オブジェクト内に含まれる **XElement** オブジェクトへの参照を取得し終えたら、他の XML データと同様に操作できるので、Visio ファイル内に含まれるデータを変更できます。 たとえば、Visio で開いている図形にテキストがある場合、対応する **Shape** 要素には 1 つ以上の **Text** 要素が含まれます。 この **Text** 要素の値を変更すると、Visio でファイルを表示する際に、この図形のテキストは変更されます。 
  
開始/終了図形内のテキストを「Begin process」から「Start process」に変更するには、**Program** クラスの **Main** メソッド内の **using**  ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) に次のコードを追加します。 
  
```cs
// Query the XML for the shape to get the Text element, and
// return the first Text element node.
IEnumerable<XElement> textElements = from element in startEndShapeXML.Elements()
                               where element.Name.LocalName == "Text"
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
    Where element.Name.LocalName == "Text"
    Select element
Dim textElement As XElement = textElements.ElementAt(0)
' Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process")

```

> [!CAUTION]
> 上記のコード例で、既存の図形のテキストと置き換える文字列の文字数は同じです。 また、LINQ クエリは、返される要素の最後の子ノード (この例ではテキスト ノード) の値を変更することにもご注意ください。 これは、**テキスト**要素の子である **cp** 要素の設定を変更しないようにするため行われます。 >**Text** 要素のすべての子を上書きする方法でプログラムによって図形のテキストを変更すると、ファイルが不安定になることがあります。 上記の例のように、テキストの書式はファイル内の **Text** 要素の下の **cp** 要素で表されます。 書式設定の定義は、親 **Section** 要素に格納されています。 これら 2 つの情報が整合していないと、ファイルは正常に動作しない可能性があります。 Visio は不整合の多くを修復しますが、プログラムによる変更が一貫しており、ファイルの最終的な動作が制御されているか確認することをお勧めします。 
  
ドキュメント パーツの XML に変更を加える場合、その変更内容はメモリ内のみに存在します。ファイル内に変更を保持するには、ドキュメント パーツに XML を戻して保存する必要があります。
  
次のコードは、[XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) クラスと [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) クラスを使用して XML をパッケージ パーツに書き戻します。 [Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx) メソッドを使用して XML をパーツに戻して保存できますが、**XmlWriter** クラスと **XmlWriterSettings** クラスを使用するとエンコードの種類を指定するなど、出力をより細かく制御できます。 **XDocument** クラスは、**XmlWriter** オブジェクトを利用して XML をストリームに書き戻す [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx) メソッドを公開します。 
  
XML を Visio ページからページ コンテンツ パーツに戻して保存するには、次の手順を使用してください。
  
### <a name="to-save-the-changed-xml-back-to-the-package"></a>変更した XML をパッケージに戻して保存するには

1. 前のステップの **Program** クラス (Visual Basic では **Module1**) 内の `GetXElementByAttribute` メソッドの後に、次のメソッドを追加します。 
    
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

2. **Program** クラスの **Main** メソッド内の **using**  ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) の、前の手順のコードの下に、次のコードを追加します。 
    
    ```cs
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

3. F5 キーを選択してソリューションをデバッグします。 プログラムの実行が完了したら、任意のキーを選択して終了します。
    
4. Visio 2013 で Visio Package.vsdx ファイルを開きます。 
    
この時点で開始/終了図形にテキスト「Start process」が含まれているはずです。
  
## <a name="recalculate-data-in-the-file"></a>ファイル内のデータを再計算する
<a name="vis15_ManipulateFF_Recalculate"> </a>

ファイル内のデータの変更には、ファイルを開いたときに、Visio で文書を再計算する必要があります。 Visio はダイアグラム、特に、図形のリレーションシップ（つまり、ある図形が別の図形に依存する場合）や接続する図形などに多くのロジックを提供します。 カスタム ロジックで使用されるデータのいずれかを変更すると、Visio はファイル内で影響を受けるすべての集計データに変更を反映する 必要があります。 
  
Visio 2013 ファイル形式には、ファイル内のデータの再計算に使用できる手法がいくつか含まれています。 次の 3 種類のシナリオは、Visio ファイルを再計算する必要があるかどうかと、再計算の方法を決めるときに考慮する必要があります。
  
- データへの変更は、ファイル形式におけるその他の値には影響しません。 ドキュメントを再計算する命令を Visio に追加する必要はありません。 既に示したように、ドキュメントの再計算を実行せずに、図形のテキストを頻繁に変更できます。
    
- データへの変更が XML 内のシェイプシート セルの値の変更に限定されており、このデータに依存している他のシェイプシート値がある場合。 この場合、([XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx) クラスを使用して) XML 処理命令を、変更された **Cell** 要素に追加する必要があります。 たとえば、図形の **ThemeIndex**セルは、図形に含まれるその他いくつかの ShapeSheet セルの値に影響します。 ファイル自体の **ThemeIndex** セル (たとえば、**N** 値が「ThemeIndex」の **Cell** 要素) を変更する場合、依存している値が更新されるように、**Cell** 要素に処理命令を追加する必要があります。 
    
- データへの変更がコネクタの位置つまり接続ポイントに影響する場合。 別の状況として、シェイプシートのデータに多数の変更があり、(変更ごとに個別に処理命令を追加するのではなく) 1 つの命令でドキュメント全体を再計算しようとする場合もあります。 この場合、ドキュメントを開くときにそのドキュメント全体を再計算するように Visio に命令できます。 そのためには、**RecalcDocument** プロパティを Visio パッケージのカスタム ファイル プロパティ パーツ (/docProps/custom.xml) に追加します。 この種のシナリオの例としては、接続された図の中の図形の位置やサイズを調整する場合があります。 
    
    パフォーマンスの観点からは、このシナリオが最もコストがかかるオプションであることに留意してください。
    
**Cell** 要素を **Shape** 要素内に挿入し、この新しい値のために同じ **Shape** 内の他の **Cell** 要素を再計算する必要がある場合には、次の手順を使用してください。 新しい **Cell** 要素には、ローカルな再計算を実行する必要があることを Visio に通知する処理命令が子要素として組み込まれています。 
  
### <a name="to-recalculate-values-for-a-single-shape"></a>1 つの図形の値を再計算するには

1. 前述の 2 つの例 (図形のテキストの変更および `SaveXDocumentToPart`に対する呼び出し) の、**Program** クラスの **Main** メソッド内の **using** ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) 内のコードを、次のコードで置き換えます。 
    
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
    ' already have a local ThemeIndex cell.
    startEndShapeXML.Add(New XElement("Cell", _
        New XAttribute("N", "ThemeIndex"),
        New XAttribute("V", "25"),
        New XProcessingInstruction("NewValue", "V")))
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

2. F5 キーを選択してソリューションをデバッグします。 プログラムの実行が完了したら、任意のキーを選択して終了します。
    
3. Visio 2013 で Visio Package.vsdx ファイルを開きます。 開始/終了図形の塗りつぶしの色が変わっているはずです。
    
図形の色は**ThemeIndex**セルの値により異なります。図形がどのアクティブなテーマを継承するかによって決まります。 前の例では、図形は別のテーマを継承する設定 (**ThemeIndex**セルが「25」の値に設定)になっています。 処理命令を使用しない場合は、図形のテキストの色（同様に **ThemeIndex**セルの影響を受けます）は再計算されません。 図形の塗りつぶしの色が白に変更されますが、テキストの色は白のままで、テキストは読み取り不可能な状態になります。 また、処理命令を使用しない場合、ファイルは図形の書式設定の値が予期せず更新される可能性のある不安定な状態のままで、Visio が図形を更新するのは後日になる可能性があります。 
  
Visio でドキュメントを再計算する必要があるファイル内のデータを変更する場合は (たとえば、接続されている図形の位置を変更するので、コネクタを再接続する必要がある場合)、Visio ファイルに再計算の命令を追加する必要があります。 この命令を作成するには、**name** 属性値が「RecalcDocument」の **property** 要素を Visio ファイル パッケージのカスタム ファイル プロパティ パーツの XML に追加します。 最善の方法として、カスタム ファイル プロパティ パーツをチェックして、ファイル内で「RecalcDocument」命令が既に登録されていないか確認する必要があります。 
  
前の例から、開始/終了図形の**PinY** セルの値を変更するには、次のコードを使用します。 このコードは、**N** 属性の値を使用して、**XElement**  オブジェクトとして**PinY** セルのデータを含む **Cell** 要素 を選択します。 その後このコードは、再計算の命令を Visio ファイルのカスタム ファイル プロパティ パーツに追加します。 
  
> [!NOTE]
> このコードは、以前に作成した `GetPackagePart` メソッドと `SaveXDocumentToPart` メソッドに依存しています。 
  
### <a name="to-recalculate-the-entire-document-when-it-is-opened"></a>ドキュメントが開いている場合にそのドキュメント全体を再計算するには

1. 前のステップの **Program** クラス (Visual Basic では **Module1**) 内の `SaveXDocumentToPart` メソッドの後に、次のメソッドを追加します。 
    
    ```cs
    private static void RecalcDocument(Package filePackage)
    {
        // Get the Custom File Properties part from the package and
        // and then extract the XML from it.
        PackagePart customPart = GetPackagePart(filePackage, 
            "https://schemas.openxmlformats.org/officeDocument/2006/relationships/" + 
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
                "https://schemas.openxmlformats.org/officeDocument/2006/" + _
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

2. 前のステップの **Program** クラス (Visual Basic では **Module1**) 内の `RecalcDocument` メソッドの後に、次のメソッドを追加します。 
    
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

3. 前述の例から、**Program** クラスの **Main** メソッド内の **using** ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) 内のコードを、次のコードで置き換えます。 
    
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

4. F5 キーを選択してソリューションをデバッグします。 プログラムの実行が完了したら、任意のキーを選択して終了します。
    
5. Visio 2013 で Visio Package.vsdx ファイルを開きます。 
    
開始/終了図形は図面の下端から 2 インチの位置にあるはずです。 開始/終了図形と処理図形の間のコネクタは、レイアウトの変更に合わせて再接続されているはずです。 **RecalcDocument** プロパティがファイルに追加されていないと、図形の位置は変わりますが、コネクタは新しい図形の位置に再接続されません。 
  
## <a name="add-a-new-package-part-to-a-package"></a>新しいパッケージ パーツをパッケージに追加する
<a name="vis15_ManipulateFF_AddNewPart"> </a>

ファイル パッケージを変更するための最も一般的なシナリオの 1 つは、新しい文書パーツをパッケージに追加することです。 たとえば、コンテンツをパッケージに追加することにより Visio 図面にページを追加する場合は、ページ コンテンツ パーツをパッケージに追加する必要があります。 
  
次のように、パッケージに新しいパーツを追加するプロセスは簡単です。 
  
1. **PackagePart** のためのデータを含む XML ドキュメントを作成します。 作成した特定の種類の XML ドキュメントのスキーマを制御する XML 名前空間に特別な注意を払う必要があります。
    
2. この XML を含む新しいファイルを作成し、そのファイルを **Package** 内の場所に保存します。
    
3. 新しい **PackagePart** と** Package**、または他の **PackagePart** オブジェクトの間に、必要なリレーションシップを作成します。 
    
4. 新しいパーツを参照する必要がある既存のパーツを更新します。たとえば、新しいページ コンテンツ パーツ (新しいページ) をファイルに追加する場合は、ページ インデックス パーツ (/visio/pages/pages.xml ファイル) を更新し、新しいページに関する正しい情報を組み込む必要もあります。
    
Visio ファイル内に新しいリボン機能拡張パーツを作成するには、次の手順を使用してください。 新しいリボン機能拡張パーツは、1 つのボタンが含まれる 1 つのグループを持つ新しいタブをリボンに追加します。
  
### <a name="to-create-a-new-package-part"></a>新しいパッケージ パーツを作成するには

1. 前の手順の **Program** クラス (Visual Basic では **Module1**) 内の `CheckForRecalc` メソッドの後に、次のメソッドを追加します。 
    
    ```cs
    private static XDocument CreateCustomUI()
    {
        // Add a new Custom User Interface document part to the package.
        // This code adds a new CUSTOM tab to the ribbon for this
        // document. The tab has one group that contains one button.
        XNamespace customUINS = 
            "https://schemas.microsoft.com/office/2006/01/customui";
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
            "https://schemas.microsoft.com/office/2006/01/customui"
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

2. 前のステップの **Program** クラス (Visual Basic では **Module1**) 内の `CreateCustomUI` メソッドの後に、次のメソッドを追加します。 
    
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

3. **Program** クラスの **Main** メソッド内の **using** ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) 内のすべてのコードを、次のコードで置き換えます。 
    
    ```cs
    // Create a new Ribbon Extensibility part and add it to the file.
    XDocument customUIXML = CreateCustomUI();
    CreateNewPackagePart(visioPackage, customUIXML, 
        new Uri("/customUI/customUI1.xml", UriKind.Relative),
        "application/xml",
        "https://schemas.microsoft.com/office/2006/relationships/ui/extensibility");
    ```

    ```vb
    ' Create a new Ribbon Extensibility part and add it to the file.
    Dim customUIXML As XDocument = CreateCustomUI()
    CreateNewPackagePart(visioPackage, customUIXML, _
        New Uri("/customUI/customUI1.xml", UriKind.Relative), _
        "application/xml", _
        "https://schemas.microsoft.com/office/2006/relationships/ui/extensibility")
    ```

4. F5 キーを選択してソリューションをデバッグします。 プログラムの実行が完了したら、任意のキーを選択して終了します。
    
5. Visio 2013 で Visio Package.vsdx ファイルを開いてから、**[カスタム]** タブを選択します。 
    
Visio 2013 でファイルを開くと、カスタム リボンは図 2 のように表示されます。
  
 **図 2. Visio 2013リボン内のカスタム タブ**
  
![リボンのカスタム タブ](media/vis15_CustomRibbonTab.PNG)
  
次のような `CreateCustomUI` メソッドによって XML が作成されます。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<customUI xmlns="https://schemas.microsoft.com/office/2006/01/customui">
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

この技術文書に含まれるコード例を作成した Visio MVP **Al Edlund** の貢献に感謝いたします。 Al は、Visio XML 図面形式 (.vdx) と新しい Visio ファイル形式 (.vsdx) の両方を含む、Visio ファイル形式の操作に関する定評のある専門家です。 Al は、プログラムによって Visio ファイル形式を調べるプロジェクトを作成しており、その内部構造を公開しています。 
  
Al による Visio ファイル形式の処理の詳細については、下記の「その他の技術情報」セクションにあるリンクを参照してください。
  
## <a name="see-also"></a>関連項目
<a name="vis15_ManipulateFF_Additional"> </a>

- Al Edlund 提供:
    
  - codeplex における[pkgVisio - Visio 2013 XML 操作](https://pkgvisio.codeplex.com/documentation)プロジェクト。 
    
  - YouTube における動画[pkgVisio_pt1](https://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be)。 
    
  - YouTube における動画[pkgVisio_pt2](https://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be)。 
    
- [Visio デベロッパー センター](https://developer.microsoft.com/visio)
    
- [Office Open XML 形式のドキュメントの操作](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa982683(v=office.12))
    
- [名前空間を持つドキュメントを作成する (C#) (LINQ to XML)](https://docs.microsoft.com/previous-versions/bb387075(v=vs.140))
    
- [Microsoft Office を起動せず、ドキュメントにカスタム XML パーツを追加する](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/bb608597(v=vs.90))
    

