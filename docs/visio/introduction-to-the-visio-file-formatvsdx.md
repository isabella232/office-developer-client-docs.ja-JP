---
title: Visio ファイル形式 (.vsdx) の概要
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.assetid: 69736f40-8f67-46c2-abf6-82dffecb2274
description: Visio 2013 の新しいファイル形式について説明し、プログラムを使用して Visio 2013 ファイル形式で作業するための上位レベルの概念を確認し、Visio 2013 ファイルを検証する簡単なコンソール アプリケーションを作成します。
localization_priority: Priority
ms.openlocfilehash: 74c0f05a1db280386f3dc9dfd23da73a9b2daaf5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699073"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a>Visio ファイル形式 (.vsdx) の概要

Visio 2013 の新しいファイル形式について説明し、プログラムを使用して Visio 2013 ファイル形式で作業するための上位レベルの概念を確認し、Visio 2013 ファイルを検証する簡単なコンソール アプリケーションを作成します。
  
|||
|:-----|:-----|
|**この記事の内容**         [概要](#vis15_IntroVSDX_Intro)          [Visio 2013 ファイル形式の "中身" について](#vis15_IntroVSDX_What)          [開発者が Visio 2013 ファイル形式で作業するためのシナリオ](#vis15_IntroVSDX_Scenarios)          [プログラムを使用した Visio 2013 ファイル形式の参照](#vis15_IntroVSDX_Explore)          [その他のリソース](#vis15_IntroVSDX_Resources)||
   
## <a name="introduction"></a>概要
<a name="vis15_IntroVSDX_Intro"> </a>

Visio 2013 では、Visio の新しいファイル形式 (.vsdx) が導入されています。これは、Visio のバイナリ ファイル形式 (.vsd) と Visio XML 図面ファイル形式 (.vdx) に代わるものです。 Visio 2013 のファイル形式は Open Packaging Conventions と XML に基づいているため、これらのテクノロジについて詳しい知識のある開発者であれば、プログラムを使用して Visio 2013 のファイル形式で作業する方法にすぐ慣れていただくことができます。 Visio の以前のバージョンの Visio XML 図面ファイル形式 (.vdx) について詳しい知識のある開発者の方は、.vsdx ファイル形式の一部に同じ XML 構造が数多く使用されていることに気づかれることでしょう。 サード パーティ製のソフトウェアでは、Visio ファイルをファイル形式レベルで操作できるため、Visio ファイルとの相互運用性が大幅に向上します。 Visio 2013 のファイル形式は、Microsoft SharePoint Server 2013 の Visio Services でサポートされています。SharePoint Server に発行するための "中間" ファイル形式は不要です。
  
Visio 2013 ファイル形式を構成するファイルの種類 (拡張子) は複数あります。 拡張子は次のとおりです。
  
- .vsdx (Visio 図面)
    
- .vsdm (Visio マクロ対応図面)
    
- .vssx (Visio ステンシル)
    
- .vssm (Visio マクロ対応ステンシル)
    
- .vstx (Visio テンプレート)
    
- .vstm (Visio マクロ対応テンプレート)
    
> [!NOTE]
> マクロ対応ファイル (.vsdm、.vssm、.vstm) でのみ VBA マクロを保存できます。マクロを .vsdx、.vssx、または .vstx 拡張子のファイルで保存することはできません。 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a>Visio 2013 ファイル形式の "中身" について
<a name="vis15_IntroVSDX_What"> </a>

Visio 2013 のファイル形式では、Open Packaging Conventions (OPC) が使用されています。OPC とは、関連するリソースと共に、アプリケーション データを ZIP ファイルなどのコンテナーを使用して格納するための構造化された手法を定義するものです。 基本的なレベルでは、Visio 2013 のファイルは実際のところ、他の種類のファイルを含む ZIP コンテナーです。 Visio 2013 で図面を .vsdx ファイルとして保存し、Windows エクスプローラーでファイル拡張子を "\*.zip" に変更すると、そのファイルをフォルダーのように開いて内部のコンテンツを確認することができます。
  
> [!NOTE]
>  Open Packaging Conventions については、この記事では簡単なご紹介のみとなります。 規則の詳細な範囲については、他の記事でご紹介しています。Open Packaging Conventions 自体の詳細については、[OPC: データのパッケージ化のための新しい標準](https://msdn.microsoft.com/magazine/cc163372.aspx)をご覧ください。 Open Packaging Conventions と、Microsoft Office ファイルでのそれらの使用に関する詳細については、[Open Packaging Conventions の基本](https://msdn.microsoft.com/library/ee361919.aspx)と [Office (2007) Open XML ファイル形式の概要](https://msdn.microsoft.com/library/aa338205.aspx)をご覧ください。 
  
### <a name="packages-and-package-parts"></a>パッケージとパッケージ パーツ

上述のとおり、Visio 2013 ファイルは ZIP コンテナー、つまり "パッケージ" であり、それらには他のファイル ("パッケージ パーツ") が格納されています。 XML ファイル、画像、そして VBA ソリューションさえも、パッケージ パーツとして使用することができます。 パッケージ内のパーツはさらに 2 つの大きなカテゴリ、"文書パーツ" と "リレーションシップ パーツ" に分類することができます。 文書パーツには、Visio ファイルの実際のコンテンツとメタデータが含まれます。たとえば、ファイル名、最初のページとそのページに含まれるすべての図形、そして図形のデータ接続などです。 パッケージ内の画像とテキスト ファイルは、文書パーツとしてみなされます。 リレーションシップ パーツについては、この記事の後半で詳しく説明します。
  
> [!NOTE]
> ZIP ユーティリティを使用して Visio 2013 のファイルを開くと、多くの場合、その ZIP パッケージに複数のフォルダーが含まれていることが確認できます。 ZIP ユーティリティを使用すれば、これらのサブアドレスをフォルダーのように操作することができます。 ただし、これらの "フォルダー" は ZIP パッケージ内のサブアドレスを表すものであり、実際にはフォルダーではありません。 ソリューション内でこれらのサブアドレスで作業する場合、フォルダーと同等の処理を実行することはできません。 
  
パッケージ パーツ (文書パーツとリレーション パーツの両方) もコンテンツの種類に関連付けられています。これらのコンテンツの種類は、MIME メディアの種類を定義する文字列です。これらのコンテンツの種類は、ファイルに含めることができる MIME の種類を指定し、調査します。
  
### <a name="relationships"></a>リレーションシップ

リレーションシップ パーツ (拡張子 "\*.rels" で終わる、"_rels" フォルダーに格納されているパーツ) は、パッケージ内のパーツの相互関係を記述し、ファイルの構成を提供します。 スタンドアロン XML ドキュメントでは、要素の親/子関係を使用して、エンティティの相互関係を決定します。 それ以外のファイルの場合、その他の階層やファイル フォルダー構造を使用して、ファイル内のコンテンツ間の相互作用を記述します。 Visio 2013 のファイル形式のパッケージは、そのパッケージに正しいパーツのセットが含まれており、かつパーツ間のリレーションシップが含まれていれば、有効な Visio ファイルになります。 
  
リレーションシップ パーツは XML ドキュメントであり、パッケージ内の異なる文書パーツ間の関係を説明します。これは次の2 つのアイテム間の関係を定義します。指定されたソース (リレーションシップ ファイルの名前と場所により定義) および指定されたターゲット文書パーツ。例えば、リレーションシップ パーツは、ファイルに関連付けられたマスター シェイプ、ページとファイルおよびページ同士を互いに関連付ける方法、および画像とオブジェクトを特定のページに関連付ける方法を示すために使用されます。 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a>Visio VDX スキーマとの類似点と相違点

前述のように、過去のバージョンの Visio には、XML ベースのファイル形式である Visio XML 図面形式 (.vdx) が含まれていました  (過去のバージョンの Visio で、Visio XML 図面形式に使用されていたスキーマは、DatadiagramML と呼ばれています)。Visio の XML スキーマの一部は、2 つのファイル形式間では同じままです。 たとえば、**Windows** 要素とその子要素については、**Windows** 要素が現在 XML ドキュメント (window.xml) のルート要素であるという点を除き、変更はありません。 
  
XML 図面形式と Visio 2013 のファイル形式の最大の相違点は、パッケージです。 XML 図面形式は、通常のスタンドアロン XML と同じように操作することができます。Visio 2013 のファイル形式は、パッケージとして操作する必要があります。 Visio 2013 では、使いやすくするために XML がパーツに分割されています。 もう 1 つの大きな変更点として、Visio 2013 のファイル形式では、すべてのドキュメント プロパティが、OPC 標準に記述された文書パーツに格納されます (app.xml、core.xml、custom.xml)。
  
さらに、すべての Visio 開発者が認識する必要がある重大な変更点が 1 つあります。それは、**セル**、**行**、および**セクション**要素の導入です。 XML 図面ファイル形式スキーマでは、ShapeSheet 内の各行と各セルは名前付き要素で表されます。 たとえば、あるドキュメントにページが 1 つ存在し、そのページには **PinX** 値が "2" (図形の回転ピンが図面の左端から 2 インチの場所にあることを意味します) である図形が含まれているとします。 次のコードは、XML 図面ファイル形式でのその設定に関連するマークアップを示します。 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

ここで、**PinX** 要素は **XForm** 要素の子であり、XForm 要素はさらに **Shape** 要素の子です。 これは Visio の ShapeSheet UI をモデルにしています。ここでは、**PinX** セルが図形の **Shape Transform** セクションに含まれます。 
  
Visio 2013 のファイル形式では、ShapeSheet 内のすべてのセル (**PinX**、**LinePattern**、**Geometry** セクション内の **MoveTo** 行内の **X** セルなど) が、1 つの種類の XML 要素、つまり **Cell** 要素で表されます。 異なる **Cell** 要素は、それらの **N** 属性の値によって互いに区別されます。 そのため、上記の例の場合、ShapeSheet 内の **PinX** セルに含まれているデータは、次のコードに示すように VSDX ファイルに格納されます。 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

**PinX** の **Cell** 要素 (同様に、**LinePattern** や **LockSelect**などの "シングルトン セル" と呼ばれるその他の名前付きの各セル) は、**Shape** 要素の直接の子です。 **PinX** セルを含む行を表すための一意の要素は必要ありません。**PinX** 要素は各図形に 1 つしか存在しないためです。
  
次に、**Geometry** セクションなど、表形式データが含まれるセクションについて説明します。 このようなセクション内のセルの場合、Visio 2013 のファイル形式スキーマではデータの格納に **Section** と **Row** 要素が使用されます (これらの要素は以下に示すように **N** 属性や **T** 属性で識別されます)。 たとえば、前述の例で使用した図形で、**Geometry 1** セクションにデータが格納される場合、XML 図面スキーマでは次のコードのようになります。 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <!--- Other cells in the ShapeSheet -->
    <Geom IX="0">
        <!--- Other cells and rows in the Geometry 1 section -->
        <LineTo IX="1">
            <X F="Width*0">0</X>
            <Y F="Height*0">0</Y>
        </LineTo>
    </Geom>
</Shape>

```

ただし、Visio 2013 ファイルでは次のコードのようになります。
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <!--- Other cells in the ShapeSheet -->
    <Section N="Geometry" IX="0"> 
        <!--- Other cells and rows in the Geometry 1 section -->
        <Row IX="1" T="LineTo">
            <Cell V="0" N="X" V="Width*0" />
            <Cell V="0" N="Y" V="Height*0" />
        </Row>
    </Section>
</Shape>

```

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a>開発者が Visio 2013 ファイル形式で作業するためのシナリオ
<a name="vis15_IntroVSDX_Scenarios"> </a>

前述のように、Visio 2013 のファイル形式では ZIP ファイルや XML などのいくつかの一般的なテクノロジを使用して、データが格納されます。 Visio 2013 図面をファイル レベルで操作する場合、ソリューションに必要なのは、ZIP ファイルや XML での作業に関連付けられた .NET Framework の名前空間とクラス ([System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) や [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx) など) を使用することだけです。
  
Visio 2013 ファイル形式の開発者にとっての主なメリットは、Visio のクライアント アプリケーションを自動化することなく、Visio 2013 ファイルの読み取りと書き込みができるという点です。 開発者が Visio 2013 ファイル形式で作業するシナリオには、次のようなものがあります。
  
- 個々の Visio 2013 ファイル内の特定のデータをチェックする。 ファイル全体を抽出することなく、ZIP コンテナーから 1 つのアイテムを選択して読み取ることができます。
    
- Visio 2013 ファイルのライブラリを特定のコンテンツで更新する。 プログラムを使用してすべての背景ページのロゴを変更し、新しいブランド ガイドラインを反映させることができます。
    
- Visio 2013 ファイルを使用するアプリケーションを作成する。 たとえば、Visio ワークフロー図を読み取り、そのワークフローを基にした独自のビジネス ロジックを実行するツールを作成できます。
    
これらのソリューションは標準の .NET Framework アセンブリを使用するため、クライアント コンピューター上で実行できるソリューションの大半をサーバーでも実行することができます。
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a>プログラムを使用した Visio 2013 ファイル形式の参照
<a name="vis15_IntroVSDX_Explore"> </a>

Visio 2013 ファイル形式で作業する開発者にとって最も基本的で重要なのは、ファイルをパッケージとして開き、パッケージ内の個々のパーツにアクセスするという作業です。 WindowsBase.dll 内の **System.IO.Packaging.Package** には、パッケージとパーツを開いて操作できるようにするクラスが多く含まれています。 
  
次のコード サンプルでは、.vsdx ファイルを開いて、パッケージ内のパーツのリストを読み取り、各パーツに関する情報を取得する方法を確認できます。
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a>.vsdx ファイルを開いて文書パーツを表示するには

1. Visio 2013 を開き、新規ドキュメントを作成します。
    
2. 作成した新しいドキュメントをデスクトップに保存します。
    
3. Visual Studio 2012 を開きます。
    
4. [**ファイル**] メニューで [**新規作成**] を選択し、[プロジェクト] を選択します。
    
5. [**Visual C#**] または [**Visual Basic**] の下で [**Windows**] を展開し、[**コンソール アプリケーション**] を選択します。
    
6. [**名前**] ボックスに、「VisioFileExplorer」と入力します。 コンソール アプリケーション プロジェクトが開きます。 
    
7. [**ソリューション エクスプローラー**] で [**VisioFileExplorer**] を右クリックし、[**参照の追加**] をクリックします。 
    
8. [**参照の追加**] ダイアログ ボックスの [**アセンブリ**] の下で、[**フレームワーク**] を展開し、[**WindowsBase**] を選択します。
    
9. 次のコードをソリューションに貼り付けます。
    
  ```cs
  using System;
  using System.Collections.Generic;
  using System.Linq;
  using System.Text;
  using System.IO;
  using System.IO.Packaging;
  using System.Diagnostics;
  namespace VisioFileExplorer
  {
      class Program
      {
          static void Main(string[] args)
          {    
              try
              {
                  Console.WriteLine("Opening the VSDX file ...");
                  // Need to get the folder path for the Desktop
                  // where the file is saved.
                  string dirPath = System.Environment.GetFolderPath(
                      System.Environment.SpecialFolder.Desktop);
                  DirectoryInfo myDir = new DirectoryInfo(dirPath);
                  // It is a best practice to get the file name string
                  // using a FileInfo object, but it isn't necessary.
                  FileInfo[] fInfos = myDir.GetFiles("*.vsdx");
                  FileInfo fi = fInfos[0];
                  string fName = fi.FullName;
                  // We're not going to do any more than open
                  // and read the list of parts in the package, although
                  // we can create a package or read/write what's inside.
                  using (Package fPackage = Package.Open(
                      fName, FileMode.Open, FileAccess.Read))
                  {
                      
                      // The way to get a reference to a package part is
                      // by using its URI. Thus, we're reading the URI
                      // for each part in the package.
                      PackagePartCollection fParts = fPackage.GetParts();
                      foreach (PackagePart fPart in fParts)
                      {
                          Console.WriteLine("Package part: {0}", fPart.Uri);
                      }
                  }   
              }
              catch (Exception err)
              {
                  Console.WriteLine("Error: {0}", err.Message);
              }
              finally
              {
                  Console.Write("\nPress any key to continue ...");
                  Console.ReadKey();
              }   
          }
      }
  }
  ```

  ```vb
  Imports System
  Imports System.Collections.Generic
  Imports System.Linq
  Imports System.Text
  Imports System.IO
  Imports System.IO.Packaging
  Imports System.Diagnostics
  Module Module1
      Sub Main()
          Try
              Console.WriteLine("Opening the VSDX file ...")
              ' Need to get the folder path for the Desktop
              ' or where the file is saved.
              Dim dirPath As String = System.Environment.GetFolderPath( _
                  System.Environment.SpecialFolder.Desktop)
              Dim myDir As New DirectoryInfo(dirPath)
              ' It is a best practice to get the file name string
              ' using a FileInfo object, but it isn't necessary.
              Dim fInfos As FileInfo() = myDir.GetFiles("*.vsdx")
              Dim fi As FileInfo = fInfos(0)
              Dim fName As String = fi.FullName
              ' We don't need to do any more than open
              ' and read the list of parts in the package, although
              ' we can create a package or read/write what's inside.
              Using fPackage As Package = Package.Open( _
                  fName, FileMode.Open, FileAccess.Read)
                  ' The way to get a reference to a document part is
                  ' by using its URI. Thus, we're reading the URI
                  ' for each document part in the package.
                  Dim fParts As PackagePartCollection = fPackage.GetParts()
                  For Each fPart As PackagePart In fParts
                      Console.WriteLine("Package part: {0}", fPart.Uri)
                  Next
              End Using
          Catch err As Exception
              Console.WriteLine("Error: {0}", err.Message)
          Finally
              Console.Write(vbLf &amp; "Press any key to continue ...")
              Console.ReadKey()
          End Try
      End Sub
  End Module
  
  ```

10. F5 キーを押してソリューションをデバッグします。プログラムの実行が完了したら、任意のキーを押して終了します。
    
## <a name="see-also"></a>関連項目
<a name="vis15_IntroVSDX_Resources"> </a>

Visio 2013 ファイル形式、Open Packaging Conventions、プログラムを使用して Visio 2013 や Office OpenXML ファイルで作業する方法の詳細については、次のリソースを参照してください。
  
- [開発者向けの Visio 情報](https://msdn.microsoft.com/office/aa905478.aspx)
    
- [OPC: データのパッケージ化のための新しい標準](https://msdn.microsoft.com/magazine/cc163372.aspx)
    
- [Open Packaging Conventions の基本](https://msdn.microsoft.com/library/ee361919.aspx)
    
- [Office (2007) Open XML ファイル形式の概要](https://msdn.microsoft.com/library/aa338205.aspx)
    

