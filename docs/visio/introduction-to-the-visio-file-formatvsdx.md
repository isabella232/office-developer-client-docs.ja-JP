---
title: Visio ファイル形式 (.vsdx) の概要
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 69736f40-8f67-46c2-abf6-82dffecb2274
description: プログラムで、Visio 2013 のファイル形式を操作するためのいくつかの大まかな概念を表示する Visio 2013 では、新しいファイル形式について説明して、Visio 2013 ファイルをチェックする簡単なコンソール アプリケーションを作成します。
ms.openlocfilehash: 4efa90ee513def005653f4f8717b0149de1cdc3d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389366"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a>Visio ファイル形式 (.vsdx) の概要

プログラムで、Visio 2013 のファイル形式を操作するためのいくつかの大まかな概念を表示する Visio 2013 では、新しいファイル形式について説明して、Visio 2013 ファイルをチェックする簡単なコンソール アプリケーションを作成します。
  
|||
|:-----|:-----|
|**この資料に記載されて**         [概要](#vis15_IntroVSDX_Intro)          [「ボンネット」Visio 2013 のファイル形式とは何ですか?](#vis15_IntroVSDX_What)          [Visio 2013 のファイル形式を操作するための開発者のシナリオ](#vis15_IntroVSDX_Scenarios)          [Visio 2013 のファイル形式をプログラムで表示](#vis15_IntroVSDX_Explore)          [その他のリソース](#vis15_IntroVSDX_Resources)||
   
## <a name="introduction"></a>概要
<a name="vis15_IntroVSDX_Intro"> </a>

Visio 2013 では、Visio で、Visio ファイルをバイナリ形式 (.vsd) ファイル形式の Visio XML 図面 (.vdx) の新しいファイル形式 (.vsdx) を紹介します。 Visio 2013 のファイル形式は、パッケージ化規則を開くと、XML に基づいているためこれらのテクノロジに精通している開発者は簡単に Visio 2013 のファイルをプログラムから操作する方法を説明します。 Visio の以前のバージョンの Visio XML 図面 (.vdx) ファイル形式を熟知している開発者には、同じ XML 構造体の .vsdx ファイル形式の多くを検索できます。 サードパーティ製のソフトウェアは、ファイル形式のレベルでの Visio ファイルを操作できますので、Visio のファイルとの相互運用性が大幅に増加します。 Visio 2013 のファイル形式は、SharePoint サーバーへの発行の「中間」ファイル形式の必要はありません、Microsoft SharePoint Server 2013 での Visio のサービスでサポートされます。
  
種類のファイルの拡張子を Visio 2013 のファイル形式を構成するにはあります。 これらの拡張機能は次のとおりです。
  
- .vsdx (Visio 図面)
    
- .vsdm (Visio マクロ対応図面)
    
- .vssx (Visio ステンシル)
    
- .vssm (Visio マクロ対応ステンシル)
    
- .vstx (Visio テンプレート)
    
- .vstm (Visio マクロ対応テンプレート)
    
> [!NOTE]
> マクロ対応ファイル (.vsdm、.vssm、.vstm) でのみ VBA マクロを保存できます。マクロを .vsdx、.vssx、または .vstx 拡張子のファイルで保存することはできません。 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a>「ボンネット」Visio 2013 のファイル形式とは何ですか。
<a name="vis15_IntroVSDX_What"> </a>

Visio 2013 のファイル形式では、開いているパッキング規則 (OPC)、いくつか sort─for 例では、ZIP ファイルのコンテナーを使用して、関連するリソースとアプリケーション データを格納する構造化された手段を定義するを使用します。 基本的なレベルでは、Visio 2013 が本当にその他の種類のファイルを含む ZIP コンテナーです。 .Vsdx ファイルとして Visio 2013 で図面を保存する、ファイルの拡張子を変更する実際には、"\*.zip"ファイルがフォルダー内のコンテンツを表示するように Windows エクスプ ローラーで開くとします。
  
> [!NOTE]
>  この資料には、開いているパッケージ化規則の概要のみが含まれています。 他の記事での表記規則のコード カバレッジの詳細についてを見つけることができます: > 自体開くパッケージ化規則の詳細についてを参照してください[OPC: A 新しい標準的なパッケージのデータを](https://msdn.microsoft.com/magazine/cc163372.aspx)。 > のパッケージ化規則を開くと Microsoft Office ファイルでの使用の詳細については、[オープンのパッケージ化規則の基礎](https://msdn.microsoft.com/library/ee361919.aspx)と[、(2007) の Office オープン XML ファイル形式の概要](https://msdn.microsoft.com/library/aa338205.aspx)を参照してください。 
  
### <a name="packages-and-package-parts"></a>パッケージとパッケージ パーツ

以前のバージョンを起動する、Visio 2013 ファイルは、ZIP コンテナーまたは「パッケージ」の (「部品パッケージ化」と呼ばれる) 他のファイルを保持しています。 パッケージ パーツは、XML ファイル、イメージ、VBA ソリューションにもできます。 パッケージ内のパーツがさらに分割する 2 つのカテゴリ、ドキュメント パーツ」および「リレーションシップ パーツ」です。 文書パーツは、実際のコンテンツとメタデータ ファイル、最初のページとそのすべてのそれに含まれる図形の名前と同じように、Visio ファイルが含まれているし、図形のデータ接続にも。 イメージやパッケージ内のテキスト ファイルは、ドキュメントの一部と見なされます。 リレーションシップ パーツは、詳細についてはこの資料の後半で説明します。
  
> [!NOTE]
> ZIP ユーティリティを使用して Visio 2013 のファイルを開く場合はいくつかのフォルダーを ZIP パッケージ内に含まれている可能性があります表示できます。 ZIP ユーティリティを使用するフォルダーと同様にこれらの下位アドレスでも操作できます。 ただし、これらの「フォルダー」は、実際のフォルダーは、ZIP パッケージ内のサブのアドレスを表します。 ソリューションでは、これらの形式のアドレスを使用するプログラムに対応するフォルダーを使うことはできません。 
  
パッケージ パーツ (文書パーツとリレーション パーツの両方) もコンテンツの種類に関連付けられています。これらのコンテンツの種類は、MIME メディアの種類を定義する文字列です。これらのコンテンツの種類は、ファイルに含めることができる MIME の種類を指定し、調査します。
  
### <a name="relationships"></a>関係

リレーションシップ パーツ (末尾に拡張子が"\*.rels"と"_rels] フォルダーに格納されます) パッケージ内のパーツを互いに関連付ける方法について説明し、ファイルの構造。 スタンドアロンの XML ドキュメントは、他のエンティティの関係を判断するのに要素の親/子関係を使用します。 その他のファイルは、他の階層やファイルのフォルダー構造を使用してファイル内のコンテンツの相互作用を記述することがあります。 Visio 2013 のファイル形式で、パッケージは有効な Visio ファイルの部分の適切なセットが含まれているし、パッケージには、パーツ間のリレーションシップが含まれています。 
  
リレーションシップ パーツは XML ドキュメントであり、パッケージ内の異なる文書パーツ間の関係を説明します。これは次の2 つのアイテム間の関係を定義します。指定されたソース (リレーションシップ ファイルの名前と場所により定義) および指定されたターゲット文書パーツ。例えば、リレーションシップ パーツは、ファイルに関連付けられたマスター シェイプ、ページとファイルおよびページ同士を互いに関連付ける方法、および画像とオブジェクトを特定のページに関連付ける方法を示すために使用されます。 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a>類似点と Visio VDX スキーマの相違点

前述のように、過去のバージョンの Visio には、XML ベースのファイル形式では、Visio XML 図面フォーマットまたは .vdx も含まれています。 (以前のバージョンの Visio では、Visio の XML 図面フォーマットに使用されるスキーマと呼びます DatadiagramML。Visio の XML スキーマからいくつかの部分に残る 2 つのファイル形式の間で同じです。 たとえば、 **Windows**の要素とその子 unchanged─with **Windows**要素が XML ドキュメント (window.xml) のルート要素で、これである例外のままです。 
  
XML 図面形式と Visio 2013 のファイル形式の最大の違いは、パッケージです。 通常のスタンドアロンの XML のように、図面フォーマットの XML ファイルを操作する可能性があります。パッケージとしては、Visio 2013 のファイル形式を操作する必要があります。 Visio 2013 での XML に分割されたを簡単に使用するパーツ。 別の顕著な変更では、Visio 2013 のファイル形式が、文書パーツ標準 OPC によって記述される (app.xml、core.xml、custom.xml) にすべてのドキュメント プロパティを格納します。
  
ただし、Visio のすべての開発者が注意しなければならない 1 つの重要な変更がある:**セル****行**、および**セクション**の要素を導入します。 図面ファイル形式の XML スキーマで個別の行と、[シェイプ シートのセルは、名前付きの要素によって表されます。 たとえば、「2」(つまり、図形の回転ピンが図面の左端からの 2 インチ) の **[pinx]** の値を持つ図形が含まれている 1 つのページを含むドキュメントがあることを想像してください。 XML 図面のファイル形式を設定するに関連するマークアップは、次のコードに表示されます。 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

ここでは、 **[pinx]** 要素は、**図形**要素の子である**XForm**の要素の子です。 これは、図形の [**図形情報**] セクションの **[pinx]** セルが含まれている Visio シェイプ シート UI をモデル化します。 
  
Visio 2013 ファイル形式で、ShapeSheet─ **[pinx]**、 **LinePattern**etc.─are の**セル**要素、XML 要素の 1 つの型で表される **[Geometry** ] セクションで **[moveto]** 行で、[ **X** ] セル内のすべてのセル。 別の**セル**要素は、[ **N** ] 属性の値によって互いから individuated します。 したがって、上記の例は、VSDX ファイル、次のコードに示すように、シェイプ シートの **[pinx]** セルに含まれるデータが格納されます。 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

**[Pinx]** (およびその他の**LinePattern**など**lockselect] を有効**に [単一のセル] と呼ばれる、個々 の名前付きセル) の**セル**要素は、**図形**要素の直接の子です。 各図形は、1 つの **[pinx]** を持つことができますのみ、 **[pinx]** セルを含む行を表す一意の要素は必要ありません。
  
[ **Geometry** ] セクションと同様に、表形式のデータが含まれているセクションについて説明します。 それらのセクションで、セルの Visio 2013 のファイル形式のスキーマ**のセクション**を使用して、 **N**属性または**T**属性に示すように below─to を使用して識別**行**の elements─also には、データが含まれます。 たとえば、前の例から同じ図形には、図面を XML スキーマでは、次のコードのような**ジオメトリの 1**セクションのデータが含まれます。 
  
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

ただし、Visio 2013 ファイルに次のコードのようになります。
  
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

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a>Visio 2013 ファイル形式で作業するための開発者向けシナリオ
<a name="vis15_IntroVSDX_Scenarios"> </a>

前述したように、Visio 2013 のファイル形式は、ZIP ファイルやデータを格納する XML のようないくつかの汎用的なテクノロジを活用します。 Visio 2013 がファイル レベルでの図面を操作するには、ソリューションは、.NET Framework 名前空間と ZIP ファイルまたは XML、 [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx)や[System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx)などの操作に関連付けられたクラスを使用する場合のみ必要があります。
  
Visio 2013 のファイル形式の開発者の主なメリットは、読み取りし、Visio クライアント アプリケーションを自動化することがなく、Visio 2013 のファイルに書き込むことができます。 Visio 2013 のファイル形式を操作するための開発者を検討するいくつかのシナリオは次のとおりです。
  
- 特定のデータの個別の Visio 2013 ファイルをチェックします。 ZIP コンテナーから 1 つの項目は、ファイル全体を抽出することがなく選択的に読み取ることができます。
    
- Visio 2013 ファイルのライブラリを特定のコンテンツで更新しています。 プログラムを使用してすべての新しいブランドのガイドラインを反映するように背景ページにロゴを変更します。
    
- Visio 2013 のファイルを使用するアプリケーションを作成します。 たとえば、Visio のワークフロー図を読み取り、そのワークフローに基づいた独自のビジネス ロジックを実行し、ツールを構築できます。
    
これらのソリューションは標準の .NET Framework アセンブリを使用するため、クライアント コンピューター上で実行できるソリューションの大半をサーバーでも実行することができます。
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a>プログラムを使用して Visio 2013 ファイル形式を探索する
<a name="vis15_IntroVSDX_Explore"> </a>

Visio 2013 のファイル形式を使用するあらゆる開発者のための最も基本的で根本的なタスクがパッケージとしてファイルを開くと、パッケージ内の個々 の部分へのアクセスします。 お**System.IO.Packaging.Package**を開き、パッケージとパーツを操作することを可能にする多くのクラスが含まれています。 
  
次のコード サンプルでは、.vsdx ファイルを開いて、パッケージ内のパーツのリストを読み取り、各パーツに関する情報を取得する方法を確認できます。
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a>.vsdx ファイルを開いて文書パーツを表示するには

1. Visio 2013 を開き、新しいドキュメントを作成します。
    
2. 新しい文書を作成してデスクトップに保存します。
    
3. Visual Studio 2012 を開きます。
    
4. [**ファイル**] メニューの [**新規**作成] を選択し、[* * プロジェクト * *。
    
5. [**Visual C#**] または [**Visual Basic**] で、[**Windows**] を展開して、[**コンソール アプリケーション**] を選択します。
    
6. **[名前**] ボックスで、'VisioFileExplorer' を入力します。 コンソール アプリケーション プロジェクトを開きます。 
    
7. [**ソリューション エクスプローラー**] で、[**VisioFileExplorer**] を右クリックして、[**参照の追加**] をクリックします。 
    
8. [**参照の追加**] ダイアログ ボックスで、[**アセンブリ**] の [**フレームワーク**] を展開して [**WindowsBase**] を選択します。
    
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

Visio 2013 のファイル形式、開いているパッケージ化規則、または Office OpenXML ファイルの 2013or をプログラムから操作する方法の詳細については、次のリソースを参照してください。
  
- [開発者は、Visio](https://msdn.microsoft.com/office/aa905478.aspx)
    
- [OPC: データをパッケージ化するための新しい標準](https://msdn.microsoft.com/magazine/cc163372.aspx)。
    
- [オープンなパッケージング規則の基礎](https://msdn.microsoft.com/library/ee361919.aspx)
    
- [Office (2007) オープン XML ファイル形式の概要](https://msdn.microsoft.com/library/aa338205.aspx)
    

