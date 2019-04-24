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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357275"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a><span data-ttu-id="2f4a7-103">Visio ファイル形式 (.vsdx) の概要</span><span class="sxs-lookup"><span data-stu-id="2f4a7-103">Introduction to the Visio file format (.vsdx)</span></span>

<span data-ttu-id="2f4a7-104">Visio 2013 の新しいファイル形式について説明し、プログラムを使用して Visio 2013 ファイル形式で作業するための上位レベルの概念を確認し、Visio 2013 ファイルを検証する簡単なコンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-104">Learn about the new file format in Visio 2013, explore some high-level concepts for working with the Visio 2013 file format programmatically, and create a simple console application that examines a Visio 2013 file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2f4a7-105">**この記事の内容**         [概要](#vis15_IntroVSDX_Intro)          [Visio 2013 ファイル形式の "中身" について](#vis15_IntroVSDX_What)</span><span class="sxs-lookup"><span data-stu-id="2f4a7-105">**In this article**         [Introduction](#vis15_IntroVSDX_Intro)          [What is the Visio 2013 file format "under the hood"?](#vis15_IntroVSDX_What)</span></span>          <span data-ttu-id="2f4a7-106">[開発者が Visio 2013 ファイル形式で作業するためのシナリオ](#vis15_IntroVSDX_Scenarios)          [プログラムを使用した Visio 2013 ファイル形式の参照](#vis15_IntroVSDX_Explore)          [その他のリソース](#vis15_IntroVSDX_Resources)</span><span class="sxs-lookup"><span data-stu-id="2f4a7-106">[Developer scenarios for working with the Visio 2013 file format](#vis15_IntroVSDX_Scenarios)          [Exploring the Visio 2013 file format programmatically](#vis15_IntroVSDX_Explore)          [Additional resources](#vis15_IntroVSDX_Resources)</span></span>||
   
## <a name="introduction"></a><span data-ttu-id="2f4a7-107">概要</span><span class="sxs-lookup"><span data-stu-id="2f4a7-107">Introduction</span></span>
<span data-ttu-id="2f4a7-108"><a name="vis15_IntroVSDX_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="2f4a7-108"></span></span>

<span data-ttu-id="2f4a7-109">Visio 2013 では、Visio の新しいファイル形式 (.vsdx) が導入されています。これは、Visio のバイナリ ファイル形式 (.vsd) と Visio XML 図面ファイル形式 (.vdx) に代わるものです。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-109">Visio 2013 introduces a new file format (.vsdx) for Visio that replaces the Visio binary file format (.vsd) and Visio XML Drawing file format (.vdx).</span></span> <span data-ttu-id="2f4a7-110">Visio 2013 のファイル形式は Open Packaging Conventions と XML に基づいているため、これらのテクノロジについて詳しい知識のある開発者であれば、プログラムを使用して Visio 2013 のファイル形式で作業する方法にすぐ慣れていただくことができます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-110">Because the Visio 2013 file format is based upon Open Packaging Conventions and XML, developers who are familiar with these technologies can quickly learn how to work with Visio 2013 files programmatically.</span></span> <span data-ttu-id="2f4a7-111">Visio の以前のバージョンの Visio XML 図面ファイル形式 (.vdx) について詳しい知識のある開発者の方は、.vsdx ファイル形式の一部に同じ XML 構造が数多く使用されていることに気づかれることでしょう。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-111">Developers who are familiar with the Visio XML Drawing file format (.vdx) from previous versions of Visio can find many of the same XML structures within the parts of .vsdx file format.</span></span> <span data-ttu-id="2f4a7-112">サード パーティ製のソフトウェアでは、Visio ファイルをファイル形式レベルで操作できるため、Visio ファイルとの相互運用性が大幅に向上します。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-112">Interoperability with Visio files is greatly increased since third-party software can manipulate Visio files at a file format level.</span></span> <span data-ttu-id="2f4a7-113">Visio 2013 のファイル形式は、Microsoft SharePoint Server 2013 の Visio Services でサポートされています。SharePoint Server に発行するための "中間" ファイル形式は不要です。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-113">The Visio 2013 file format is supported on Visio Services in Microsoft SharePoint Server 2013, without the need of an "intermediary" file format for publishing to SharePoint Server.</span></span>
  
<span data-ttu-id="2f4a7-114">Visio 2013 ファイル形式を構成するファイルの種類 (拡張子) は複数あります。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-114">There are several file types, by extension, that comprise the Visio 2013 file format.</span></span> <span data-ttu-id="2f4a7-115">拡張子は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-115">These extensions include:</span></span>
  
- <span data-ttu-id="2f4a7-116">.vsdx (Visio 図面)</span><span class="sxs-lookup"><span data-stu-id="2f4a7-116">.vsdx (Visio drawing)</span></span>
    
- <span data-ttu-id="2f4a7-117">.vsdm (Visio マクロ対応図面)</span><span class="sxs-lookup"><span data-stu-id="2f4a7-117">.vsdm (Visio macro-enabled drawing)</span></span>
    
- <span data-ttu-id="2f4a7-118">.vssx (Visio ステンシル)</span><span class="sxs-lookup"><span data-stu-id="2f4a7-118">.vssx (Visio stencil)</span></span>
    
- <span data-ttu-id="2f4a7-119">.vssm (Visio マクロ対応ステンシル)</span><span class="sxs-lookup"><span data-stu-id="2f4a7-119">.vssm (Visio macro-enabled stencil)</span></span>
    
- <span data-ttu-id="2f4a7-120">.vstx (Visio テンプレート)</span><span class="sxs-lookup"><span data-stu-id="2f4a7-120">.vstx (Visio template)</span></span>
    
- <span data-ttu-id="2f4a7-121">.vstm (Visio マクロ対応テンプレート)</span><span class="sxs-lookup"><span data-stu-id="2f4a7-121">.vstm (Visio macro-enabled template)</span></span>
    
> [!NOTE]
> <span data-ttu-id="2f4a7-p104">マクロ対応ファイル (.vsdm、.vssm、.vstm) でのみ VBA マクロを保存できます。マクロを .vsdx、.vssx、または .vstx 拡張子のファイルで保存することはできません。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-p104">Only the macro-enabled files (.vsdm, .vssm, .vstm) can store VBA macros. You cannot store macros in files with a .vsdx, .vssx, or .vstx extension.</span></span> 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a><span data-ttu-id="2f4a7-124">Visio 2013 ファイル形式の "中身" について</span><span class="sxs-lookup"><span data-stu-id="2f4a7-124">What is the Visio 2013 file format "under the hood"?</span></span>
<span data-ttu-id="2f4a7-125"><a name="vis15_IntroVSDX_What"> </a></span><span class="sxs-lookup"><span data-stu-id="2f4a7-125"></span></span>

<span data-ttu-id="2f4a7-126">Visio 2013 のファイル形式では、Open Packaging Conventions (OPC) が使用されています。OPC とは、関連するリソースと共に、アプリケーション データを ZIP ファイルなどのコンテナーを使用して格納するための構造化された手法を定義するものです。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-126">The Visio 2013 file format uses the Open Packing Conventions (OPC), which defines a structured means to store application data together with related resources using a container of some sort─for example, a ZIP file.</span></span> <span data-ttu-id="2f4a7-127">基本的なレベルでは、Visio 2013 のファイルは実際のところ、他の種類のファイルを含む ZIP コンテナーです。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-127">At a basic level, a Visio 2013 file is really a ZIP container that contains other types of files.</span></span> <span data-ttu-id="2f4a7-128">Visio 2013 で図面を .vsdx ファイルとして保存し、Windows エクスプローラーでファイル拡張子を "\*.zip" に変更すると、そのファイルをフォルダーのように開いて内部のコンテンツを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-128">In fact, you can save a drawing in Visio 2013 as a .vsdx file, rename the file extension to "\*.zip" in Windows Explorer, and then open the file like a folder to see the contents inside.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="2f4a7-129">Open Packaging Conventions については、この記事では簡単なご紹介のみとなります。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-129">This article contains only a brief overview of the Open Packaging Conventions.</span></span> <span data-ttu-id="2f4a7-130">規則の詳細な範囲については、他の記事でご紹介しています。Open Packaging Conventions 自体の詳細については、[OPC: データのパッケージ化のための新しい標準](https://msdn.microsoft.com/magazine/cc163372.aspx)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-130">You can find more detailed coverage of the conventions in other articles: >  For more information about the Open Packaging Conventions themselves, see [OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span> <span data-ttu-id="2f4a7-131">Open Packaging Conventions と、Microsoft Office ファイルでのそれらの使用に関する詳細については、[Open Packaging Conventions の基本](https://msdn.microsoft.com/library/ee361919.aspx)と [Office (2007) Open XML ファイル形式の概要](https://msdn.microsoft.com/library/aa338205.aspx)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-131">>  For more information about the Open Packaging Conventions and their use in Microsoft Office files, see [Essentials of the Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx) and [Introducing the Office (2007) Open XML File Formats](https://msdn.microsoft.com/library/aa338205.aspx).</span></span> 
  
### <a name="packages-and-package-parts"></a><span data-ttu-id="2f4a7-132">パッケージとパッケージ パーツ</span><span class="sxs-lookup"><span data-stu-id="2f4a7-132">Packages and Package Parts</span></span>

<span data-ttu-id="2f4a7-133">上述のとおり、Visio 2013 ファイルは ZIP コンテナー、つまり "パッケージ" であり、それらには他のファイル ("パッケージ パーツ") が格納されています。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-133">As started earlier, Visio 2013 files are ZIP containers or "packages" that hold other files (called "package parts") within them.</span></span> <span data-ttu-id="2f4a7-134">XML ファイル、画像、そして VBA ソリューションさえも、パッケージ パーツとして使用することができます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-134">A package part can be an XML file, an image, even a VBA solution.</span></span> <span data-ttu-id="2f4a7-135">パッケージ内のパーツはさらに 2 つの大きなカテゴリ、"文書パーツ" と "リレーションシップ パーツ" に分類することができます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-135">The parts within the package can be further divided into two broad categories, "document parts" and "relationship parts."</span></span> <span data-ttu-id="2f4a7-136">文書パーツには、Visio ファイルの実際のコンテンツとメタデータが含まれます。たとえば、ファイル名、最初のページとそのページに含まれるすべての図形、そして図形のデータ接続などです。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-136">The document parts contain the actual content and metadata of the Visio file, like the name of the file, the first page and all of the shapes that it contains, and even the data connections for the shapes.</span></span> <span data-ttu-id="2f4a7-137">パッケージ内の画像とテキスト ファイルは、文書パーツとしてみなされます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-137">Images and text files within the package are considered document parts.</span></span> <span data-ttu-id="2f4a7-138">リレーションシップ パーツについては、この記事の後半で詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-138">Relationship parts are described in more detail later in this article.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2f4a7-139">ZIP ユーティリティを使用して Visio 2013 のファイルを開くと、多くの場合、その ZIP パッケージに複数のフォルダーが含まれていることが確認できます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-139">If you open a Visio 2013 file using a ZIP utility, you can probably see several folders contained inside of the ZIP package.</span></span> <span data-ttu-id="2f4a7-140">ZIP ユーティリティを使用すれば、これらのサブアドレスをフォルダーのように操作することができます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-140">You can even manipulate these sub-addresses like folders using a ZIP utility.</span></span> <span data-ttu-id="2f4a7-141">ただし、これらの "フォルダー" は ZIP パッケージ内のサブアドレスを表すものであり、実際にはフォルダーではありません。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-141">However, these "folders" represent sub-addresses within the ZIP package, not actual folders.</span></span> <span data-ttu-id="2f4a7-142">ソリューション内でこれらのサブアドレスで作業する場合、フォルダーと同等の処理を実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-142">You cannot use the programmatic equivalents of folders to work with these sub-addresses in your solution.</span></span> 
  
<span data-ttu-id="2f4a7-p109">パッケージ パーツ (文書パーツとリレーション パーツの両方) もコンテンツの種類に関連付けられています。これらのコンテンツの種類は、MIME メディアの種類を定義する文字列です。これらのコンテンツの種類は、ファイルに含めることができる MIME の種類を指定し、調査します。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-p109">Package parts─both document parts and relationship parts─also have associated content types. These content types are strings that define a MIME media type. These content types specify and scope the kind of MIME types that can be contained in the file.</span></span>
  
### <a name="relationships"></a><span data-ttu-id="2f4a7-146">リレーションシップ</span><span class="sxs-lookup"><span data-stu-id="2f4a7-146">Relationships</span></span>

<span data-ttu-id="2f4a7-147">リレーションシップ パーツ (拡張子 "\*.rels" で終わる、"_rels" フォルダーに格納されているパーツ) は、パッケージ内のパーツの相互関係を記述し、ファイルの構成を提供します。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-147">The relationship parts (which end with the extension "\*.rels" and are stored in a "_rels" folder) describe how the parts within the package relate to each other and provide the structure of the file.</span></span> <span data-ttu-id="2f4a7-148">スタンドアロン XML ドキュメントでは、要素の親/子関係を使用して、エンティティの相互関係を決定します。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-148">A standalone XML document uses the parent/child relationship of elements to determine the relationship of entities to each other.</span></span> <span data-ttu-id="2f4a7-149">それ以外のファイルの場合、その他の階層やファイル フォルダー構造を使用して、ファイル内のコンテンツ間の相互作用を記述します。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-149">Other files may use other hierarchies or file folder structure to describe the interaction of content in the file.</span></span> <span data-ttu-id="2f4a7-150">Visio 2013 のファイル形式のパッケージは、そのパッケージに正しいパーツのセットが含まれており、かつパーツ間のリレーションシップが含まれていれば、有効な Visio ファイルになります。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-150">For the Visio 2013 file format, the package is a valid Visio file if it contains the correct set of parts and the package contains the relationships between the parts.</span></span> 
  
<span data-ttu-id="2f4a7-p111">リレーションシップ パーツは XML ドキュメントであり、パッケージ内の異なる文書パーツ間の関係を説明します。これは次の2 つのアイテム間の関係を定義します。指定されたソース (リレーションシップ ファイルの名前と場所により定義) および指定されたターゲット文書パーツ。例えば、リレーションシップ パーツは、ファイルに関連付けられたマスター シェイプ、ページとファイルおよびページ同士を互いに関連付ける方法、および画像とオブジェクトを特定のページに関連付ける方法を示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-p111">Relationship parts are XML documents that describe the relationships between different document parts within the package. They define an association between two items: a specified source (defined by the name and location of the relationship file) and a specified target document part. For example, relationship parts are used to describe which shape masters are associated with the file, how pages relate to the file and to each other, or how images and objects relate to a specific page.</span></span> 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a><span data-ttu-id="2f4a7-154">Visio VDX スキーマとの類似点と相違点</span><span class="sxs-lookup"><span data-stu-id="2f4a7-154">Similarities and differences with Visio VDX schema</span></span>

<span data-ttu-id="2f4a7-155">前述のように、過去のバージョンの Visio には、XML ベースのファイル形式である Visio XML 図面形式 (.vdx) が含まれていました </span><span class="sxs-lookup"><span data-stu-id="2f4a7-155">As mentioned, past versions of Visio also included an XML-based file format, the Visio XML Drawing Format or .vdx.</span></span> <span data-ttu-id="2f4a7-156">(過去のバージョンの Visio で、Visio XML 図面形式に使用されていたスキーマは、DatadiagramML と呼ばれています)。Visio の XML スキーマの一部は、2 つのファイル形式間では同じままです。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-156">(In previous versions of Visio, the schema used for the Visio XML Drawing Format is called DatadiagramML.) Some pieces from the Visio XML schema have stayed the same between the two file formats.</span></span> <span data-ttu-id="2f4a7-157">たとえば、**Windows** 要素とその子要素については、**Windows** 要素が現在 XML ドキュメント (window.xml) のルート要素であるという点を除き、変更はありません。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-157">For example, the **Windows** element and its children remain unchanged─with the exception that the **Windows** element is now a root element of an XML document (window.xml).</span></span> 
  
<span data-ttu-id="2f4a7-158">XML 図面形式と Visio 2013 のファイル形式の最大の相違点は、パッケージです。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-158">The largest difference between the XML Drawing Format and the Visio 2013 file format is the packaging.</span></span> <span data-ttu-id="2f4a7-159">XML 図面形式は、通常のスタンドアロン XML と同じように操作することができます。Visio 2013 のファイル形式は、パッケージとして操作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-159">An XML Drawing Format file could be manipulated like a normal stand-alone XML; the Visio 2013 file format must be manipulated as a package.</span></span> <span data-ttu-id="2f4a7-160">Visio 2013 では、使いやすくするために XML がパーツに分割されています。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-160">In the Visio 2013, the XML has been divided up into parts for easier consumption.</span></span> <span data-ttu-id="2f4a7-161">もう 1 つの大きな変更点として、Visio 2013 のファイル形式では、すべてのドキュメント プロパティが、OPC 標準に記述された文書パーツに格納されます (app.xml、core.xml、custom.xml)。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-161">Another noticeable change is that the Visio 2013 file format stores all document properties in document parts described by the OPC standard (app.xml, core.xml, custom.xml).</span></span>
  
<span data-ttu-id="2f4a7-162">さらに、すべての Visio 開発者が認識する必要がある重大な変更点が 1 つあります。それは、**セル**、**行**、および**セクション**要素の導入です。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-162">However, there is one significant change that all Visio developers must be aware of: the introduction of the **Cell**, **Row**, and **Section** elements.</span></span> <span data-ttu-id="2f4a7-163">XML 図面ファイル形式スキーマでは、ShapeSheet 内の各行と各セルは名前付き要素で表されます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-163">In the XML Drawing File Format schema, individual rows and cells in the ShapeSheet are represented by named elements.</span></span> <span data-ttu-id="2f4a7-164">たとえば、あるドキュメントにページが 1 つ存在し、そのページには **PinX** 値が "2" (図形の回転ピンが図面の左端から 2 インチの場所にあることを意味します) である図形が含まれているとします。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-164">For example, imagine that you have a document with a single page that contains a shape with a **PinX** value of "2" (meaning that the rotation pin of the shape is 2 inches from the left edge of the drawing).</span></span> <span data-ttu-id="2f4a7-165">次のコードは、XML 図面ファイル形式でのその設定に関連するマークアップを示します。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-165">The relevant markup for that setting in the XML Drawing File Format is shown in the following code.</span></span> 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

<span data-ttu-id="2f4a7-166">ここで、**PinX** 要素は **XForm** 要素の子であり、XForm 要素はさらに **Shape** 要素の子です。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-166">Here, the **PinX** element is a child of the **XForm** element, which is in turn a child of the **Shape** element.</span></span> <span data-ttu-id="2f4a7-167">これは Visio の ShapeSheet UI をモデルにしています。ここでは、**PinX** セルが図形の **Shape Transform** セクションに含まれます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-167">This models the Visio ShapeSheet UI, where the **PinX** cell is included in the **Shape Transform** section of a shape.</span></span> 
  
<span data-ttu-id="2f4a7-168">Visio 2013 のファイル形式では、ShapeSheet 内のすべてのセル (**PinX**、**LinePattern**、**Geometry** セクション内の **MoveTo** 行内の **X** セルなど) が、1 つの種類の XML 要素、つまり **Cell** 要素で表されます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-168">In the Visio 2013 file format, all cells in the ShapeSheet─ **PinX**, **LinePattern**, an **X** cell in a **MoveTo** row in a **Geometry** section, etc.─are represented by one type of XML element, the **Cell** element.</span></span> <span data-ttu-id="2f4a7-169">異なる **Cell** 要素は、それらの **N** 属性の値によって互いに区別されます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-169">Different **Cell** elements are individuated from each other by the value of their **N** attribute.</span></span> <span data-ttu-id="2f4a7-170">そのため、上記の例の場合、ShapeSheet 内の **PinX** セルに含まれているデータは、次のコードに示すように VSDX ファイルに格納されます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-170">Thus, in the example from above, the data contained in the **PinX** cell in the ShapeSheet is stored in a VSDX file as shown in the following code.</span></span> 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

<span data-ttu-id="2f4a7-171">**PinX** の **Cell** 要素 (同様に、**LinePattern** や **LockSelect**などの "シングルトン セル" と呼ばれるその他の名前付きの各セル) は、**Shape** 要素の直接の子です。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-171">The **Cell** element for **PinX** (as well as other individual, named cells called "singleton cells" like **LinePattern** or **LockSelect**) is a direct child of the **Shape** element.</span></span> <span data-ttu-id="2f4a7-172">**PinX** セルを含む行を表すための一意の要素は必要ありません。**PinX** 要素は各図形に 1 つしか存在しないためです。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-172">No unique element is needed to represent the row that contains the **PinX** cell, as each shape can only have one **PinX**.</span></span>
  
<span data-ttu-id="2f4a7-173">次に、**Geometry** セクションなど、表形式データが含まれるセクションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-173">What about sections that include tabular data, like **Geometry** sections?</span></span> <span data-ttu-id="2f4a7-174">このようなセクション内のセルの場合、Visio 2013 のファイル形式スキーマではデータの格納に **Section** と **Row** 要素が使用されます (これらの要素は以下に示すように **N** 属性や **T** 属性で識別されます)。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-174">For the cells in those sections, the Visio 2013 file format schema uses **Section** and **Row** elements─also distinguished by their **N** attribute or **T** attribute as shown below─to contain the data.</span></span> <span data-ttu-id="2f4a7-175">たとえば、前述の例で使用した図形で、**Geometry 1** セクションにデータが格納される場合、XML 図面スキーマでは次のコードのようになります。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-175">For example, the same shape from the previous example might contain data in the **Geometry 1** section that looks like the following code in the XML Drawing schema.</span></span> 
  
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

<span data-ttu-id="2f4a7-176">ただし、Visio 2013 ファイルでは次のコードのようになります。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-176">However, it looks like the following code in the Visio 2013 file.</span></span>
  
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

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a><span data-ttu-id="2f4a7-177">開発者が Visio 2013 ファイル形式で作業するためのシナリオ</span><span class="sxs-lookup"><span data-stu-id="2f4a7-177">Developer scenarios for working with the Visio 2013 file format</span></span>
<span data-ttu-id="2f4a7-178"><a name="vis15_IntroVSDX_Scenarios"> </a></span><span class="sxs-lookup"><span data-stu-id="2f4a7-178"></span></span>

<span data-ttu-id="2f4a7-179">前述のように、Visio 2013 のファイル形式では ZIP ファイルや XML などのいくつかの一般的なテクノロジを使用して、データが格納されます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-179">As explained above, the Visio 2013 file format leverages several well-understood technologies like ZIP files and XML to store data.</span></span> <span data-ttu-id="2f4a7-180">Visio 2013 図面をファイル レベルで操作する場合、ソリューションに必要なのは、ZIP ファイルや XML での作業に関連付けられた .NET Framework の名前空間とクラス ([System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) や [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx) など) を使用することだけです。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-180">To manipulate a Visio 2013 drawing at the file level, a solution need only to use the .NET Framework namespaces and classes associated with working with ZIP files or XML, like [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) or [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).</span></span>
  
<span data-ttu-id="2f4a7-181">Visio 2013 ファイル形式の開発者にとっての主なメリットは、Visio のクライアント アプリケーションを自動化することなく、Visio 2013 ファイルの読み取りと書き込みができるという点です。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-181">The key benefit to developers of the Visio 2013 file format is that you can read and write to Visio 2013 files without automating the Visio client application.</span></span> <span data-ttu-id="2f4a7-182">開発者が Visio 2013 ファイル形式で作業するシナリオには、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-182">Some scenarios that you might consider as a developer for working with Visio 2013 file format include:</span></span>
  
- <span data-ttu-id="2f4a7-183">個々の Visio 2013 ファイル内の特定のデータをチェックする。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-183">Checking individual Visio 2013 files for specific data.</span></span> <span data-ttu-id="2f4a7-184">ファイル全体を抽出することなく、ZIP コンテナーから 1 つのアイテムを選択して読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-184">You can selectively read one item out of the ZIP container without having to extract the whole file.</span></span>
    
- <span data-ttu-id="2f4a7-185">Visio 2013 ファイルのライブラリを特定のコンテンツで更新する。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-185">Updating libraries of Visio 2013 files with specific content.</span></span> <span data-ttu-id="2f4a7-186">プログラムを使用してすべての背景ページのロゴを変更し、新しいブランド ガイドラインを反映させることができます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-186">You can programmatically change the logo in all of the background pages to reflect new branding guidelines.</span></span>
    
- <span data-ttu-id="2f4a7-187">Visio 2013 ファイルを使用するアプリケーションを作成する。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-187">Creating applications that consume Visio 2013 files.</span></span> <span data-ttu-id="2f4a7-188">たとえば、Visio ワークフロー図を読み取り、そのワークフローを基にした独自のビジネス ロジックを実行するツールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-188">For example, you can build a tool that reads a Visio workflow diagram and then executes its own business logic based upon that workflow.</span></span>
    
<span data-ttu-id="2f4a7-189">これらのソリューションは標準の .NET Framework アセンブリを使用するため、クライアント コンピューター上で実行できるソリューションの大半をサーバーでも実行することができます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-189">Be aware that because these solutions use standard .NET Framework assemblies, most solutions that can be run on a client machine can also be run on a server!</span></span>
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a><span data-ttu-id="2f4a7-190">プログラムを使用した Visio 2013 ファイル形式の参照</span><span class="sxs-lookup"><span data-stu-id="2f4a7-190">Exploring the Visio 2013 file format programmatically</span></span>
<span data-ttu-id="2f4a7-191"><a name="vis15_IntroVSDX_Explore"> </a></span><span class="sxs-lookup"><span data-stu-id="2f4a7-191"></span></span>

<span data-ttu-id="2f4a7-192">Visio 2013 ファイル形式で作業する開発者にとって最も基本的で重要なのは、ファイルをパッケージとして開き、パッケージ内の個々のパーツにアクセスするという作業です。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-192">The most basic and fundamental task for any developer working with the Visio 2013 file format is opening the file as a package and then accessing individual parts within the package.</span></span> <span data-ttu-id="2f4a7-193">WindowsBase.dll 内の **System.IO.Packaging.Package** には、パッケージとパーツを開いて操作できるようにするクラスが多く含まれています。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-193">The **System.IO.Packaging.Package** in the WindowsBase.dll contains many classes that enable you to open and manipulate packages and parts.</span></span> 
  
<span data-ttu-id="2f4a7-194">次のコード サンプルでは、.vsdx ファイルを開いて、パッケージ内のパーツのリストを読み取り、各パーツに関する情報を取得する方法を確認できます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-194">In the following code sample, you can see how to open a .vsdx file, read the list of parts in the package, and get information about each part.</span></span>
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a><span data-ttu-id="2f4a7-195">.vsdx ファイルを開いて文書パーツを表示するには</span><span class="sxs-lookup"><span data-stu-id="2f4a7-195">To open a .vsdx file and view the document parts</span></span>

1. <span data-ttu-id="2f4a7-196">Visio 2013 を開き、新規ドキュメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-196">Open Visio 2013 and create a new document.</span></span>
    
2. <span data-ttu-id="2f4a7-197">作成した新しいドキュメントをデスクトップに保存します。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-197">Create a new document and save it to the Desktop.</span></span>
    
3. <span data-ttu-id="2f4a7-198">Visual Studio 2012 を開きます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-198">Open Visual Studio 2012.</span></span>
    
4. <span data-ttu-id="2f4a7-199">[**ファイル**] メニューで [**新規作成**] を選択し、[プロジェクト] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-199">On the **File** menu, choose **New**, and then choose \*\* Project \*\*.</span></span>
    
5. <span data-ttu-id="2f4a7-200">[**Visual C#**] または [**Visual Basic**] の下で [**Windows**] を展開し、[**コンソール アプリケーション**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-200">Under **Visual C#** or **Visual Basic**, expand **Windows**, and then select **Console Application**.</span></span>
    
6. <span data-ttu-id="2f4a7-201">[**名前**] ボックスに、「VisioFileExplorer」と入力します。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-201">In the **Name** box, type 'VisioFileExplorer'.</span></span> <span data-ttu-id="2f4a7-202">コンソール アプリケーション プロジェクトが開きます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-202">The Console Application project opens.</span></span> 
    
7. <span data-ttu-id="2f4a7-203">[**ソリューション エクスプローラー**] で [**VisioFileExplorer**] を右クリックし、[**参照の追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-203">In the **Solution Explorer**, right-click **VisioFileExplorer**, and then click **Add Reference**.</span></span> 
    
8. <span data-ttu-id="2f4a7-204">[**参照の追加**] ダイアログ ボックスの [**アセンブリ**] の下で、[**フレームワーク**] を展開し、[**WindowsBase**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-204">In the **Add Reference** dialog box, under **Assemblies**, expand **Framework**, and then choose **WindowsBase**.</span></span>
    
9. <span data-ttu-id="2f4a7-205">次のコードをソリューションに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-205">Paste the following code into the solution.</span></span>
    
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

10. <span data-ttu-id="2f4a7-p126">F5 キーを押してソリューションをデバッグします。プログラムの実行が完了したら、任意のキーを押して終了します。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-p126">Press F5 to debug the solution. When the program has completed running, press any key to exit.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2f4a7-208">関連項目</span><span class="sxs-lookup"><span data-stu-id="2f4a7-208">See also</span></span>
<span data-ttu-id="2f4a7-209"><a name="vis15_IntroVSDX_Resources"> </a></span><span class="sxs-lookup"><span data-stu-id="2f4a7-209"></span></span>

<span data-ttu-id="2f4a7-210">Visio 2013 ファイル形式、Open Packaging Conventions、プログラムを使用して Visio 2013 や Office OpenXML ファイルで作業する方法の詳細については、次のリソースを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f4a7-210">For more information about the Visio 2013 file format, the Open Packaging Convention, or how to work with Visio 2013or Office OpenXML files programmatically, see the following resources:</span></span>
  
- [<span data-ttu-id="2f4a7-211">開発者向けの Visio 情報</span><span class="sxs-lookup"><span data-stu-id="2f4a7-211">Visio for developers</span></span>](https://msdn.microsoft.com/office/aa905478.aspx)
    
- <span data-ttu-id="2f4a7-212">[OPC: データのパッケージ化のための新しい標準](https://msdn.microsoft.com/magazine/cc163372.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f4a7-212">[OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span>
    
- [<span data-ttu-id="2f4a7-213">Open Packaging Conventions の基本</span><span class="sxs-lookup"><span data-stu-id="2f4a7-213">Essentials of the Open Packaging Conventions</span></span>](https://msdn.microsoft.com/library/ee361919.aspx)
    
- [<span data-ttu-id="2f4a7-214">Office (2007) Open XML ファイル形式の概要</span><span class="sxs-lookup"><span data-stu-id="2f4a7-214">Introducing the Office (2007) Open XML File Formats</span></span>](https://msdn.microsoft.com/library/aa338205.aspx)
    

