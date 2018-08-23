---
title: Visio ファイル形式 (.vsdx) の概要
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 69736f40-8f67-46c2-abf6-82dffecb2274
description: プログラムで、Visio 2013 のファイル形式を操作するためのいくつかの大まかな概念を表示する Visio 2013 では、新しいファイル形式について説明して、Visio 2013 ファイルをチェックする簡単なコンソール アプリケーションを作成します。
ms.openlocfilehash: aa3497af7c467c8f51ab80ab82071776568b4978
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805594"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a><span data-ttu-id="132d7-103">Visio ファイル形式 (.vsdx) の概要</span><span class="sxs-lookup"><span data-stu-id="132d7-103">Introduction to the Visio file format (.vsdx)</span></span>

<span data-ttu-id="132d7-104">プログラムで、Visio 2013 のファイル形式を操作するためのいくつかの大まかな概念を表示する Visio 2013 では、新しいファイル形式について説明して、Visio 2013 ファイルをチェックする簡単なコンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="132d7-104">Learn about the new file format in Visio 2013, explore some high-level concepts for working with the Visio 2013 file format programmatically, and create a simple console application that examines a Visio 2013 file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="132d7-105">**この資料に記載されて**         [概要](#vis15_IntroVSDX_Intro)          [「ボンネット」Visio 2013 のファイル形式とは何ですか?](#vis15_IntroVSDX_What)</span><span class="sxs-lookup"><span data-stu-id="132d7-105">**In this article**         [Introduction](#vis15_IntroVSDX_Intro)          [What is the Visio 2013 file format "under the hood"?](#vis15_IntroVSDX_What)</span></span>          <span data-ttu-id="132d7-106">[Visio 2013 のファイル形式を操作するための開発者のシナリオ](#vis15_IntroVSDX_Scenarios)          [Visio 2013 のファイル形式をプログラムで表示](#vis15_IntroVSDX_Explore)          [その他のリソース](#vis15_IntroVSDX_Resources)</span><span class="sxs-lookup"><span data-stu-id="132d7-106">[Developer scenarios for working with the Visio 2013 file format](#vis15_IntroVSDX_Scenarios)          [Exploring the Visio 2013 file format programmatically](#vis15_IntroVSDX_Explore)          [Additional resources](#vis15_IntroVSDX_Resources)</span></span>||
   
## <a name="introduction"></a><span data-ttu-id="132d7-107">概要</span><span class="sxs-lookup"><span data-stu-id="132d7-107">Introduction</span></span>
<span data-ttu-id="132d7-108"><a name="vis15_IntroVSDX_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="132d7-108"></span></span>

<span data-ttu-id="132d7-109">Visio 2013 では、Visio で、Visio ファイルをバイナリ形式 (.vsd) ファイル形式の Visio XML 図面 (.vdx) の新しいファイル形式 (.vsdx) を紹介します。</span><span class="sxs-lookup"><span data-stu-id="132d7-109">Visio 2013 introduces a new file format (.vsdx) for Visio that replaces the Visio binary file format (.vsd) and Visio XML Drawing file format (.vdx).</span></span> <span data-ttu-id="132d7-110">Visio 2013 のファイル形式は、パッケージ化規則を開くと、XML に基づいているためこれらのテクノロジに精通している開発者は簡単に Visio 2013 のファイルをプログラムから操作する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="132d7-110">Because the Visio 2013 file format is based upon Open Packaging Conventions and XML, developers who are familiar with these technologies can quickly learn how to work with Visio 2013 files programmatically.</span></span> <span data-ttu-id="132d7-111">Visio の以前のバージョンの Visio XML 図面 (.vdx) ファイル形式を熟知している開発者には、同じ XML 構造体の .vsdx ファイル形式の多くを検索できます。</span><span class="sxs-lookup"><span data-stu-id="132d7-111">Developers who are familiar with the Visio XML Drawing file format (.vdx) from previous versions of Visio can find many of the same XML structures within the parts of .vsdx file format.</span></span> <span data-ttu-id="132d7-112">サードパーティ製のソフトウェアは、ファイル形式のレベルでの Visio ファイルを操作できますので、Visio のファイルとの相互運用性が大幅に増加します。</span><span class="sxs-lookup"><span data-stu-id="132d7-112">Interoperability with Visio files is greatly increased since third-party software can manipulate Visio files at a file format level.</span></span> <span data-ttu-id="132d7-113">Visio 2013 のファイル形式は、SharePoint サーバーへの発行の「中間」ファイル形式の必要はありません、Microsoft SharePoint Server 2013 での Visio のサービスでサポートされます。</span><span class="sxs-lookup"><span data-stu-id="132d7-113">The Visio 2013 file format is supported on Visio Services in Microsoft SharePoint Server 2013, without the need of an "intermediary" file format for publishing to SharePoint Server.</span></span>
  
<span data-ttu-id="132d7-114">種類のファイルの拡張子を Visio 2013 のファイル形式を構成するにはあります。</span><span class="sxs-lookup"><span data-stu-id="132d7-114">There are several file types, by extension, that comprise the Visio 2013 file format.</span></span> <span data-ttu-id="132d7-115">これらの拡張機能は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="132d7-115">These extensions include:</span></span>
  
- <span data-ttu-id="132d7-116">.vsdx (Visio 図面)</span><span class="sxs-lookup"><span data-stu-id="132d7-116">.vsdx (Visio drawing)</span></span>
    
- <span data-ttu-id="132d7-117">.vsdm (Visio マクロ対応図面)</span><span class="sxs-lookup"><span data-stu-id="132d7-117">.vsdm (Visio macro-enabled drawing)</span></span>
    
- <span data-ttu-id="132d7-118">.vssx (Visio ステンシル)</span><span class="sxs-lookup"><span data-stu-id="132d7-118">.vssx (Visio stencil)</span></span>
    
- <span data-ttu-id="132d7-119">.vssm (Visio マクロ対応ステンシル)</span><span class="sxs-lookup"><span data-stu-id="132d7-119">.vssm (Visio macro-enabled stencil)</span></span>
    
- <span data-ttu-id="132d7-120">.vstx (Visio テンプレート)</span><span class="sxs-lookup"><span data-stu-id="132d7-120">.vstx (Visio template)</span></span>
    
- <span data-ttu-id="132d7-121">.vstm (Visio マクロ対応テンプレート)</span><span class="sxs-lookup"><span data-stu-id="132d7-121">.vstm (Visio macro-enabled template)</span></span>
    
> [!NOTE]
> <span data-ttu-id="132d7-p104">マクロ対応ファイル (.vsdm、.vssm、.vstm) でのみ VBA マクロを保存できます。マクロを .vsdx、.vssx、または .vstx 拡張子のファイルで保存することはできません。</span><span class="sxs-lookup"><span data-stu-id="132d7-p104">Only the macro-enabled files (.vsdm, .vssm, .vstm) can store VBA macros. You cannot store macros in files with a .vsdx, .vssx, or .vstx extension.</span></span> 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a><span data-ttu-id="132d7-124">「ボンネット」Visio 2013 のファイル形式とは何ですか。</span><span class="sxs-lookup"><span data-stu-id="132d7-124">What is the Visio 2013 file format "under the hood"?</span></span>
<span data-ttu-id="132d7-125"><a name="vis15_IntroVSDX_What"> </a></span><span class="sxs-lookup"><span data-stu-id="132d7-125"></span></span>

<span data-ttu-id="132d7-126">Visio 2013 のファイル形式では、開いているパッキング規則 (OPC)、いくつか sort─for 例では、ZIP ファイルのコンテナーを使用して、関連するリソースとアプリケーション データを格納する構造化された手段を定義するを使用します。</span><span class="sxs-lookup"><span data-stu-id="132d7-126">The Visio 2013 file format uses the Open Packing Conventions (OPC), which defines a structured means to store application data together with related resources using a container of some sort─for example, a ZIP file.</span></span> <span data-ttu-id="132d7-127">基本的なレベルでは、Visio 2013 が本当にその他の種類のファイルを含む ZIP コンテナーです。</span><span class="sxs-lookup"><span data-stu-id="132d7-127">At a basic level, a Visio 2013 file is really a ZIP container that contains other types of files.</span></span> <span data-ttu-id="132d7-128">.Vsdx ファイルとして Visio 2013 で図面を保存する、ファイルの拡張子を変更する実際には、"\*.zip"ファイルがフォルダー内のコンテンツを表示するように Windows エクスプ ローラーで開くとします。</span><span class="sxs-lookup"><span data-stu-id="132d7-128">In fact, you can save a drawing in Visio 2013 as a .vsdx file, rename the file extension to "\*.zip" in Windows Explorer, and then open the file like a folder to see the contents inside.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="132d7-129">この資料には、開いているパッケージ化規則の概要のみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="132d7-129">This article contains only a brief overview of the Open Packaging Conventions.</span></span> <span data-ttu-id="132d7-130">他の記事での表記規則のコード カバレッジの詳細についてを見つけることができます: > 自体開くパッケージ化規則の詳細についてを参照してください[OPC: A 新しい標準的なパッケージのデータを](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx)。</span><span class="sxs-lookup"><span data-stu-id="132d7-130">You can find more detailed coverage of the conventions in other articles: >  For more information about the Open Packaging Conventions themselves, see [OPC: A New Standard for Packaging Your Data](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx).</span></span> <span data-ttu-id="132d7-131">> のパッケージ化規則を開くと Microsoft Office ファイルでの使用の詳細については、[オープンのパッケージ化規則の基礎](http://msdn.microsoft.com/en-us/library/ee361919.aspx)と[、(2007) の Office オープン XML ファイル形式の概要](http://msdn.microsoft.com/en-us/library/aa338205.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="132d7-131">>  For more information about the Open Packaging Conventions and their use in Microsoft Office files, see [Essentials of the Open Packaging Conventions](http://msdn.microsoft.com/en-us/library/ee361919.aspx) and [Introducing the Office (2007) Open XML File Formats](http://msdn.microsoft.com/en-us/library/aa338205.aspx).</span></span> 
  
### <a name="packages-and-package-parts"></a><span data-ttu-id="132d7-132">パッケージとパッケージ パーツ</span><span class="sxs-lookup"><span data-stu-id="132d7-132">Packages and Package Parts</span></span>

<span data-ttu-id="132d7-133">以前のバージョンを起動する、Visio 2013 ファイルは、ZIP コンテナーまたは「パッケージ」の (「部品パッケージ化」と呼ばれる) 他のファイルを保持しています。</span><span class="sxs-lookup"><span data-stu-id="132d7-133">As started earlier, Visio 2013 files are ZIP containers or "packages" that hold other files (called "package parts") within them.</span></span> <span data-ttu-id="132d7-134">パッケージ パーツは、XML ファイル、イメージ、VBA ソリューションにもできます。</span><span class="sxs-lookup"><span data-stu-id="132d7-134">A package part can be an XML file, an image, even a VBA solution.</span></span> <span data-ttu-id="132d7-135">パッケージ内のパーツがさらに分割する 2 つのカテゴリ、ドキュメント パーツ」および「リレーションシップ パーツ」です。</span><span class="sxs-lookup"><span data-stu-id="132d7-135">The parts within the package can be further divided into two broad categories, "document parts" and "relationship parts."</span></span> <span data-ttu-id="132d7-136">文書パーツは、実際のコンテンツとメタデータ ファイル、最初のページとそのすべてのそれに含まれる図形の名前と同じように、Visio ファイルが含まれているし、図形のデータ接続にも。</span><span class="sxs-lookup"><span data-stu-id="132d7-136">The document parts contain the actual content and metadata of the Visio file, like the name of the file, the first page and all of the shapes that it contains, and even the data connections for the shapes.</span></span> <span data-ttu-id="132d7-137">イメージやパッケージ内のテキスト ファイルは、ドキュメントの一部と見なされます。</span><span class="sxs-lookup"><span data-stu-id="132d7-137">Images and text files within the package are considered document parts.</span></span> <span data-ttu-id="132d7-138">リレーションシップ パーツは、詳細についてはこの資料の後半で説明します。</span><span class="sxs-lookup"><span data-stu-id="132d7-138">Relationship parts are described in more detail later in this article.</span></span>
  
> [!NOTE]
> <span data-ttu-id="132d7-139">ZIP ユーティリティを使用して Visio 2013 のファイルを開く場合はいくつかのフォルダーを ZIP パッケージ内に含まれている可能性があります表示できます。</span><span class="sxs-lookup"><span data-stu-id="132d7-139">If you open a Visio 2013 file using a ZIP utility, you can probably see several folders contained inside of the ZIP package.</span></span> <span data-ttu-id="132d7-140">ZIP ユーティリティを使用するフォルダーと同様にこれらの下位アドレスでも操作できます。</span><span class="sxs-lookup"><span data-stu-id="132d7-140">You can even manipulate these sub-addresses like folders using a ZIP utility.</span></span> <span data-ttu-id="132d7-141">ただし、これらの「フォルダー」は、実際のフォルダーは、ZIP パッケージ内のサブのアドレスを表します。</span><span class="sxs-lookup"><span data-stu-id="132d7-141">However, these "folders" represent sub-addresses within the ZIP package, not actual folders.</span></span> <span data-ttu-id="132d7-142">ソリューションでは、これらの形式のアドレスを使用するプログラムに対応するフォルダーを使うことはできません。</span><span class="sxs-lookup"><span data-stu-id="132d7-142">You cannot use the programmatic equivalents of folders to work with these sub-addresses in your solution.</span></span> 
  
<span data-ttu-id="132d7-p109">パッケージ パーツ (文書パーツとリレーション パーツの両方) もコンテンツの種類に関連付けられています。これらのコンテンツの種類は、MIME メディアの種類を定義する文字列です。これらのコンテンツの種類は、ファイルに含めることができる MIME の種類を指定し、調査します。</span><span class="sxs-lookup"><span data-stu-id="132d7-p109">Package parts─both document parts and relationship parts─also have associated content types. These content types are strings that define a MIME media type. These content types specify and scope the kind of MIME types that can be contained in the file.</span></span>
  
### <a name="relationships"></a><span data-ttu-id="132d7-146">関係</span><span class="sxs-lookup"><span data-stu-id="132d7-146">Relationships</span></span>

<span data-ttu-id="132d7-147">リレーションシップ パーツ (末尾に拡張子が"\*.rels"と"_rels] フォルダーに格納されます) パッケージ内のパーツを互いに関連付ける方法について説明し、ファイルの構造。</span><span class="sxs-lookup"><span data-stu-id="132d7-147">The relationship parts (which end with the extension "\*.rels" and are stored in a "_rels" folder) describe how the parts within the package relate to each other and provide the structure of the file.</span></span> <span data-ttu-id="132d7-148">スタンドアロンの XML ドキュメントは、他のエンティティの関係を判断するのに要素の親/子関係を使用します。</span><span class="sxs-lookup"><span data-stu-id="132d7-148">A standalone XML document uses the parent/child relationship of elements to determine the relationship of entities to each other.</span></span> <span data-ttu-id="132d7-149">その他のファイルは、他の階層やファイルのフォルダー構造を使用してファイル内のコンテンツの相互作用を記述することがあります。</span><span class="sxs-lookup"><span data-stu-id="132d7-149">Other files may use other hierarchies or file folder structure to describe the interaction of content in the file.</span></span> <span data-ttu-id="132d7-150">Visio 2013 のファイル形式で、パッケージは有効な Visio ファイルの部分の適切なセットが含まれているし、パッケージには、パーツ間のリレーションシップが含まれています。</span><span class="sxs-lookup"><span data-stu-id="132d7-150">For the Visio 2013 file format, the package is a valid Visio file if it contains the correct set of parts and the package contains the relationships between the parts.</span></span> 
  
<span data-ttu-id="132d7-p111">リレーションシップ パーツは XML ドキュメントであり、パッケージ内の異なる文書パーツ間の関係を説明します。これは次の2 つのアイテム間の関係を定義します。指定されたソース (リレーションシップ ファイルの名前と場所により定義) および指定されたターゲット文書パーツ。例えば、リレーションシップ パーツは、ファイルに関連付けられたマスター シェイプ、ページとファイルおよびページ同士を互いに関連付ける方法、および画像とオブジェクトを特定のページに関連付ける方法を示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="132d7-p111">Relationship parts are XML documents that describe the relationships between different document parts within the package. They define an association between two items: a specified source (defined by the name and location of the relationship file) and a specified target document part. For example, relationship parts are used to describe which shape masters are associated with the file, how pages relate to the file and to each other, or how images and objects relate to a specific page.</span></span> 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a><span data-ttu-id="132d7-154">類似点と Visio VDX スキーマの相違点</span><span class="sxs-lookup"><span data-stu-id="132d7-154">Similarities and differences with Visio VDX schema</span></span>

<span data-ttu-id="132d7-155">前述のように、過去のバージョンの Visio には、XML ベースのファイル形式では、Visio XML 図面フォーマットまたは .vdx も含まれています。</span><span class="sxs-lookup"><span data-stu-id="132d7-155">As mentioned, past versions of Visio also included an XML-based file format, the Visio XML Drawing Format or .vdx.</span></span> <span data-ttu-id="132d7-156">(以前のバージョンの Visio では、Visio の XML 図面フォーマットに使用されるスキーマと呼びます DatadiagramML。Visio の XML スキーマからいくつかの部分に残る 2 つのファイル形式の間で同じです。</span><span class="sxs-lookup"><span data-stu-id="132d7-156">(In previous versions of Visio, the schema used for the Visio XML Drawing Format is called DatadiagramML.) Some pieces from the Visio XML schema have stayed the same between the two file formats.</span></span> <span data-ttu-id="132d7-157">たとえば、 **Windows**の要素とその子 unchanged─with **Windows**要素が XML ドキュメント (window.xml) のルート要素で、これである例外のままです。</span><span class="sxs-lookup"><span data-stu-id="132d7-157">For example, the **Windows** element and its children remain unchanged─with the exception that the **Windows** element is now a root element of an XML document (window.xml).</span></span> 
  
<span data-ttu-id="132d7-158">XML 図面形式と Visio 2013 のファイル形式の最大の違いは、パッケージです。</span><span class="sxs-lookup"><span data-stu-id="132d7-158">The largest difference between the XML Drawing Format and the Visio 2013 file format is the packaging.</span></span> <span data-ttu-id="132d7-159">通常のスタンドアロンの XML のように、図面フォーマットの XML ファイルを操作する可能性があります。パッケージとしては、Visio 2013 のファイル形式を操作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="132d7-159">An XML Drawing Format file could be manipulated like a normal stand-alone XML; the Visio 2013 file format must be manipulated as a package.</span></span> <span data-ttu-id="132d7-160">Visio 2013 での XML に分割されたを簡単に使用するパーツ。</span><span class="sxs-lookup"><span data-stu-id="132d7-160">In the Visio 2013, the XML has been divided up into parts for easier consumption.</span></span> <span data-ttu-id="132d7-161">別の顕著な変更では、Visio 2013 のファイル形式が、文書パーツ標準 OPC によって記述される (app.xml、core.xml、custom.xml) にすべてのドキュメント プロパティを格納します。</span><span class="sxs-lookup"><span data-stu-id="132d7-161">Another noticeable change is that the Visio 2013 file format stores all document properties in document parts described by the OPC standard (app.xml, core.xml, custom.xml).</span></span>
  
<span data-ttu-id="132d7-162">ただし、Visio のすべての開発者が注意しなければならない 1 つの重要な変更がある:**セル****行**、および**セクション**の要素を導入します。</span><span class="sxs-lookup"><span data-stu-id="132d7-162">However, there is one significant change that all Visio developers must be aware of: the introduction of the **Cell**, **Row**, and **Section** elements.</span></span> <span data-ttu-id="132d7-163">図面ファイル形式の XML スキーマで個別の行と、[シェイプ シートのセルは、名前付きの要素によって表されます。</span><span class="sxs-lookup"><span data-stu-id="132d7-163">In the XML Drawing File Format schema, individual rows and cells in the ShapeSheet are represented by named elements.</span></span> <span data-ttu-id="132d7-164">たとえば、「2」(つまり、図形の回転ピンが図面の左端からの 2 インチ) の **[pinx]** の値を持つ図形が含まれている 1 つのページを含むドキュメントがあることを想像してください。</span><span class="sxs-lookup"><span data-stu-id="132d7-164">For example, imagine that you have a document with a single page that contains a shape with a **PinX** value of "2" (meaning that the rotation pin of the shape is 2 inches from the left edge of the drawing).</span></span> <span data-ttu-id="132d7-165">XML 図面のファイル形式を設定するに関連するマークアップは、次のコードに表示されます。</span><span class="sxs-lookup"><span data-stu-id="132d7-165">The relevant markup for that setting in the XML Drawing File Format is shown in the following code.</span></span> 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

<span data-ttu-id="132d7-166">ここでは、 **[pinx]** 要素は、**図形**要素の子である**XForm**の要素の子です。</span><span class="sxs-lookup"><span data-stu-id="132d7-166">Here, the **PinX** element is a child of the **XForm** element, which is in turn a child of the **Shape** element.</span></span> <span data-ttu-id="132d7-167">これは、図形の [**図形情報**] セクションの **[pinx]** セルが含まれている Visio シェイプ シート UI をモデル化します。</span><span class="sxs-lookup"><span data-stu-id="132d7-167">This models the Visio ShapeSheet UI, where the **PinX** cell is included in the **Shape Transform** section of a shape.</span></span> 
  
<span data-ttu-id="132d7-168">Visio 2013 ファイル形式で、ShapeSheet─ **[pinx]**、 **LinePattern**etc.─are の**セル**要素、XML 要素の 1 つの型で表される **[Geometry** ] セクションで **[moveto]** 行で、[ **X** ] セル内のすべてのセル。</span><span class="sxs-lookup"><span data-stu-id="132d7-168">In the Visio 2013 file format, all cells in the ShapeSheet─ **PinX**, **LinePattern**, an **X** cell in a **MoveTo** row in a **Geometry** section, etc.─are represented by one type of XML element, the **Cell** element.</span></span> <span data-ttu-id="132d7-169">別の**セル**要素は、[ **N** ] 属性の値によって互いから individuated します。</span><span class="sxs-lookup"><span data-stu-id="132d7-169">Different **Cell** elements are individuated from each other by the value of their **N** attribute.</span></span> <span data-ttu-id="132d7-170">したがって、上記の例は、VSDX ファイル、次のコードに示すように、シェイプ シートの **[pinx]** セルに含まれるデータが格納されます。</span><span class="sxs-lookup"><span data-stu-id="132d7-170">Thus, in the example from above, the data contained in the **PinX** cell in the ShapeSheet is stored in a VSDX file as shown in the following code.</span></span> 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

<span data-ttu-id="132d7-171">**[Pinx]** (およびその他の**LinePattern**など**lockselect] を有効**に [単一のセル] と呼ばれる、個々 の名前付きセル) の**セル**要素は、**図形**要素の直接の子です。</span><span class="sxs-lookup"><span data-stu-id="132d7-171">The **Cell** element for **PinX** (as well as other individual, named cells called "singleton cells" like **LinePattern** or **LockSelect**) is a direct child of the **Shape** element.</span></span> <span data-ttu-id="132d7-172">各図形は、1 つの **[pinx]** を持つことができますのみ、 **[pinx]** セルを含む行を表す一意の要素は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="132d7-172">No unique element is needed to represent the row that contains the **PinX** cell, as each shape can only have one **PinX**.</span></span>
  
<span data-ttu-id="132d7-173">[ **Geometry** ] セクションと同様に、表形式のデータが含まれているセクションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="132d7-173">What about sections that include tabular data, like **Geometry** sections?</span></span> <span data-ttu-id="132d7-174">それらのセクションで、セルの Visio 2013 のファイル形式のスキーマ**のセクション**を使用して、 **N**属性または**T**属性に示すように below─to を使用して識別**行**の elements─also には、データが含まれます。</span><span class="sxs-lookup"><span data-stu-id="132d7-174">For the cells in those sections, the Visio 2013 file format schema uses **Section** and **Row** elements─also distinguished by their **N** attribute or **T** attribute as shown below─to contain the data.</span></span> <span data-ttu-id="132d7-175">たとえば、前の例から同じ図形には、図面を XML スキーマでは、次のコードのような**ジオメトリの 1**セクションのデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="132d7-175">For example, the same shape from the previous example might contain data in the **Geometry 1** section that looks like the following code in the XML Drawing schema.</span></span> 
  
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

<span data-ttu-id="132d7-176">ただし、Visio 2013 ファイルに次のコードのようになります。</span><span class="sxs-lookup"><span data-stu-id="132d7-176">However, it looks like the following code in the Visio 2013 file.</span></span>
  
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

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a><span data-ttu-id="132d7-177">Visio 2013 ファイル形式で作業するための開発者向けシナリオ</span><span class="sxs-lookup"><span data-stu-id="132d7-177">Developer scenarios for working with the Visio 2013 file format</span></span>
<span data-ttu-id="132d7-178"><a name="vis15_IntroVSDX_Scenarios"> </a></span><span class="sxs-lookup"><span data-stu-id="132d7-178"></span></span>

<span data-ttu-id="132d7-179">前述したように、Visio 2013 のファイル形式は、ZIP ファイルやデータを格納する XML のようないくつかの汎用的なテクノロジを活用します。</span><span class="sxs-lookup"><span data-stu-id="132d7-179">As explained above, the Visio 2013 file format leverages several well-understood technologies like ZIP files and XML to store data.</span></span> <span data-ttu-id="132d7-180">Visio 2013 がファイル レベルでの図面を操作するには、ソリューションは、.NET Framework 名前空間と ZIP ファイルまたは XML、 [System.IO.Packaging](http://msdn.microsoft.com/en-us/library/system.io.packaging%28v=vs.110%29.aspx)や[System.Xml](http://msdn.microsoft.com/en-us/library/system.xml%28v=vs.110%29.aspx)などの操作に関連付けられたクラスを使用する場合のみ必要があります。</span><span class="sxs-lookup"><span data-stu-id="132d7-180">To manipulate a Visio 2013 drawing at the file level, a solution need only to use the .NET Framework namespaces and classes associated with working with ZIP files or XML, like [System.IO.Packaging](http://msdn.microsoft.com/en-us/library/system.io.packaging%28v=vs.110%29.aspx) or [System.Xml](http://msdn.microsoft.com/en-us/library/system.xml%28v=vs.110%29.aspx).</span></span>
  
<span data-ttu-id="132d7-181">Visio 2013 のファイル形式の開発者の主なメリットは、読み取りし、Visio クライアント アプリケーションを自動化することがなく、Visio 2013 のファイルに書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="132d7-181">The key benefit to developers of the Visio 2013 file format is that you can read and write to Visio 2013 files without automating the Visio client application.</span></span> <span data-ttu-id="132d7-182">Visio 2013 のファイル形式を操作するための開発者を検討するいくつかのシナリオは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="132d7-182">Some scenarios that you might consider as a developer for working with Visio 2013 file format include:</span></span>
  
- <span data-ttu-id="132d7-183">特定のデータの個別の Visio 2013 ファイルをチェックします。</span><span class="sxs-lookup"><span data-stu-id="132d7-183">Checking individual Visio 2013 files for specific data.</span></span> <span data-ttu-id="132d7-184">ZIP コンテナーから 1 つの項目は、ファイル全体を抽出することがなく選択的に読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="132d7-184">You can selectively read one item out of the ZIP container without having to extract the whole file.</span></span>
    
- <span data-ttu-id="132d7-185">Visio 2013 ファイルのライブラリを特定のコンテンツで更新しています。</span><span class="sxs-lookup"><span data-stu-id="132d7-185">Updating libraries of Visio 2013 files with specific content.</span></span> <span data-ttu-id="132d7-186">プログラムを使用してすべての新しいブランドのガイドラインを反映するように背景ページにロゴを変更します。</span><span class="sxs-lookup"><span data-stu-id="132d7-186">You can programmatically change the logo in all of the background pages to reflect new branding guidelines.</span></span>
    
- <span data-ttu-id="132d7-187">Visio 2013 のファイルを使用するアプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="132d7-187">Creating applications that consume Visio 2013 files.</span></span> <span data-ttu-id="132d7-188">たとえば、Visio のワークフロー図を読み取り、そのワークフローに基づいた独自のビジネス ロジックを実行し、ツールを構築できます。</span><span class="sxs-lookup"><span data-stu-id="132d7-188">For example, you can build a tool that reads a Visio workflow diagram and then executes its own business logic based upon that workflow.</span></span>
    
<span data-ttu-id="132d7-189">これらのソリューションは標準の .NET Framework アセンブリを使用するため、クライアント コンピューター上で実行できるソリューションの大半をサーバーでも実行することができます。</span><span class="sxs-lookup"><span data-stu-id="132d7-189">Be aware that because these solutions use standard .NET Framework assemblies, most solutions that can be run on a client machine can also be run on a server!</span></span>
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a><span data-ttu-id="132d7-190">プログラムを使用して Visio 2013 ファイル形式を探索する</span><span class="sxs-lookup"><span data-stu-id="132d7-190">Exploring the Visio 2013 file format programmatically</span></span>
<span data-ttu-id="132d7-191"><a name="vis15_IntroVSDX_Explore"> </a></span><span class="sxs-lookup"><span data-stu-id="132d7-191"></span></span>

<span data-ttu-id="132d7-192">Visio 2013 のファイル形式を使用するあらゆる開発者のための最も基本的で根本的なタスクがパッケージとしてファイルを開くと、パッケージ内の個々 の部分へのアクセスします。</span><span class="sxs-lookup"><span data-stu-id="132d7-192">The most basic and fundamental task for any developer working with the Visio 2013 file format is opening the file as a package and then accessing individual parts within the package.</span></span> <span data-ttu-id="132d7-193">お**System.IO.Packaging.Package**を開き、パッケージとパーツを操作することを可能にする多くのクラスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="132d7-193">The **System.IO.Packaging.Package** in the WindowsBase.dll contains many classes that enable you to open and manipulate packages and parts.</span></span> 
  
<span data-ttu-id="132d7-194">次のコード サンプルでは、.vsdx ファイルを開いて、パッケージ内のパーツのリストを読み取り、各パーツに関する情報を取得する方法を確認できます。</span><span class="sxs-lookup"><span data-stu-id="132d7-194">In the following code sample, you can see how to open a .vsdx file, read the list of parts in the package, and get information about each part.</span></span>
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a><span data-ttu-id="132d7-195">.vsdx ファイルを開いて文書パーツを表示するには</span><span class="sxs-lookup"><span data-stu-id="132d7-195">To open a .vsdx file and view the document parts</span></span>

1. <span data-ttu-id="132d7-196">Visio 2013 を開き、新しいドキュメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="132d7-196">Open Visio 2013 and create a new document.</span></span>
    
2. <span data-ttu-id="132d7-197">新しい文書を作成してデスクトップに保存します。</span><span class="sxs-lookup"><span data-stu-id="132d7-197">Create a new document and save it to the Desktop.</span></span>
    
3. <span data-ttu-id="132d7-198">Visual Studio 2012 を開きます。</span><span class="sxs-lookup"><span data-stu-id="132d7-198">Open Visual Studio 2012.</span></span>
    
4. <span data-ttu-id="132d7-199">[**ファイル**] メニューの [**新規**作成] を選択し、[* * プロジェクト * *。</span><span class="sxs-lookup"><span data-stu-id="132d7-199">On the **File** menu, choose **New**, and then choose ** Project **.</span></span>
    
5. <span data-ttu-id="132d7-200">[**Visual C#**] または [**Visual Basic**] で、[**Windows**] を展開して、[**コンソール アプリケーション**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="132d7-200">Under **Visual C#** or **Visual Basic**, expand **Windows**, and then select **Console Application**.</span></span>
    
6. <span data-ttu-id="132d7-201">**[名前**] ボックスで、'VisioFileExplorer' を入力します。</span><span class="sxs-lookup"><span data-stu-id="132d7-201">In the **Name** box, type 'VisioFileExplorer'.</span></span> <span data-ttu-id="132d7-202">コンソール アプリケーション プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="132d7-202">The Console Application project opens.</span></span> 
    
7. <span data-ttu-id="132d7-203">[**ソリューション エクスプローラー**] で、[**VisioFileExplorer**] を右クリックして、[**参照の追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="132d7-203">In the **Solution Explorer**, right-click **VisioFileExplorer**, and then click **Add Reference**.</span></span> 
    
8. <span data-ttu-id="132d7-204">[**参照の追加**] ダイアログ ボックスで、[**アセンブリ**] の [**フレームワーク**] を展開して [**WindowsBase**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="132d7-204">In the **Add Reference** dialog box, under **Assemblies**, expand **Framework**, and then choose **WindowsBase**.</span></span>
    
9. <span data-ttu-id="132d7-205">次のコードをソリューションに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="132d7-205">Paste the following code into the solution.</span></span>
    
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

10. <span data-ttu-id="132d7-p126">F5 キーを押してソリューションをデバッグします。プログラムの実行が完了したら、任意のキーを押して終了します。</span><span class="sxs-lookup"><span data-stu-id="132d7-p126">Press F5 to debug the solution. When the program has completed running, press any key to exit.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="132d7-208">関連項目</span><span class="sxs-lookup"><span data-stu-id="132d7-208">See also</span></span>
<span data-ttu-id="132d7-209"><a name="vis15_IntroVSDX_Resources"> </a></span><span class="sxs-lookup"><span data-stu-id="132d7-209"></span></span>

<span data-ttu-id="132d7-210">Visio 2013 のファイル形式、開いているパッケージ化規則、または Office OpenXML ファイルの 2013or をプログラムから操作する方法の詳細については、次のリソースを参照してください。</span><span class="sxs-lookup"><span data-stu-id="132d7-210">For more information about the Visio 2013 file format, the Open Packaging Convention, or how to work with Visio 2013or Office OpenXML files programmatically, see the following resources:</span></span>
  
- [<span data-ttu-id="132d7-211">開発者は、Visio</span><span class="sxs-lookup"><span data-stu-id="132d7-211">Visio for developers</span></span>](http://msdn.microsoft.com/en-us/office/aa905478.aspx)
    
- <span data-ttu-id="132d7-212">[OPC: データをパッケージ化するための新しい標準](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx)。</span><span class="sxs-lookup"><span data-stu-id="132d7-212">[OPC: A New Standard for Packaging Your Data](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx).</span></span>
    
- [<span data-ttu-id="132d7-213">オープンなパッケージング規則の基礎</span><span class="sxs-lookup"><span data-stu-id="132d7-213">Essentials of the Open Packaging Conventions</span></span>](http://msdn.microsoft.com/en-us/library/ee361919.aspx)
    
- [<span data-ttu-id="132d7-214">Office (2007) オープン XML ファイル形式の概要</span><span class="sxs-lookup"><span data-stu-id="132d7-214">Introducing the Office (2007) Open XML File Formats</span></span>](http://msdn.microsoft.com/en-us/library/aa338205.aspx)
    

