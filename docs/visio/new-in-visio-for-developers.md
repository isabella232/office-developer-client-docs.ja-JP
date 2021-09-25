---
title: 開発者向け Visio の新機能
manager: soliver
ms.date: 09/18/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 7e3fb858-0ab8-bd2e-217c-c85b10d79785
description: このドキュメントでは、2013 年の開発者向けの機能強化と追加のVisioします。 Visio プラットフォームでジャンプ スタートを開始する準備ができている開発者向けには、Visio 2013 に対してコーディングを開始するための十分な詳細が提供されます。
ms.openlocfilehash: 8e55927926c5aa43d0ac879037a5dfeae160b0f5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608208"
---
# <a name="new-in-visio-for-developers"></a>開発者向け Visio の新機能

このドキュメントでは、2013 年の開発者向けの機能強化と追加のVisioします。 Visio プラットフォームでジャンプ スタートを開始する準備ができている開発者向けには、Visio 2013 に対してコーディングを開始するための十分な詳細が提供されます。
  
## <a name="introduction"></a>はじめに
<a name="vis15_WhatsNew_Intro"> </a>

Visio 2013 は、カスタム図面ソリューションに強力な単一プラットフォームを提供します。 新しいオブジェクト、コレクション、プロパティ、メソッド、列挙、およびイベントが追加されるとともに、新しいシェイプシート セルおよび関数が提供され、ソリューションで要素の動作を定義する際の選択肢が広がりました。
  
2013 年 2013 年の開発者Visio新しい機能の中には、新しいファイル形式があります。テーマの堅牢な更新。図形の機能を変更する (図形を別の図形に置き換える)新しい図形効果。コメントの改善。サーバー 2013 SharePoint共同編集。カスタマイズ可能な画像クリッピング。相対ジオメトリ。Business Connectivity (BCS) データのサポート。2013 Visioの Microsoft SharePoint Server サービスの更新。ページ機能が重複しています。 ここでは、これらの各機能について簡単に説明し、これらの機能に関連付けられて、Visual Basic for Applications (VBA) に公開されている Visio の新しいオブジェクトやメンバーの一部を紹介します。 これらの機能と付随するコード サンプルの詳細については、「開発者センター」[を参照Visioしてください](https://msdn.microsoft.com/office/aa905478.aspx)。
  
> [!NOTE]
> Visio 2013 には、新しい ShapeSheet セル、行、および関数が多数含まれています。このページでは、新しい機能をサポートVisio。 Visio 2013 の ShapeSheet の新機能の詳細については[、「What's new](what-s-new-for-visio-shapesheet-developers.md)for Visio ShapeSheet 開発者向け」を参照してください。 
  
## <a name="new-file-format"></a>新しいファイル形式
<a name="vis15_WhatsNew_NewFF"> </a>

Visio 2013 で導入された新しいファイル形式は、Open Packaging Conventions (OPC) 標準 (ISO 29500、パート 2) と、以前の Visio XML ファイル形式 (.vdx) の XML 要素が基になっています。 zip された、この XML ベースのファイル形式は、他の アプリケーションで使用されるファイル形式に似ています。
  
新しいファイル形式は Microsoft SharePoint Server 2013 の Visio 2013 と Visio Services の両方でサポートされていますので、Visio Web 図面 (.vdw) としてファイルを発行することなく、Visio 図面を SharePoint Server ライブラリに直接保存できます。 このような場合でも、Visio Services は、Visio Web 図面ファイルの読み込みと表示が可能です。
  
この新しいファイル形式には、次のファイルの種類 (拡張子で区別する) が含まれます。
  
- .vsdx (Visio 図面)
    
- .vsdm (Visio マクロ対応図面)
    
- .vssx (Visio ステンシル)
    
- .vssm (Visio マクロ対応ステンシル)
    
- .vstx (Visio テンプレート)
    
- .vstm (Visio マクロ対応テンプレート)
    
ファイル形式パッケージ [(System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) など) の読み取りおよび書き込みおよび XML の解析に既存のサポートを [ 使用System.Xml。Linq)](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) を使用すると、新しいファイル形式をプログラムで操作できます。 
  
Visio 2013 では、古いファイル形式 (.vsd、.vss、.vst、.vdx、.vsx、.vtx、.vdw、.vwi) を読み取る機能が保持されます。 Visio 2013 では、XML ファイル形式 (.vdx) Visioに保存されない。 新しいファイル形式とそのスキーマを読み取Visio XML ファイル形式 (.vdx) ファイルを使用するソリューションまたはツールをリファクタリングする必要があります。
  
Visio Services では、ブラウザーで Visio Web 図面 (.vdw) 形式のファイルを表示できます。また、新しいファイル形式の Visio 図面 (.vsdx) と Visio マクロ対応図面 (.vsdm) 形式を表示できるようになりました。
  
## <a name="themes"></a>テーマ
<a name="vis15_WhatsNew_Themes"> </a>

テーマのデザインは Visio 2013 で変更され、図形とアートの効果の統合など、より多彩な効果やスタイルを使用するようになっています。 ユーザーは、テーマを適用することにより全体的なスタイルを選択したうえで、テーマのバリエーションを使用して図をカスタマイズしたり、クイック スタイルを使用して個々の図形を強調したりできます。 シェイプシートの開発者は、これらの機能と共に、シェイプシートの新しい機能およびセルを使用できます。
  
テーマの操作は、[ページ](https://msdn.microsoft.com/library/7a7f37ab-b448-eb70-b4f1-c185dfbd511e%28Office.15%29.aspx)、[図形](https://msdn.microsoft.com/library/da7a8872-4ebb-a607-e0ed-eebf68ff5630%28Office.15%29.aspx)、および[選択範囲](https://msdn.microsoft.com/library/e5734140-6dbe-7de8-9695-1a22fb4ac628%28Office.15%29.aspx)オブジェクトのレベルでも実行できます。テーマを操作するための新しい API には、[Page.SetTheme](https://msdn.microsoft.com/library/5a186f58-9a7a-bd8a-826b-85da75a4d59f%28Office.15%29.aspx) メソッド、[Page.SetThemeVariant](https://msdn.microsoft.com/library/8393a95f-83ca-0efa-d987-ae498bfe5e9d%28Office.15%29.aspx) メソッド、[Shape.SetQuickStyle](https://msdn.microsoft.com/library/aebe80cb-fae9-0be7-e903-882f6eb58b63%28Office.15%29.aspx) メソッド、および [Selection.SetQuickStyle](https://msdn.microsoft.com/library/39b810b5-0738-daed-0103-8a2df07559c6%28Office.15%29.aspx) メソッドなどがあります。 
  
2013 年 2013 年の新しい API のVisio、この記事の「Visio[オブジェクト](#vis15_WhatsNew_NewOM)モデルの変更」セクションを参照してください。 2013 年 2013 年の新しい Shape Visio Sheet セルの詳細については、「What's new for [Visio シェイプシート開発者」を参照してください](what-s-new-for-visio-shapesheet-developers.md)。
  
## <a name="change-shape"></a>図形の変更
<a name="vis15_WhatsNew_ChangeShapes"> </a>

Visio 2013 には、ステンシルに含まれる別の図形に対して 1 つ以上の図形を入れ替え、図形テキストの図形、図形データ、図形の書式設定などの元の図形のローカル値の一部を保持できる、図形置換 API が含まれています。 図形の開発者は、カスタム図形のシェイプシートの設定を更新することにより、開発した図形の図形変更動作を指定できます。 新しい API としては、[Shape.ReplaceShapes](https://msdn.microsoft.com/library/b330a63d-4e3f-0c4d-c38c-6ee806670225%28Office.15%29.aspx) メソッド、[Selection.ReplaceShapes](https://msdn.microsoft.com/library/dc278901-77ce-e1fe-c44f-f464bbb1c360%28Office.15%29.aspx) メソッド、[ReplaceShape](https://msdn.microsoft.com/library/26c4e7cb-6618-6d2f-a4be-515584f8cd10%28Office.15%29.aspx) イベントなどがあります。 
  
2013 年 2013 年の新しい API のVisio、この記事の「Visio[オブジェクト](#vis15_WhatsNew_NewOM)モデルの変更」セクションを参照してください。 2013 年 2013 年の新しい Shape Visio Sheet セルの詳細については、「What's new for [Visio シェイプシート開発者」を参照してください](what-s-new-for-visio-shapesheet-developers.md)。
  
## <a name="shape-effects"></a>図形の効果
<a name="vis15_WhatsNew_ShapeEffects"> </a>

面取り、3D 回転、光彩、反射、スケッチなどの新しい図形の効果が、Visio 2013 に追加されています。 シェイプシートには、これらの効果を操作するための新しいセルが含まれています。
  
2013 年 2013 年の新しい Shape Visio Sheet セルの詳細については、「What's new for [Visio シェイプシート開発者」を参照してください](what-s-new-for-visio-shapesheet-developers.md)。
  
## <a name="commenting"></a>コメント入力
<a name="vis15_WhatsNew_Commenting"> </a>

Visio 2013 には新しいコメント入力フレームワークが含まれます。 コメントを特定の図形やページと関連付けることができます。 Visio 2013 には、コメントとコメント という 2 つの新しい[オブジェクト](https://msdn.microsoft.com/library/f028cc03-0ef1-8017-a936-d30d45211864%28Office.15%29.aspx)が[含まれています](https://msdn.microsoft.com/library/7cd0ee53-6b8d-a03b-ecd6-f6f6dda0f2d4%28Office.15%29.aspx)。 プログラムからコメントにアクセスするための新しい API には、[Document.Comments](https://msdn.microsoft.com/library/15a322ad-70eb-1487-701d-76e2fde73309%28Office.15%29.aspx)、[Page.Comments](https://msdn.microsoft.com/library/9618c86c-96c0-be95-ee20-5d1b99f4d5e8%28Office.15%29.aspx)、[Shape.Comments](https://msdn.microsoft.com/library/498eca91-beb9-b764-0262-a935e5205710%28Office.15%29.aspx)、および [Page.ShapeComments](https://msdn.microsoft.com/library/b7d86594-ba1f-627b-222f-905da1b1201e%28Office.15%29.aspx) の各プロパティがあります。 
  
Visioサービスには、図のページまたは図形からコメントを読み取る JavaScript API が含まれています。
  
2013 年 2013 年の新しい API のVisio、この記事の「Visio[オブジェクト](#vis15_WhatsNew_NewOM)モデルの変更」セクションを参照してください。 
  
> [!NOTE]
> コメントは、シェイプシートからはアクセスできなくなりました。 
  
## <a name="coauthoring"></a>共同編集
<a name="vis15_WhatsNew_Coauthoring"> </a>

Visio 2013 には、図を作成する機能が含まれています。SharePointまたはMicrosoft OneDrive。 開発者は、共同編集による図の変更についての情報を提供する [Document.AfterDocumentMerge](https://msdn.microsoft.com/library/50658da5-592a-4d16-908f-c6abe3050f09%28Office.15%29.aspx) イベントにアクセスできます。 また、ソリューションの開発者向けに、カスタムのニーズに合わせて共同編集を無効にする機能が提供されており、文書のシェイプシートの [NoCoauth](nocoauth-cell-document-properties-section.md) セルを使用してそれを設定できます。 
  
2013 年 2013 年の新しい API のVisio、この記事の「Visio[オブジェクト](#vis15_WhatsNew_NewOM)モデルの変更」セクションを参照してください。 
  
## <a name="customizable-image-clipping"></a>カスタマイズ可能なイメージ クリップ
<a name="vis15_WhatsNew_ClipImages"> </a>

Visio 2013 は、任意の図形にトリミングされるカスタム イメージ クリップ パスの定義をサポートします。 これにより、2010 年Visioの容量が拡張され、四角形の方法でクリッピング 画像がサポートされました。 この機能は、シェイプシートの **Foreign Image Info** セクションの [ClippingPath](clippingpath-cell-foreign-image-info-section.md) のセルで使用できます。 
  
2013 年 2013 年の新しい Shape Visio Sheet セルの詳細については、「What's new for [Visio シェイプシート開発者」を参照してください](what-s-new-for-visio-shapesheet-developers.md)。
  
## <a name="relative-geometries"></a>相対ジオメトリ
<a name="vis15_WhatsNew_RelativeGeometry"> </a>

以前のバージョンのVisio図形のジオメトリは、図形の高さまたは幅に依存する数式によって定義されました。 たとえば、Visio 2010 では、多くの組み込みの Visio 図形の頂点は、図形の高さまたは幅に定数を掛けて定義されました。 これらの図形には **、MoveTo** 行や [LineTo](moveto-row-geometry-section.md)行 (たとえば) などの数式を含む Geometry セクション [](lineto-row-geometry-section.md) `Width*1` が含まれていました `Height*0` 。
  
Visio 2013 では、ShapeSheet の相対ジオメトリがサポートされます。 図形の開発者は、相対的なジオメトリを使用して、ジオメトリを単純な値または数式として指定し、高さまたは幅を自動的に乗算できます。 たとえば、頂点を図形の幅または高さの倍数として表現する必要がなされるなど、図形の頂点を定数で表現できます。 これにより、開発者は、パフォーマンスが向上し、ファイル サイズが小さくて、図形を簡単に作成できます。 新しい行には [、RelMoveTo](relmoveto-row-geometry-section.md) 行と [RelLineTo](rellineto-row-geometry-section.md) 行が含まれます。この行では **、X** セルと **Y** セルの値に図形の幅または高さが自動的に乗算されます (それぞれ)。 
  
2013 年 2013 年の新しい ShapeSheet 行の詳細については、「Visio [What's new for Visio シェイプシート開発者」を参照してください](what-s-new-for-visio-shapesheet-developers.md)。
  
## <a name="support-for-business-connectivity-services-bcs-data"></a>Business Connectivity Services (BCS) データのサポート
<a name="vis15_WhatsNew_BCS"> </a>

Visio 2013 のダイアグラムを、サーバー 2013 サーバー上のSharePointに接続できます。 外部リストは、microsoft Business Connectivity Services (BCS) を使用して SharePoint リストに接続されている SharePoint (SQL Server テーブルなど) の外部コンテンツ ソースです。 Visio Services では、データの更新プログラムとして Visio 図面を更新する機能をサポートしています。
  
Visio サービスの新機能の詳細については、「Visio [2013 SharePoint」を参照](https://msdn.microsoft.com/library/jj164027%28office.15%29.aspx)してください。 Business Connectivity サービス (BCS) の詳細については[、「Business Connectivity 2013 SharePoint」](https://msdn.microsoft.com/library/jj163782%28office.15%29.aspx)を参照してください。
  
## <a name="improvements-in-visio-services"></a>Visio サービスの改善
<a name="vis15_WhatsNew_VisioServices"> </a>

Visio2013 Microsoft SharePoint Serverサービスには、多くの改善点が含まれています。 前述したように、Visio サービスは、新しいファイル形式 (Visio .vsdx と .vsdm の両方) をサポートしています。 Visioサービスでは、データの更新と再計算が拡張され、ダイアグラム全体で数式を再計算できます。 
  
Visio サービスの新機能の詳細については、「Visio [2013 SharePoint」を参照](https://msdn.microsoft.com/library/jj164027%28office.15%29.aspx)してください。
  
## <a name="duplicate-page"></a>ページの複製
<a name="vis15_WhatsNew_DuplicatePage"> </a>

2013 年に同じドキュメント内のページとその図形Visioできます。 したがって **、Page オブジェクトには、ページ** を複製し、新しい **Page** オブジェクトを返す新しいメソッド [Duplicate](https://msdn.microsoft.com/library/394be23b-997d-0da1-b3bd-8278564fb4e0%28Office.15%29.aspx)があります。 
  
## <a name="visio-object-model-changes"></a>Visioモデルの変更点
<a name="vis15_WhatsNew_NewOM"> </a>

Visio オブジェクト モデルに新しいオブジェクト、プロパティ、メソッド、イベントが追加され、2013 年の新しい Visio 機能がサポートされています。 さらに、オブジェクト モデルの改善により、開発者が頻繁に行う変更要求に対応し、Visioできます。
  
### <a name="new-members"></a>新しいメンバー

次のメンバーが、オブジェクト モデル内の既存のVisio追加されています。
  
 **表 1. Visio オブジェクト モデルの機能拡張**
  
|**オブジェクトまたはコレクション**|**新しいメンバー**|
|:-----|:-----|
|[Application オブジェクト (Visio)](https://msdn.microsoft.com/library/5b3c8939-793f-116f-11b8-1d4170d95a63%28Office.15%29.aspx) <br/> |[Application.AfterReplaceShapes イベント (Visio)](https://msdn.microsoft.com/library/b02de031-086a-41cc-d832-5434b8096444%28Office.15%29.aspx) <br/> |
||[Application.BeforeReplaceShapes イベント (Visio)](https://msdn.microsoft.com/library/fbf44569-0539-9292-ce20-1f9e34238b33%28Office.15%29.aspx) <br/> |
||[Application.QueryCancelReplaceShapes イベント (Visio)](https://msdn.microsoft.com/library/50c0f2a6-f534-f3af-7e83-c865abda8bf9%28Office.15%29.aspx) <br/> |
||[Application.ReplaceShapesCanceled イベント (Visio)](https://msdn.microsoft.com/library/e8eecd64-e4bd-d2c4-b942-c5ff607a4121%28Office.15%29.aspx) <br/> |
|[ApplicationSettings オブジェクト (Visio)](https://msdn.microsoft.com/library/f2e24211-ecc6-e0f5-4c00-fc50f98a3505%28Office.15%29.aspx) <br/> |[ApplicationSettings.EnterCommitsText プロパティ (Visio)](https://msdn.microsoft.com/library/ba9ce9fa-d224-cdc3-668d-46c1849911c7%28Office.15%29.aspx) <br/> |
||[ApplicationSettings.SVGExportFormat プロパティ (Visio)](https://msdn.microsoft.com/library/9e7ca1cb-5ace-b75b-0e59-61566b9a0169%28Office.15%29.aspx) <br/> |
|[Document オブジェクト (Visio)](https://msdn.microsoft.com/library/21640062-13a2-a2b2-7c61-7e707671207c%28Office.15%29.aspx) <br/> |[Document.AfterDocumentMerge イベント (Visio)](https://msdn.microsoft.com/library/50658da5-592a-4d16-908f-c6abe3050f09%28Office.15%29.aspx) <br/> |
||[Document.Comments プロパティ (Visio)](https://msdn.microsoft.com/library/15a322ad-70eb-1487-701d-76e2fde73309%28Office.15%29.aspx) <br/> |
||[Document.CompatibilityMode プロパティ (Visio)](https://msdn.microsoft.com/library/98fc00d3-5d2b-218e-9828-b5581ee7313d%28Office.15%29.aspx) <br/> |
|[Documents オブジェクト (Visio)](https://msdn.microsoft.com/library/e9291149-964e-c6fb-4c62-bf2f35a6a0a7%28Office.15%29.aspx) <br/> |[Documents.AfterDocumentMerge イベント (Visio)](https://msdn.microsoft.com/library/cac0544d-77b9-b722-cfdb-e42475ce2558%28Office.15%29.aspx) <br/> |
||[Documents.AfterReplaceShapes イベント (Visio)](https://msdn.microsoft.com/library/e01c069e-440b-7b8b-8d7d-cdb664f6e2d6%28Office.15%29.aspx) <br/> |
||[Documents.BeforeReplaceShapes イベント (Visio)](https://msdn.microsoft.com/library/55a66c47-a2ca-5c8a-2693-aaa1b079c704%28Office.15%29.aspx) <br/> |
||[Documents.QueryCancelReplaceShapes イベント (Visio)](https://msdn.microsoft.com/library/d613730e-04c8-d17f-0ad1-19e976aa107d%28Office.15%29.aspx) <br/> |
||[Documents.ReplaceShapesCanceled イベント (Visio)](https://msdn.microsoft.com/library/94a20fe7-da09-4e3c-d048-05ba0b8f1070%28Office.15%29.aspx) <br/> |
|[InvisibleApp オブジェクト (Visio)](https://msdn.microsoft.com/library/70a30571-2017-af8b-eaa1-bf93c758a46a%28Office.15%29.aspx) <br/> |[InvisibleApp.AfterReplaceShapes イベント (Visio)](https://msdn.microsoft.com/library/5d7b8ec2-ef65-1a49-fb50-3fae95d56761%28Office.15%29.aspx) <br/> |
||[InvisibleApp.BeforeReplaceShapes イベント (Visio)](https://msdn.microsoft.com/library/bd0e37ca-887a-4d53-3b0c-3339492df3dd%28Office.15%29.aspx) <br/> |
||[InvisibleApp.QueryCancelReplaceShapes イベント (Visio)](https://msdn.microsoft.com/library/5e5d9b76-dfd4-1d02-d205-9e64350449d5%28Office.15%29.aspx) <br/> |
||[InvisibleApp.ReplaceShapesCanceled イベント (Visio)](https://msdn.microsoft.com/library/17e43497-c7a8-8546-595c-4630afb301a3%28Office.15%29.aspx) <br/> |
|[Page オブジェクト (Visio)](https://msdn.microsoft.com/library/7a7f37ab-b448-eb70-b4f1-c185dfbd511e%28Office.15%29.aspx) <br/> |[Page.AfterReplaceShapes イベント (Visio)](https://msdn.microsoft.com/library/e4005987-acb1-78d7-91fb-c3c2d5b036e3%28Office.15%29.aspx) <br/> |
||[Page.BeforeReplaceShapes イベント (Visio)](https://msdn.microsoft.com/library/57ea9836-74dd-77c2-6541-f8f61b89c0b6%28Office.15%29.aspx) <br/> |
||[Page.Comments プロパティ (Visio)](https://msdn.microsoft.com/library/9618c86c-96c0-be95-ee20-5d1b99f4d5e8%28Office.15%29.aspx) <br/> |
||[Page.Duplicate メソッド (Visio)](https://msdn.microsoft.com/library/394be23b-997d-0da1-b3bd-8278564fb4e0%28Office.15%29.aspx) <br/> |
||[Page.GetTheme メソッド (Visio)](https://msdn.microsoft.com/library/31c84e69-0bc8-2d1a-84d8-7397110d74ae%28Office.15%29.aspx) <br/> |
||[Page.GetThemeVariant メソッド (Visio)](https://msdn.microsoft.com/library/40c2be31-fdb0-68ee-a129-2788b1b17c82%28Office.15%29.aspx) <br/> |
||[Page.QueryCancelReplaceShapes イベント (Visio)](https://msdn.microsoft.com/library/17ead23f-825a-c608-3315-e2eed6784cd5%28Office.15%29.aspx) <br/> |
||[Page.ReplaceShapesCanceled イベント (Visio)](https://msdn.microsoft.com/library/867b1fc1-96bd-cbeb-fd61-b02a96e039ca%28Office.15%29.aspx) <br/> |
||[Page.SetTheme メソッド (Visio)](https://msdn.microsoft.com/library/5a186f58-9a7a-bd8a-826b-85da75a4d59f%28Office.15%29.aspx) <br/> |
||[Page.SetThemeVariant メソッド (Visio)](https://msdn.microsoft.com/library/8393a95f-83ca-0efa-d987-ae498bfe5e9d%28Office.15%29.aspx) <br/> |
||[Page.ShapeComments プロパティ (Visio)](https://msdn.microsoft.com/library/b7d86594-ba1f-627b-222f-905da1b1201e%28Office.15%29.aspx) <br/> |
|[Pages オブジェクト (Visio)](https://msdn.microsoft.com/library/45eec568-b5cc-5e80-ff5c-4dfa567efb5d%28Office.15%29.aspx) <br/> |[Pages.AfterReplaceShapes イベント (Visio)](https://msdn.microsoft.com/library/05c33bdd-e697-d36e-46a8-45705e9ad2c2%28Office.15%29.aspx) <br/> |
||[Pages.BeforeReplaceShapes イベント (Visio)](https://msdn.microsoft.com/library/3f6dbc31-0583-dd67-0432-335d6df7a50c%28Office.15%29.aspx) <br/> |
||[Pages.QueryCancelReplaceShapes イベント (Visio)](https://msdn.microsoft.com/library/d11ff976-0016-da6b-92fb-379baa7e8f94%28Office.15%29.aspx) <br/> |
||[Pages.ReplaceShapesCanceled イベント (Visio)](https://msdn.microsoft.com/library/f0ce8c66-7a15-5f91-8c89-e177bc6671d2%28Office.15%29.aspx) <br/> |
|[Selection オブジェクト (Visio)](https://msdn.microsoft.com/library/e5734140-6dbe-7de8-9695-1a22fb4ac628%28Office.15%29.aspx) <br/> |[Selection.ReplaceShape メソッド (Visio)](https://msdn.microsoft.com/library/dc278901-77ce-e1fe-c44f-f464bbb1c360%28Office.15%29.aspx) <br/> |
||[Selection.SetQuickStyle メソッド (Visio)](https://msdn.microsoft.com/library/39b810b5-0738-daed-0103-8a2df07559c6%28Office.15%29.aspx) <br/> |
|[Shape オブジェクト (Visio)](https://msdn.microsoft.com/library/da7a8872-4ebb-a607-e0ed-eebf68ff5630%28Office.15%29.aspx) <br/> |[Shape.ChangePicture メソッド (Visio)](https://msdn.microsoft.com/library/9193d802-cebd-2bfd-5f8e-400fac36c1a5%28Office.15%29.aspx) <br/> |
||[Shape.Comments プロパティ (Visio)](https://msdn.microsoft.com/library/498eca91-beb9-b764-0262-a935e5205710%28Office.15%29.aspx) <br/> |
||[Shape.ReplaceShape メソッド (Visio)](https://msdn.microsoft.com/library/b330a63d-4e3f-0c4d-c38c-6ee806670225%28Office.15%29.aspx) <br/> |
||[Shape.SetQuickStyle メソッド (Visio)](https://msdn.microsoft.com/library/aebe80cb-fae9-0be7-e903-882f6eb58b63%28Office.15%29.aspx) <br/> |
   
### <a name="new-objects-and-enumerations"></a>新しいオブジェクトと列挙

次のオブジェクトがオブジェクト モデルにVisioされました。
  
 **表 2. Visio オブジェクト モデルへの追加**
  
|**オブジェクト**|**プロパティ**|**メソッド**|
|:-----|:-----|:-----|
|[CoauthMergeEvent オブジェクト (Visio)](https://msdn.microsoft.com/library/eb9425cb-0108-4909-e334-9cd51e5b9303%28Office.15%29.aspx) <br/> |[CoauthMergeEvent.BaseDocument プロパティ (Visio)](https://msdn.microsoft.com/library/7ec09a85-6f51-685b-0c87-4b9eb3266773%28Office.15%29.aspx) <br/> [CoauthMergeEvent.DownloadDocument プロパティ (Visio)](https://msdn.microsoft.com/library/19239540-cd5a-13ea-3b26-282ac3676abd%28Office.15%29.aspx) <br/> [CoauthMergeEvent.ObjectType プロパティ (Visio)](https://msdn.microsoft.com/library/01baa0c2-75b7-2713-9732-1e7a8a7b33aa%28Office.15%29.aspx) <br/> [CoauthMergeEvent.Stat プロパティ (Visio)](https://msdn.microsoft.com/library/d8a96b8e-36b5-c61f-8cea-76266f7eed39%28Office.15%29.aspx) <br/> [CoauthMergeEvent.WorkingDocument プロパティ (Visio)](https://msdn.microsoft.com/library/0f3c4358-0d63-df7f-12fe-7f378bacca86%28Office.15%29.aspx) <br/> |なし  <br/> |
|[Comment オブジェクト (Visio)](https://msdn.microsoft.com/library/f028cc03-0ef1-8017-a936-d30d45211864%28Office.15%29.aspx) <br/> |[Comment.AssociatedObject プロパティ (Visio)](https://msdn.microsoft.com/library/e28eed2e-260e-59c9-9b24-631817fe1ae1%28Office.15%29.aspx) <br/> [Comment.AuthorInitials プロパティ (Visio)](https://msdn.microsoft.com/library/abc07100-8c5c-9982-674d-40b58c096816%28Office.15%29.aspx) <br/> [Comment.AuthorName プロパティ (Visio)](https://msdn.microsoft.com/library/e1da4db8-7a16-16bf-2a5f-be1ac5372d34%28Office.15%29.aspx) <br/> [Comment.AuthorSipAddress プロパティ (Visio)](https://msdn.microsoft.com/library/f8d185a9-91b6-471a-3c0e-ffa8a06b36b3%28Office.15%29.aspx) <br/> [Comment.AuthorSMTPAddress プロパティ (Visio)](https://msdn.microsoft.com/library/22e04ccc-c524-ca08-d5e2-db68fdb3afb6%28Office.15%29.aspx) <br/> [Comment.Collapsed プロパティ (Visio)](https://msdn.microsoft.com/library/9552e379-e351-78d7-e0ed-4f524c3273a1%28Office.15%29.aspx) <br/> [Comment.CreateDate プロパティ (Visio)](https://msdn.microsoft.com/library/b643e13e-da12-a992-3a59-99b37f003fb9%28Office.15%29.aspx) <br/> [Comment.Document プロパティ (Visio)](https://msdn.microsoft.com/library/d57b1377-b895-1fe1-2f98-ef000fdd9c39%28Office.15%29.aspx) <br/> [Comment.EditDate プロパティ (Visio)](https://msdn.microsoft.com/library/4ad13f54-215e-3680-5de6-13715e309fbf%28Office.15%29.aspx) <br/> [Comment.ObjectType プロパティ (Visio)](https://msdn.microsoft.com/library/bf0d786d-e1b6-65f1-3112-5dfd4ff324e9%28Office.15%29.aspx) <br/> [Comment.Stat プロパティ (Visio)](https://msdn.microsoft.com/library/f457598c-af42-cb83-ecd2-4fd42898ea16%28Office.15%29.aspx) <br/> [Comment.Text プロパティ (Visio)](https://msdn.microsoft.com/library/3ec63034-de5f-d9f2-16a5-e06a56883867%28Office.15%29.aspx) <br/> |[Comment.Delete メソッド (Visio)](https://msdn.microsoft.com/library/7762f264-f680-5758-7c35-dfe9067b61ca%28Office.15%29.aspx) <br/> |
|[Comments オブジェクト (Visio)](https://msdn.microsoft.com/library/7cd0ee53-6b8d-a03b-ecd6-f6f6dda0f2d4%28Office.15%29.aspx) <br/> |[Comments.Count プロパティ (Visio)](https://msdn.microsoft.com/library/abac02d5-5047-2c9d-5c5c-e2738f99a4a6%28Office.15%29.aspx) <br/> [Comments.Document プロパティ (Visio)](https://msdn.microsoft.com/library/507d4698-e282-f8a9-1299-c67945ee5fc4%28Office.15%29.aspx) <br/> [Comments.Item プロパティ (Visio)](https://msdn.microsoft.com/library/fed2a079-de87-d5ce-1d74-0bfa5a328441%28Office.15%29.aspx) <br/> [Comments.ObjectType プロパティ (Visio)](https://msdn.microsoft.com/library/06544d73-ce00-2c89-1ecb-20541b251d57%28Office.15%29.aspx) <br/> [Comments.Stat プロパティ (Visio)](https://msdn.microsoft.com/library/1f5f29b2-236c-91b6-6d25-7bacc37ca96c%28Office.15%29.aspx) <br/> |[Comments.Add メソッド (Visio)](https://msdn.microsoft.com/library/da02de49-8057-7e5c-6b59-0a013e56256d%28Office.15%29.aspx) <br/> [Comments.DeleteAll メソッド (Visio)](https://msdn.microsoft.com/library/50777ed3-553c-90ae-2d30-9dde412fe6b9%28Office.15%29.aspx) <br/> |
|[ReplaceShapesEvent オブジェクト (Visio)](https://msdn.microsoft.com/library/26c4e7cb-6618-6d2f-a4be-515584f8cd10%28Office.15%29.aspx) <br/> |[ReplaceShapesEvent.ObjectType プロパティ (Visio)](https://msdn.microsoft.com/library/bcc442f0-aa4e-cd5a-d116-f3fb74459927%28Office.15%29.aspx) <br/> [ReplaceShapesEvent.ReplaceFlags プロパティ (Visio)](https://msdn.microsoft.com/library/d0d00891-c794-bd0c-d37e-1ab98c92beab%28Office.15%29.aspx) <br/> [ReplaceShapesEvent.ReplacementMaster プロパティ (Visio)](https://msdn.microsoft.com/library/326a1889-8952-b4ac-c5c0-ac4470257c06%28Office.15%29.aspx) <br/> [ReplaceShapesEvent.SelectionSource プロパティ (Visio)](https://msdn.microsoft.com/library/f81c0b66-b63b-fc7c-1769-d56a17d5cf78%28Office.15%29.aspx) <br/> [ReplaceShapesEvent.Stat プロパティ (Visio)](https://msdn.microsoft.com/library/96f3d382-5dda-7f93-088d-96edc831cd7c%28Office.15%29.aspx) <br/> |なし  <br/> |
   
次の表に、2013 年に導入された新しい列挙と定数Visio示します。
  
 **表 3. Visio の列挙の追加**
  
|**列挙**|**説明**|
|:-----|:-----|
|[VisQuickStyleColors 列挙 (Visio)](https://msdn.microsoft.com/library/c19d91f3-a9a4-e31e-ed7a-eef15553fbf4%28Office.15%29.aspx) <br/> |テーマに含まれる指定した名前の色を指定します。  <br/> |
|[VisQuickStyleMatrixIndices 列挙 (Visio)](https://msdn.microsoft.com/library/0fb0b448-85ba-4fc4-d933-21d574cefa2a%28Office.15%29.aspx) <br/> |2013 年に指定されたテーマとバリエーションの指定Visioします。  <br/> |
|[VisReplaceFlags 列挙 (Visio)](https://msdn.microsoft.com/library/cf270178-f939-7eb4-b8e1-3b4153aff221%28Office.15%29.aspx) <br/> |図形の変更操作の動作を指定します。  <br/> |
|[VisSVGExportFormat 列挙 (Visio)](https://msdn.microsoft.com/library/d8ca8c3f-41d9-4e9d-8f6d-f5567361b14e%28Office.15%29.aspx) <br/> |図を SVG にエクスポートするときに、Visio マークアップを含めるか除外するかを指定します。  <br/> |
   
### <a name="deprecated-objects-and-members"></a>使用されていないオブジェクトおよびメンバー

次の表に、2013 年に導入された非推奨のオブジェクトとVisio示します。 「**使用されていないメンバー**」列に、使用されなくなったオブジェクト メンバーだけを記載します。 
  
 **表 4. Visio オブジェクト モデルで使用されていないメンバー**
  
|**オブジェクトまたはコレクション**|**使用されていないメンバー**|
|:-----|:-----|
|**Window** オブジェクト  <br/> |**PageTabWidth** プロパティ  <br/> |
   
## <a name="see-also"></a>関連項目
<a name="vis15_WhatsNew_Additional"> </a>

- [開発者向けの Visio 情報](https://msdn.microsoft.com/office/aa905478.aspx)
    
- [Visio ShapeSheet 開発者向け新機能](what-s-new-for-visio-shapesheet-developers.md)
    
- [SharePoint 2013 の Visio Services](https://msdn.microsoft.com/library/jj164027%28office.15%29.aspx)
    
- [Visio の新機能 (Office.com)](https://office.com/redir/HA102749364.aspx)
    
- [Visio デベロッパー センター](https://msdn.microsoft.com/office/aa905478.aspx)
    

