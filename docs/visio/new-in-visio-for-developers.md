---
title: 開発者向け Visio の新機能
manager: soliver
ms.date: 09/18/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7e3fb858-0ab8-bd2e-217c-c85b10d79785
description: このドキュメントでは、最上位のビューの機能強化と Visio 2013 の開発者向けの追加機能を提供します。 Visio プラットフォームでのジャンプ スタートを取得する準備ができている開発者は、Visio 2013 に関するコーディングを開始するための十分な詳細を提供します。
ms.openlocfilehash: 3e0f119ac0b6b43737ff394a4553405982a4ec04
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805928"
---
# <a name="new-in-visio-for-developers"></a>開発者向け Visio の新機能

このドキュメントでは、最上位のビューの機能強化と Visio 2013 の開発者向けの追加機能を提供します。 Visio プラットフォームでのジャンプ スタートを取得する準備ができている開発者は、Visio 2013 に関するコーディングを開始するための十分な詳細を提供します。
  
## <a name="introduction"></a>概要
<a name="vis15_WhatsNew_Intro"> </a>

Visio 2013 は、カスタム描画ソリューションの 1 つの強力なプラットフォームを提供します。 新しいオブジェクト、コレクション、プロパティ、メソッド、列挙、およびイベントと共に、新しいシェイプ シート セルおよび関数を使用することにより、ソリューションで要素の動作を定義するため。
  
Visio 2013 の開発者を対象の新機能は、新しいファイル形式です。テーマに信頼性の高い更新プログラム変更する図形の機能を (することを別の図形を置き換えます)。新しい図形の効果です。強化されたコメントです。SharePoint Server 2013 はの共同編集カスタマイズ可能なイメージのクリッピングです。相対的なジオメトリです。Business Connectivity Services (BCS) のデータのサポートMicrosoft SharePoint Server 2013 は、Visio Services の更新重複しているページの機能です。 このトピックでは、各機能の簡単な概要を提供し、新しい Visio のオブジェクトと機能に関連付けられているでは、Visual Basic for Applications (VBA) を公開するメンバーの一部を紹介します。 これらの機能と付属のコード サンプルについては、 [Visio デベロッパー センター](http://msdn.microsoft.com/en-us/office/aa905478.aspx)を参照してください。
  
> [!NOTE]
> Visio 2013 には、多く新しいシェイプ シートのセル、行、および Visio の新しい機能をサポートする機能が含まれています。 Visio 2013 のシェイプ シートでは新規の詳細については、 [Visio のシェイプ シート開発者向けの新はどのような](what-s-new-for-visio-shapesheet-developers.md)資料を参照してください。 
  
## <a name="new-file-format"></a>新しいファイル形式
<a name="vis15_WhatsNew_NewFF"> </a>

Visio 2013 で導入された新しいファイル形式は、Open Packaging Conventions (OPC) 標準 (ISO 29500、パート 2) と、以前の Visio XML ファイル形式 (.vdx) の XML 要素が基になっています。 その他のアプリケーションで使用されるファイル形式に似ています (zip 形式)、XML ベースのファイル形式です。
  
新しいファイル形式は、Visio 2013 と Visio サービスの両方では、Microsoft SharePoint Server 2013 ではため、Visio 図面を Visio Web 図面 (.vdw) としてファイルを発行することがなく SharePoint Server ライブラリに直接保存できます。 そうであっても、Visio Services が読み取りも、および Visio Web 図面のファイルを表示できます。
  
この新しいファイル形式には、次のファイルの種類 (拡張子で区別する) が含まれます。
  
- .vsdx (Visio 図面)
    
- .vsdm (Visio マクロ対応図面)
    
- .vssx (Visio ステンシル)
    
- .vssm (Visio マクロ対応ステンシル)
    
- .vstx (Visio テンプレート)
    
- .vstm (Visio マクロ対応テンプレート)
    
読み取りと書き込み ( [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) ) などのファイル形式のパッケージを ( [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) ) の XML を解析して、既存のサポートを使用して、新しいファイル形式をプログラムで操作できます。 
  
Visio 2013 には、(.vsd、.vss、.vst、.vdx、.vsx、.vtx、.vdw、.vwi) は、古いファイル形式を読み取る機能が保持されます。 Visio 2013 は、前の Visio の XML ファイル形式 (.vdx) は保存されません。 ソリューションまたは以前の Visio の XML ファイルの形式 (.vdx) ファイルを使用するツールは、新しいファイル形式およびそのスキーマを読み込むためにリファクタリングする必要があります。
  
Visio Services では、ブラウザーで Visio Web 図面 (.vdw) 形式のファイルを表示できます。また、新しいファイル形式の Visio 図面 (.vsdx) と Visio マクロ対応図面 (.vsdm) 形式を表示できるようになりました。
  
## <a name="themes"></a>テーマ
<a name="vis15_WhatsNew_Themes"> </a>

テーマのデザインは Visio 2013 で変更され、図形とアートの効果の統合など、より多彩な効果やスタイルを使用するようになっています。 ユーザーことができます今すぐテーマを適用することにより、包括的なスタイルを決定、テーマのバリエーションを含むダイアグラムをカスタマイズおよびクイック スタイルを使用して個々 の図形を強調表示します。 シェイプ シート開発者では、新しい機能と、[シェイプ シートのセルのこれらの機能を利用できます。
  
テーマの操作は、[ページ](http://msdn.microsoft.com/library/7a7f37ab-b448-eb70-b4f1-c185dfbd511e%28Office.15%29.aspx)、[図形](http://msdn.microsoft.com/library/da7a8872-4ebb-a607-e0ed-eebf68ff5630%28Office.15%29.aspx)、および[選択範囲](http://msdn.microsoft.com/library/e5734140-6dbe-7de8-9695-1a22fb4ac628%28Office.15%29.aspx)オブジェクトのレベルでも実行できます。テーマを操作するための新しい API には、[Page.SetTheme](http://msdn.microsoft.com/library/5a186f58-9a7a-bd8a-826b-85da75a4d59f%28Office.15%29.aspx) メソッド、[Page.SetThemeVariant](http://msdn.microsoft.com/library/8393a95f-83ca-0efa-d987-ae498bfe5e9d%28Office.15%29.aspx) メソッド、[Shape.SetQuickStyle](http://msdn.microsoft.com/library/aebe80cb-fae9-0be7-e903-882f6eb58b63%28Office.15%29.aspx) メソッド、および [Selection.SetQuickStyle](http://msdn.microsoft.com/library/39b810b5-0738-daed-0103-8a2df07559c6%28Office.15%29.aspx) メソッドなどがあります。 
  
Visio 2013 の新しい Api の詳細については、この資料の[Visio オブジェクト モデルの変更](#vis15_WhatsNew_NewOM)」を参照してください。 Visio 2013 の新しいシェイプ シート セルの詳細については、 [Visio のシェイプ シート開発者向けの新はどのような](what-s-new-for-visio-shapesheet-developers.md)資料を参照してください。
  
## <a name="change-shape"></a>図形の変更
<a name="vis15_WhatsNew_ChangeShapes"> </a>

Visio 2013 には、図形交換いくつかの図形のテキストの図形、図形データ、または図形の書式設定と同様に、元の図形からローカルの値を保持しながら、ステンシルに含まれている別の図形の 1 つまたは複数の図形をスワップすることを可能にする API が含まれています。 図形の開発者は、それらの図形の図形の変更動作を指定するのには、カスタム図形のシェイプ シートの設定を更新できます。 新しい Api は、 [Shape.ReplaceShapes](http://msdn.microsoft.com/library/b330a63d-4e3f-0c4d-c38c-6ee806670225%28Office.15%29.aspx)メソッドと[Selection.ReplaceShapes](http://msdn.microsoft.com/library/dc278901-77ce-e1fe-c44f-f464bbb1c360%28Office.15%29.aspx)メソッドと[ReplaceShape](http://msdn.microsoft.com/library/26c4e7cb-6618-6d2f-a4be-515584f8cd10%28Office.15%29.aspx)のイベントがあります。 
  
Visio 2013 の新しい Api の詳細については、この資料の[Visio オブジェクト モデルの変更](#vis15_WhatsNew_NewOM)」を参照してください。 Visio 2013 の新しいシェイプ シート セルの詳細については、 [Visio のシェイプ シート開発者向けの新はどのような](what-s-new-for-visio-shapesheet-developers.md)資料を参照してください。
  
## <a name="shape-effects"></a>図形の効果
<a name="vis15_WhatsNew_ShapeEffects"> </a>

面取り、3D 回転、光彩、反射、スケッチなどの新しい図形の効果が、Visio 2013 に追加されています。 シェイプ シートには、これらの影響を操作するための新しいセルが含まれています。
  
Visio 2013 の新しいシェイプ シート セルの詳細については、 [Visio のシェイプ シート開発者向けの新はどのような](what-s-new-for-visio-shapesheet-developers.md)資料を参照してください。
  
## <a name="commenting"></a>コメント入力
<a name="vis15_WhatsNew_Commenting"> </a>

Visio 2013 には新しいコメント入力フレームワークが含まれます。 コメントを特定の図形やページと関連付けることができます。 Visio 2013 には、2 つの新しいオブジェクト、[コメント](http://msdn.microsoft.com/library/f028cc03-0ef1-8017-a936-d30d45211864%28Office.15%29.aspx)および[コメント](http://msdn.microsoft.com/library/7cd0ee53-6b8d-a03b-ecd6-f6f6dda0f2d4%28Office.15%29.aspx)が含まれています。 コメントをプログラムでアクセスするための新しい Api には、 [Document.Comments](http://msdn.microsoft.com/library/15a322ad-70eb-1487-701d-76e2fde73309%28Office.15%29.aspx)、 [Page.Comments](http://msdn.microsoft.com/library/9618c86c-96c0-be95-ee20-5d1b99f4d5e8%28Office.15%29.aspx)、 [Shape.Comments](http://msdn.microsoft.com/library/498eca91-beb9-b764-0262-a935e5205710%28Office.15%29.aspx)、および[Page.ShapeComments](http://msdn.microsoft.com/library/b7d86594-ba1f-627b-222f-905da1b1201e%28Office.15%29.aspx)プロパティが含まれます。 
  
Visio のサービスには、ページまたは図表内の図形からコメントを読むに JavaScript Api が含まれています。
  
Visio 2013 の新しい Api の詳細については、この資料の[Visio オブジェクト モデルの変更](#vis15_WhatsNew_NewOM)」を参照してください。 
  
> [!NOTE]
> コメントは、シェイプシートからはアクセスできなくなりました。 
  
## <a name="coauthoring"></a>共同編集
<a name="vis15_WhatsNew_Coauthoring"> </a>

Visio 2013 には、SharePoint またはマイクロソフトの OneDrive に格納されている共同作成者の図の機能が含まれています。 開発者には、共同編集のための図の変更に関する情報を提供する[Document.AfterDocumentMerge](http://msdn.microsoft.com/library/50658da5-592a-4d16-908f-c6abe3050f09%28Office.15%29.aspx)イベントへのアクセスがあります。 ソリューション開発者は、図面のシェイプ シートのセルの[NoCoauth](nocoauth-cell-document-properties-section.md)を使用して、カスタムのニーズに合わせて共同編集を無効にすることもあります。 
  
Visio 2013 の新しい Api の詳細については、この資料の[Visio オブジェクト モデルの変更](#vis15_WhatsNew_NewOM)」を参照してください。 
  
## <a name="customizable-image-clipping"></a>カスタマイズ可能なイメージ クリップ
<a name="vis15_WhatsNew_ClipImages"> </a>

Visio 2013 は、任意の図形にトリミングされるカスタム イメージ クリップ パスの定義をサポートします。 これは、長方形の方法でクリップの画像をサポートして、Visio 2010 の容量を拡張します。 この機能は **、外部イメージ情報**」セクションで、 [ClippingPath](clippingpath-cell-foreign-image-info-section.md)のセルを使用してシェイプ シートで使用可能です。 
  
Visio 2013 の新しいシェイプ シート セルの詳細については、 [Visio のシェイプ シート開発者向けの新はどのような](what-s-new-for-visio-shapesheet-developers.md)資料を参照してください。
  
## <a name="relative-geometries"></a>相対的な形状
<a name="vis15_WhatsNew_RelativeGeometry"> </a>

以前のバージョンの Visio では、図形の座標は図形の幅、高さに依存する数式で定義されました。 たとえば、Visio 2010 では多くの組み込みの Visio 図形の頂点が定数で、図形の幅、高さを乗算することによって定義されました。 これらの図形と同じように数式を使用して (例えば) [[moveto]](moveto-row-geometry-section.md)または[[lineto]](lineto-row-geometry-section.md)行を含む [ **Geometry** ] セクションが`Width*1`と`Height*0`。
  
Visio 2013 は、シェイプ シート内の相対的なジオメトリをサポートしています。 図形の開発者では、単純な値または式で、高さまたは幅が自動的に乗算としてジオメトリを指定するのには相対的なジオメトリを使用できます。 図形の頂点今すぐ表現できる定数、たとえば、頂点を図形の幅または高さの倍数として表現する必要性をなくします。 これにより、パフォーマンスが向上し、ファイルサイズが小さく、図形を作成する開発者が容易になります。 新しい行には、位置**X**と**Y**のセルの値に自動的が掛けられます幅または図形の高さを (それぞれ) [RelMoveTo](relmoveto-row-geometry-section.md)と[RelLineTo](rellineto-row-geometry-section.md)の行が含まれます。 
  
Visio 2013 の新しいシェイプ シート行の詳細については、 [Visio のシェイプ シート開発者向けの新はどのような](what-s-new-for-visio-shapesheet-developers.md)資料を参照してください。
  
## <a name="support-for-business-connectivity-services-bcs-data"></a>Business Connectivity Services (BCS) データのサポート
<a name="vis15_WhatsNew_BCS"> </a>

Visio 2013 の図は、SharePoint Server 2013 のサーバー上の外部リストに今すぐ接続できます。 外部リストは、Microsoft Business Connectivity Services (BCS) を使用して SharePoint リストに接続されている SharePoint (たとえば、SQL Server テーブル) の外部のコンテンツのソースです。 Visio Services では、データの更新プログラムとして Visio 図面を更新する機能をサポートしています。
  
Visio Services では新規の詳細については、「 [SharePoint 2013 で Visio Services](http://msdn.microsoft.com/en-us/library/jj164027%28office.15%29.aspx)」を参照してください。 Business Connectivity Services (BCS) の詳細については、 [SharePoint 2013 での Business Connectivity Services](http://msdn.microsoft.com/en-us/library/jj163782%28office.15%29.aspx)を参照してください。
  
## <a name="improvements-in-visio-services"></a>Visio Services の機能強化
<a name="vis15_WhatsNew_VisioServices"> </a>

Microsoft SharePoint Server 2013 で Visio のサービスには、多くの改良が含まれています。 前述のように、Visio Services は、新しい Visio ファイルの形式 (.vsdx と .vsdm の両方) をサポートします。 データの更新や再計算、図全体にわたって、数式を再計算する機能など、Visio のサービスを拡大しました。 
  
Visio Services では新規の詳細については、「 [SharePoint 2013 で Visio Services](http://msdn.microsoft.com/en-us/library/jj164027%28office.15%29.aspx)」を参照してください。
  
## <a name="duplicate-page"></a>ページの複製
<a name="vis15_WhatsNew_DuplicatePage"> </a>

Visio 2013 で、ページとすべての同じ文書内の図形をコピーできます。 したがって、**ページ**オブジェクトには、[重複する](http://msdn.microsoft.com/library/394be23b-997d-0da1-b3bd-8278564fb4e0%28Office.15%29.aspx)ページを複製し、新規の**Page**オブジェクトを返しますが、新しいメソッドがあります。 
  
## <a name="visio-object-model-changes"></a>Visio オブジェクト モデルの変更
<a name="vis15_WhatsNew_NewOM"> </a>

Visio 2013 の新機能のプログラミングのサポートを提供するのには Visio のオブジェクト モデルに、新しいオブジェクト、プロパティ、メソッド、およびイベントが追加されました。 さらに、オブジェクト モデルの機能強化には、Visio プラットフォームへの変更の要求を頻繁に開発者が対応します。
  
### <a name="new-members"></a>新しいメンバー

Visio のオブジェクト モデル内の既存のオブジェクトには、次のメンバーが追加されました。
  
 **表 1. Visio オブジェクト モデルの機能拡張**
  
|**オブジェクトまたはコレクション**|**新しいメンバー**|
|:-----|:-----|
|[Application オブジェクト (Visio)](http://msdn.microsoft.com/library/5b3c8939-793f-116f-11b8-1d4170d95a63%28Office.15%29.aspx) <br/> |[Application.AfterReplaceShapes イベント (Visio)](http://msdn.microsoft.com/library/b02de031-086a-41cc-d832-5434b8096444%28Office.15%29.aspx) <br/> |
||[Application.BeforeReplaceShapes イベント (Visio)](http://msdn.microsoft.com/library/fbf44569-0539-9292-ce20-1f9e34238b33%28Office.15%29.aspx) <br/> |
||[Application.QueryCancelReplaceShapes イベント (Visio)](http://msdn.microsoft.com/library/50c0f2a6-f534-f3af-7e83-c865abda8bf9%28Office.15%29.aspx) <br/> |
||[Application.ReplaceShapesCanceled イベント (Visio)](http://msdn.microsoft.com/library/e8eecd64-e4bd-d2c4-b942-c5ff607a4121%28Office.15%29.aspx) <br/> |
|[ApplicationSettings オブジェクト (Visio)](http://msdn.microsoft.com/library/f2e24211-ecc6-e0f5-4c00-fc50f98a3505%28Office.15%29.aspx) <br/> |[ApplicationSettings.EnterCommitsText プロパティ (Visio)](http://msdn.microsoft.com/library/ba9ce9fa-d224-cdc3-668d-46c1849911c7%28Office.15%29.aspx) <br/> |
||[ApplicationSettings.SVGExportFormat プロパティ (Visio)](http://msdn.microsoft.com/library/9e7ca1cb-5ace-b75b-0e59-61566b9a0169%28Office.15%29.aspx) <br/> |
|[Document オブジェクト (Visio)](http://msdn.microsoft.com/library/21640062-13a2-a2b2-7c61-7e707671207c%28Office.15%29.aspx) <br/> |[Document.AfterDocumentMerge イベント (Visio)](http://msdn.microsoft.com/library/50658da5-592a-4d16-908f-c6abe3050f09%28Office.15%29.aspx) <br/> |
||[Document.Comments プロパティ (Visio)](http://msdn.microsoft.com/library/15a322ad-70eb-1487-701d-76e2fde73309%28Office.15%29.aspx) <br/> |
||[Document.CompatibilityMode プロパティ (Visio)](http://msdn.microsoft.com/library/98fc00d3-5d2b-218e-9828-b5581ee7313d%28Office.15%29.aspx) <br/> |
|[ドキュメント オブジェクト (Visio)](http://msdn.microsoft.com/library/e9291149-964e-c6fb-4c62-bf2f35a6a0a7%28Office.15%29.aspx) <br/> |[Documents.AfterDocumentMerge イベント (Visio)](http://msdn.microsoft.com/library/cac0544d-77b9-b722-cfdb-e42475ce2558%28Office.15%29.aspx) <br/> |
||[Documents.AfterReplaceShapes イベント (Visio)](http://msdn.microsoft.com/library/e01c069e-440b-7b8b-8d7d-cdb664f6e2d6%28Office.15%29.aspx) <br/> |
||[Documents.BeforeReplaceShapes イベント (Visio)](http://msdn.microsoft.com/library/55a66c47-a2ca-5c8a-2693-aaa1b079c704%28Office.15%29.aspx) <br/> |
||[Documents.QueryCancelReplaceShapes イベント (Visio)](http://msdn.microsoft.com/library/d613730e-04c8-d17f-0ad1-19e976aa107d%28Office.15%29.aspx) <br/> |
||[Documents.ReplaceShapesCanceled イベント (Visio)](http://msdn.microsoft.com/library/94a20fe7-da09-4e3c-d048-05ba0b8f1070%28Office.15%29.aspx) <br/> |
|[InvisibleApp オブジェクト (Visio)](http://msdn.microsoft.com/library/70a30571-2017-af8b-eaa1-bf93c758a46a%28Office.15%29.aspx) <br/> |[InvisibleApp.AfterReplaceShapes イベント (Visio)](http://msdn.microsoft.com/library/5d7b8ec2-ef65-1a49-fb50-3fae95d56761%28Office.15%29.aspx) <br/> |
||[InvisibleApp.BeforeReplaceShapes イベント (Visio)](http://msdn.microsoft.com/library/bd0e37ca-887a-4d53-3b0c-3339492df3dd%28Office.15%29.aspx) <br/> |
||[InvisibleApp.QueryCancelReplaceShapes イベント (Visio)](http://msdn.microsoft.com/library/5e5d9b76-dfd4-1d02-d205-9e64350449d5%28Office.15%29.aspx) <br/> |
||[InvisibleApp.ReplaceShapesCanceled イベント (Visio)](http://msdn.microsoft.com/library/17e43497-c7a8-8546-595c-4630afb301a3%28Office.15%29.aspx) <br/> |
|[Page オブジェクト (Visio)](http://msdn.microsoft.com/library/7a7f37ab-b448-eb70-b4f1-c185dfbd511e%28Office.15%29.aspx) <br/> |[Page.AfterReplaceShapes イベント (Visio)](http://msdn.microsoft.com/library/e4005987-acb1-78d7-91fb-c3c2d5b036e3%28Office.15%29.aspx) <br/> |
||[Page.BeforeReplaceShapes イベント (Visio)](http://msdn.microsoft.com/library/57ea9836-74dd-77c2-6541-f8f61b89c0b6%28Office.15%29.aspx) <br/> |
||[Page.Comments プロパティ (Visio)](http://msdn.microsoft.com/library/9618c86c-96c0-be95-ee20-5d1b99f4d5e8%28Office.15%29.aspx) <br/> |
||[Page.Duplicate メソッド (Visio)](http://msdn.microsoft.com/library/394be23b-997d-0da1-b3bd-8278564fb4e0%28Office.15%29.aspx) <br/> |
||[Page.GetTheme メソッド (Visio)](http://msdn.microsoft.com/library/31c84e69-0bc8-2d1a-84d8-7397110d74ae%28Office.15%29.aspx) <br/> |
||[Page.GetThemeVariant メソッド (Visio)](http://msdn.microsoft.com/library/40c2be31-fdb0-68ee-a129-2788b1b17c82%28Office.15%29.aspx) <br/> |
||[Page.QueryCancelReplaceShapes イベント (Visio)](http://msdn.microsoft.com/library/17ead23f-825a-c608-3315-e2eed6784cd5%28Office.15%29.aspx) <br/> |
||[Page.ReplaceShapesCanceled イベント (Visio)](http://msdn.microsoft.com/library/867b1fc1-96bd-cbeb-fd61-b02a96e039ca%28Office.15%29.aspx) <br/> |
||[Page.SetTheme メソッド (Visio)](http://msdn.microsoft.com/library/5a186f58-9a7a-bd8a-826b-85da75a4d59f%28Office.15%29.aspx) <br/> |
||[Page.SetThemeVariant メソッド (Visio)](http://msdn.microsoft.com/library/8393a95f-83ca-0efa-d987-ae498bfe5e9d%28Office.15%29.aspx) <br/> |
||[Page.ShapeComments プロパティ (Visio)](http://msdn.microsoft.com/library/b7d86594-ba1f-627b-222f-905da1b1201e%28Office.15%29.aspx) <br/> |
|[ページ オブジェクト (Visio)](http://msdn.microsoft.com/library/45eec568-b5cc-5e80-ff5c-4dfa567efb5d%28Office.15%29.aspx) <br/> |[Pages.AfterReplaceShapes イベント (Visio)](http://msdn.microsoft.com/library/05c33bdd-e697-d36e-46a8-45705e9ad2c2%28Office.15%29.aspx) <br/> |
||[Pages.BeforeReplaceShapes イベント (Visio)](http://msdn.microsoft.com/library/3f6dbc31-0583-dd67-0432-335d6df7a50c%28Office.15%29.aspx) <br/> |
||[Pages.QueryCancelReplaceShapes イベント (Visio)](http://msdn.microsoft.com/library/d11ff976-0016-da6b-92fb-379baa7e8f94%28Office.15%29.aspx) <br/> |
||[Pages.ReplaceShapesCanceled イベント (Visio)](http://msdn.microsoft.com/library/f0ce8c66-7a15-5f91-8c89-e177bc6671d2%28Office.15%29.aspx) <br/> |
|[Selection オブジェクト (Visio)](http://msdn.microsoft.com/library/e5734140-6dbe-7de8-9695-1a22fb4ac628%28Office.15%29.aspx) <br/> |[Selection.ReplaceShape メソッド (Visio)](http://msdn.microsoft.com/library/dc278901-77ce-e1fe-c44f-f464bbb1c360%28Office.15%29.aspx) <br/> |
||[Selection.SetQuickStyle メソッド (Visio)](http://msdn.microsoft.com/library/39b810b5-0738-daed-0103-8a2df07559c6%28Office.15%29.aspx) <br/> |
|[Shape オブジェクト (Visio)](http://msdn.microsoft.com/library/da7a8872-4ebb-a607-e0ed-eebf68ff5630%28Office.15%29.aspx) <br/> |[Shape.ChangePicture メソッド (Visio)](http://msdn.microsoft.com/library/9193d802-cebd-2bfd-5f8e-400fac36c1a5%28Office.15%29.aspx) <br/> |
||[Shape.Comments プロパティ (Visio)](http://msdn.microsoft.com/library/498eca91-beb9-b764-0262-a935e5205710%28Office.15%29.aspx) <br/> |
||[Shape.ReplaceShape メソッド (Visio)](http://msdn.microsoft.com/library/b330a63d-4e3f-0c4d-c38c-6ee806670225%28Office.15%29.aspx) <br/> |
||[Shape.SetQuickStyle メソッド (Visio)](http://msdn.microsoft.com/library/aebe80cb-fae9-0be7-e903-882f6eb58b63%28Office.15%29.aspx) <br/> |
   
### <a name="new-objects-and-enumerations"></a>新しいオブジェクトと列挙

Visio オブジェクト モデルには、次のオブジェクトが追加されました。
  
 **表 2. Visio オブジェクト モデルへの追加**
  
|**オブジェクト**|**プロパティ**|**メソッド**|
|:-----|:-----|:-----|
|[CoauthMergeEvent オブジェクト (Visio)](http://msdn.microsoft.com/library/eb9425cb-0108-4909-e334-9cd51e5b9303%28Office.15%29.aspx) <br/> |[CoauthMergeEvent.BaseDocument プロパティ (Visio)](http://msdn.microsoft.com/library/7ec09a85-6f51-685b-0c87-4b9eb3266773%28Office.15%29.aspx) <br/> [CoauthMergeEvent.DownloadDocument プロパティ (Visio)](http://msdn.microsoft.com/library/19239540-cd5a-13ea-3b26-282ac3676abd%28Office.15%29.aspx) <br/> [CoauthMergeEvent.ObjectType プロパティ (Visio)](http://msdn.microsoft.com/library/01baa0c2-75b7-2713-9732-1e7a8a7b33aa%28Office.15%29.aspx) <br/> [CoauthMergeEvent.Stat プロパティ (Visio)](http://msdn.microsoft.com/library/d8a96b8e-36b5-c61f-8cea-76266f7eed39%28Office.15%29.aspx) <br/> [CoauthMergeEvent.WorkingDocument プロパティ (Visio)](http://msdn.microsoft.com/library/0f3c4358-0d63-df7f-12fe-7f378bacca86%28Office.15%29.aspx) <br/> |なし  <br/> |
|[コメント オブジェクト (Visio)](http://msdn.microsoft.com/library/f028cc03-0ef1-8017-a936-d30d45211864%28Office.15%29.aspx) <br/> |[Comment.AssociatedObject プロパティ (Visio)](http://msdn.microsoft.com/library/e28eed2e-260e-59c9-9b24-631817fe1ae1%28Office.15%29.aspx) <br/> [Comment.AuthorInitials プロパティ (Visio)](http://msdn.microsoft.com/library/abc07100-8c5c-9982-674d-40b58c096816%28Office.15%29.aspx) <br/> [Comment.AuthorName プロパティ (Visio)](http://msdn.microsoft.com/library/e1da4db8-7a16-16bf-2a5f-be1ac5372d34%28Office.15%29.aspx) <br/> [Comment.AuthorSipAddress プロパティ (Visio)](http://msdn.microsoft.com/library/f8d185a9-91b6-471a-3c0e-ffa8a06b36b3%28Office.15%29.aspx) <br/> [Comment.AuthorSMTPAddress プロパティ (Visio)](http://msdn.microsoft.com/library/22e04ccc-c524-ca08-d5e2-db68fdb3afb6%28Office.15%29.aspx) <br/> [Comment.Collapsed プロパティ (Visio)](http://msdn.microsoft.com/library/9552e379-e351-78d7-e0ed-4f524c3273a1%28Office.15%29.aspx) <br/> [Comment.CreateDate プロパティ (Visio)](http://msdn.microsoft.com/library/b643e13e-da12-a992-3a59-99b37f003fb9%28Office.15%29.aspx) <br/> [Comment.Document プロパティ (Visio)](http://msdn.microsoft.com/library/d57b1377-b895-1fe1-2f98-ef000fdd9c39%28Office.15%29.aspx) <br/> [Comment.EditDate プロパティ (Visio)](http://msdn.microsoft.com/library/4ad13f54-215e-3680-5de6-13715e309fbf%28Office.15%29.aspx) <br/> [Comment.ObjectType プロパティ (Visio)](http://msdn.microsoft.com/library/bf0d786d-e1b6-65f1-3112-5dfd4ff324e9%28Office.15%29.aspx) <br/> [Comment.Stat プロパティ (Visio)](http://msdn.microsoft.com/library/f457598c-af42-cb83-ecd2-4fd42898ea16%28Office.15%29.aspx) <br/> [Comment.Text プロパティ (Visio)](http://msdn.microsoft.com/library/3ec63034-de5f-d9f2-16a5-e06a56883867%28Office.15%29.aspx) <br/> |[Comment.Delete メソッド (Visio)](http://msdn.microsoft.com/library/7762f264-f680-5758-7c35-dfe9067b61ca%28Office.15%29.aspx) <br/> |
|[コメント オブジェクト (Visio)](http://msdn.microsoft.com/library/7cd0ee53-6b8d-a03b-ecd6-f6f6dda0f2d4%28Office.15%29.aspx) <br/> |[Comments.Count プロパティ (Visio)](http://msdn.microsoft.com/library/abac02d5-5047-2c9d-5c5c-e2738f99a4a6%28Office.15%29.aspx) <br/> [Comments.Document プロパティ (Visio)](http://msdn.microsoft.com/library/507d4698-e282-f8a9-1299-c67945ee5fc4%28Office.15%29.aspx) <br/> [Comments.Item プロパティ (Visio)](http://msdn.microsoft.com/library/fed2a079-de87-d5ce-1d74-0bfa5a328441%28Office.15%29.aspx) <br/> [Comments.ObjectType プロパティ (Visio)](http://msdn.microsoft.com/library/06544d73-ce00-2c89-1ecb-20541b251d57%28Office.15%29.aspx) <br/> [Comments.Stat プロパティ (Visio)](http://msdn.microsoft.com/library/1f5f29b2-236c-91b6-6d25-7bacc37ca96c%28Office.15%29.aspx) <br/> |[Comments.Add メソッド (Visio)](http://msdn.microsoft.com/library/da02de49-8057-7e5c-6b59-0a013e56256d%28Office.15%29.aspx) <br/> [Comments.DeleteAll メソッド (Visio)](http://msdn.microsoft.com/library/50777ed3-553c-90ae-2d30-9dde412fe6b9%28Office.15%29.aspx) <br/> |
|[ReplaceShapesEvent オブジェクト (Visio)](http://msdn.microsoft.com/library/26c4e7cb-6618-6d2f-a4be-515584f8cd10%28Office.15%29.aspx) <br/> |[ReplaceShapesEvent.ObjectType プロパティ (Visio)](http://msdn.microsoft.com/library/bcc442f0-aa4e-cd5a-d116-f3fb74459927%28Office.15%29.aspx) <br/> [ReplaceShapesEvent.ReplaceFlags プロパティ (Visio)](http://msdn.microsoft.com/library/d0d00891-c794-bd0c-d37e-1ab98c92beab%28Office.15%29.aspx) <br/> [ReplaceShapesEvent.ReplacementMaster プロパティ (Visio)](http://msdn.microsoft.com/library/326a1889-8952-b4ac-c5c0-ac4470257c06%28Office.15%29.aspx) <br/> [ReplaceShapesEvent.SelectionSource プロパティ (Visio)](http://msdn.microsoft.com/library/f81c0b66-b63b-fc7c-1769-d56a17d5cf78%28Office.15%29.aspx) <br/> [ReplaceShapesEvent.Stat プロパティ (Visio)](http://msdn.microsoft.com/library/96f3d382-5dda-7f93-088d-96edc831cd7c%28Office.15%29.aspx) <br/> |なし  <br/> |
   
新しい列挙体と Visio 2013 で導入された定数は、次を表します。
  
 **表 3. Visio の列挙の追加**
  
|**列挙**|**説明**|
|:-----|:-----|
|[VisQuickStyleColors 列挙型 (Visio)](http://msdn.microsoft.com/library/c19d91f3-a9a4-e31e-ed7a-eef15553fbf4%28Office.15%29.aspx) <br/> |テーマに含まれる指定した名前の色を指定します。  <br/> |
|[VisQuickStyleMatrixIndices 列挙型 (Visio)](http://msdn.microsoft.com/library/0fb0b448-85ba-4fc4-d933-21d574cefa2a%28Office.15%29.aspx) <br/> |テーマと Visio 2013 で提供されるバリエーションに指定された名前を指定します。  <br/> |
|[VisReplaceFlags 列挙型 (Visio)](http://msdn.microsoft.com/library/cf270178-f939-7eb4-b8e1-3b4153aff221%28Office.15%29.aspx) <br/> |図形の変更操作の動作を指定します。  <br/> |
|[VisSVGExportFormat 列挙型 (Visio)](http://msdn.microsoft.com/library/d8ca8c3f-41d9-4e9d-8f6d-f5567361b14e%28Office.15%29.aspx) <br/> |図を SVG にエクスポートするときに、Visio マークアップを含めるか除外するかを指定します。  <br/> |
   
### <a name="deprecated-objects-and-members"></a>使用されていないオブジェクトおよびメンバー

次の表は、非推奨のオブジェクトと Visio 2013 で導入されたメンバーを一覧します。 のみメンバーが**メンバーを非推奨**] 列に一覧表示されたオブジェクトは使用されなくなりました。 
  
 **表 4. Visio オブジェクト モデルで使用されていないメンバー**
  
|**オブジェクトまたはコレクション**|**使用されていないメンバー**|
|:-----|:-----|
|**ウィンドウ**オブジェクト  <br/> |**PageTabWidth**プロパティ  <br/> |
   
## <a name="see-also"></a>関連項目
<a name="vis15_WhatsNew_Additional"> </a>

- [開発者は、Visio](http://msdn.microsoft.com/en-us/office/aa905478.aspx)
    
- [Visio ShapeSheet 開発者向け新機能](what-s-new-for-visio-shapesheet-developers.md)
    
- [SharePoint 2013 の Visio Services](http://msdn.microsoft.com/en-us/library/jj164027%28office.15%29.aspx)
    
- [(Office.com) の Visio の新機能](http://office.com/redir/HA102749364.aspx)
    
- [Visio デベロッパー センター](http://msdn.microsoft.com/en-us/office/aa905478.aspx)
    

