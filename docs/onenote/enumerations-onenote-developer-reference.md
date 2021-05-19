---
title: 列挙 (OneNote開発者向け参照)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 62912d6e-c39e-4f8b-8cdb-ae9b6376cbc0
description: このトピックでは、2013 オブジェクト モデルのOneNoteについて説明します。
ms.openlocfilehash: 3338e444e5b0bfd0239e363c3161aeb1914b2d53
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410337"
---
# <a name="enumerations-onenote-developer-reference"></a>列挙 (OneNote開発者向け参照)

このトピックでは、2013 オブジェクト モデルのOneNoteについて説明します。
  
## <a name="createfiletype"></a>CreateFileType
<a name="odc_CreateFileType"> </a>

**OpenHierarchy** メソッドに渡された場合、メソッドに渡されたパスがまだ存在しない場合は、作成するオブジェクトの種類を指定します (存在する場合)。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**cftNone** <br/> |0  <br/> |新しいオブジェクトを作成します。  <br/> |
|**cftNotebook** <br/> |1  <br/> |指定した名前と場所を使用してノートブックを作成します。  <br/> |
|**cftFolder** <br/> |2  <br/> |指定した名前と場所を使用してセクション グループを作成します。  <br/> |
|**cftSection** <br/> |3  <br/> |指定した名前と場所を使用してセクションを作成します。  <br/> |
   
## <a name="docklocation"></a>DockLocation
<a name="odc_CreateFileType"> </a>

Window インターフェイスを使用して、OneNote 2013 ウィンドウのドッキング位置を[示](window-interfaces-onenote.md)します。 **DockedLocation プロパティに設定すると**、ウィンドウをドッキングする場所OneNoteします。 この列挙は、2013 年OneNoteです。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**dlDefault** <br/> |-1  <br/> |[OneNoteウィンドウは、デスクトップ上の既定の場所にドッキングされます。  <br/> |
|**dlLeft** <br/> |1  <br/> |ウィンドウOneNoteデスクトップの左側にドッキングされます。  <br/> |
|**dlRight** <br/> |2  <br/> |ウィンドウOneNoteデスクトップの右側にドッキングされます。  <br/> |
|**dlTop** <br/> |3  <br/> |ウィンドウOneNoteデスクトップの上部にドッキングされます。  <br/> |
|**dlBottom** <br/> |4  <br/> |ウィンドウOneNoteデスクトップの下部にドッキングされます。  <br/> |
   
## <a name="filinglocation"></a>FilingLocation
<a name="odc_CreateFileType"> </a>

**SetFilingLocation** メソッドに渡す場合、コンテンツ タイプがファイル に送信される際にファイリング場所が設定されるコンテンツの種類をOneNote。 この列挙は、2013 年OneNoteです。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**flEMail** <br/> |0  <br/> |メール メッセージOutlookする場所を設定します。  <br/> |
|**flContacts** <br/> |1  <br/> |連絡先をOutlookする場所を設定します。  <br/> |
|**flTasks** <br/> |2  <br/> |タスクをOutlookする場所を設定します。  <br/> |
|**flMeetings** <br/> |3  <br/> |会議をOutlookする場所を設定します。  <br/> |
|**flWebContent** <br/> |4  <br/> |コンテンツをInternet Explorerする場所を設定します。  <br/> |
|**flPrintOuts** <br/> |5  <br/> |プリンターからの印刷OneNoteする場所を設定します。  <br/> |
   
## <a name="filinglocationtype"></a>FilingLocationType
<a name="odc_CreateFileType"> </a>

**SetFilingLocation** メソッドに渡された場合、ファイルに送信されるコンテンツのOneNote指定します。 この列挙は、2013 年OneNoteです。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**fltNamedSectionNewPage** <br/> |0  <br/> |指定したセクションの新しいページにファイルするコンテンツを設定します。  <br/> |
|**fltCurrentSectionNewPage** <br/> |1  <br/> |現在のセクションの新しいページにファイルするコンテンツを設定します。  <br/> |
|**fltCurrentPage** <br/> |2  <br/> |現在のページにファイルするコンテンツを設定します。  <br/> |
|**fltNamedPage** <br/> |4  <br/> |指定したページにファイルするコンテンツを設定します。  <br/> |
   
## <a name="hierarchyelement"></a>HierarchyElement
<a name="odc_CreateFileType"> </a>

[IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md)インターフェイスの **TreeDepth** プロパティに割り当てられた場合、クイック ファイリング ダイアログが表示される際に表示する OneNote ツリーの深度を指定します。 **IQuickFilingDialog** オブジェクトの **AddButton** メソッドに渡された場合は、階層内の特定のOneNoteします。 この列挙は、2013 年OneNoteです。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**heNone** <br/> |0  <br/> |要素なしを参照します。  <br/> |
|**heNotebooks** <br/> |1  <br/> |Notebook 要素を参照します。  <br/> |
|**heSectionGroups** <br/> |2  <br/> |セクション グループ要素を参照します。  <br/> |
|**heSections** <br/> |4  <br/> |Section 要素を参照します。  <br/> |
|**hePages** <br/> |8  <br/> |Page 要素を参照します。  <br/> |
   
## <a name="hierarchyscope"></a>HierarchyScope
<a name="odc_HierarchyScope"> </a>

**GetHierarchy** メソッドに渡された場合、ノートブック ノード階層で取得する最低レベルを指定します。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**hsSelf** <br/> |0  <br/> |指定された開始ノードと子孫を取得します。  <br/> |
|**hsChildren** <br/> |1  <br/> |開始ノードの直下の子ノードを取得し、上位または下位のサブセクション グループの子孫を取得します。  <br/> |
|**hsNotebooks** <br/> |2  <br/> |スタート ノードまたはルートの下のすべてのノートブックを取得します。  <br/> |
|**hsSections** <br/> |3  <br/> |開始ノードの下のすべてのセクション (セクション グループとサブセクション グループのセクションを含む) を取得します。  <br/> |
|**hsPages** <br/> |4  <br/> |セクション グループおよびサブセクション グループ内のすべてのページを含む、スタート ノードの下のすべてのページを取得します。  <br/> |
   
## <a name="newpagestyle"></a>NewPageStyle
<a name="odc_HierarchyScope"> </a>

**CreateNewPage メソッドに渡** す場合は、新しいページのスタイルを指定します。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**npsDefault** <br/> |0  <br/> |既定のページ スタイルを持つページを作成します。  <br/> |
|**npsBlankPageWithTitle** <br/> |1  <br/> |タイトルがある空白のページを作成します。  <br/> |
|**npsBlankPageNoTitle** <br/> |2  <br/> |タイトルがない空白のページを作成します。  <br/> |
   
## <a name="notebookfilterouttype"></a>NotebookFilterOutType
<a name="odc_HierarchyScope"> </a>

QFD オブジェクト **の NotebookFilterOut** メソッドに渡す場合は **、QFD** ボックスをレンダリングするときに表示するノートブックを指定します。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**nfoLocal** <br/> |1  <br/> |ローカル ノートブックのみを許可します。  <br/> |
|**nfoNetwork** <br/> |2  <br/> |UNC またはノートブックSharePoint許可します。  <br/> |
|**nfoWeb** <br/> |4  <br/> |ノートブックOneDrive許可します。  <br/> |
|**nfoNoWacUrl** <br/> |8  <br/> |Web クライアントを持つ場所のノートブック。  <br/> |
   
## <a name="pageinfo-updated-for-onenote-2013"></a>PageInfo (2013 OneNote更新)
<a name="odc_PageInfo"> </a>

**GetPageContent** メソッドに渡された場合、ページコンテンツと一緒に返す情報の種類を指定します。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**piBasic** <br/> |0  <br/> |選択マークアップ、バイナリ データ オブジェクトおよびバイナリ データ オブジェクトのファイルの種類を指定せずに、基本的なページ コンテンツのみを返します。 これは、渡す標準の値です。  <br/> |
|**piBinaryData** <br/> |1  <br/> |選択マークアップを含め、すべてのバイナリ データを含むページ コンテンツを返します。  <br/> |
|**piSelection** <br/> |2  <br/> |選択マークアップを持つページ コンテンツを返しますが、バイナリ データはありません。  <br/> |
|**piBinaryDataSelection** <br/> |3  <br/> |選択マークアップとすべてのバイナリ データを含むページ コンテンツを返します。  <br/> |
|**piFileType** <br/> |4  <br/> |バイナリ データ オブジェクトのファイルの種類情報を含むページ コンテンツを返します。  <br/> |
|**piBinaryDataFileType** <br/> |5  <br/> |バイナリ データ オブジェクトおよびバイナリ データ オブジェクトのファイルの種類情報を含むページ コンテンツを返します。  <br/> |
|**piSelectionFileType** <br/> |6  <br/> |バイナリ データの選択マークアップとファイルの種類情報を含むページ コンテンツを返します。  <br/> |
|**piAll** <br/> |7  <br/> |すべてのページ コンテンツを返します。  <br/> |
   
## <a name="publishformat"></a>PublishFormat
<a name="odc_PublishFormat"> </a>

Publish メソッドに **渡す** 場合は、発行されたページが表示される形式を指定します。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**pfOneNote** <br/> |0  <br/> |発行済みページは .one 形式です。  <br/> |
|**pfOneNotePackage** <br/> |1  <br/> |発行済みページは .onepkg 形式です。  <br/> |
|**pfMHTML** <br/> |2  <br/> |発行済みページは .mht 形式です。  <br/> |
|**pfPDF** <br/> |3  <br/> |発行済みページは、.pdf形式です。  <br/> |
|**pfXPS** <br/> |4  <br/> |発行済みページは .xps 形式です。  <br/> |
|**pfWord** <br/> |5  <br/> |発行済みページは、.docまたは.docx形式です。  <br/> |
|**pfEMF** <br/> |6  <br/> |発行されたページは、拡張メタファイル (.emf) 形式です。  <br/> |
|**pfHTML** <br/> |7  <br/> |発行済みページは、.html形式です。 このメンバーは、2013 年OneNoteです。  <br/> |
|**pfOneNote2007** <br/> |8  <br/> |発行済みページは 2007 .one 形式です。 このメンバーは、2013 年OneNoteです。  <br/> |
   
## <a name="recentresulttype"></a>RecentResultType
<a name="odc_RecentResultType"> </a>

**IQuickFilingDialog** オブジェクトの **SetRecentResults** メソッドに渡された場合は、[クイック ファイリング] ダイアログ ボックスが表示される際に表示する最近の結果リストを指定します。 最近の結果リストは、[クイック ファイリング] ダイアログ ボックスOneNote選択した場所のセットを追跡するために使用されます。 2013 OneNote 年 2013 年には、ファイリング、検索、およびリンクアクションを追跡する 3 つの最近の結果リストがあります。 この列挙は、2013 年OneNoteです。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**rrtNone** <br/> |0  <br/> |レンダリングする最近の結果リストを設定します。  <br/> |
|**rrtFiling** <br/> |1  <br/> |レンダリングする "ファイリング" の最近の結果リストを設定します。  <br/> |
|**rrtSearch** <br/> |2  <br/> |レンダリングする "Search" の最近の結果リストを設定します。  <br/> |
|**rrtLinks** <br/> |3  <br/> |レンダリングする "リンク" の最近の結果リストを設定します。  <br/> |
   
## <a name="speciallocation"></a>SpecialLocation
<a name="odc_SpecialLocation"> </a>

**GetSpecialLocation メソッドに渡された** 場合、取得する特別な場所のパスを指定します。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**slBackupFolder** <br/> |0  <br/> |バックアップ フォルダー フォルダーの場所へのパスを取得します。  <br/> |
|**slUnfiledNotesSection** <br/> |1  <br/> |Unfiled Notes フォルダーの場所へのパスを取得します。  <br/> |
|**slDefaultNotebookFolder** <br/> |2  <br/> |既定のノートブック フォルダーの場所へのパスを取得します。  <br/> |
   
## <a name="treecollapsedstatetype"></a>TreeCollapsedStateType
<a name="odc_SpecialLocation"> </a>

**QFD** オブジェクト **の TreeCollapsedState** メソッドに渡す場合は、階層ツリーを展開するか折りたたむかを指定します。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**tcsExpanded** <br/> |0  <br/> |階層ツリーを展開に設定します。  <br/> |
|**tcsCollapsed** <br/> |1  <br/> |階層ツリーを折りたたみに設定します。  <br/> |
   
## <a name="xmlschema-updated-for-onenote-2013"></a>XMLSchema (2013 年OneNote更新)
<a name="odc_SpecialLocation"> </a>

次のいずれかのメソッドに渡す場合は、使用する XML スキーマのバージョンOneNote指定します。
  
- **OneNote15.Application.GetPageContent**
    
- **OneNote15.Application.FindMeta**
    
- **OneNote15.Application.FindPages**
    
- **OneNote15.Application.GetHierarchy**
    
- **OneNote15.Application.GetPageContent**
    
- **OneNote15.Application.UpdateHierarchy**
    
- **OneNote15.Application.UpdatePageContent**
    
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**xs2007** <br/> |0  <br/> |2007 OneNoteを参照します。  <br/> |
|**xs2010** <br/> |1  <br/> |2010 OneNoteを参照します。  <br/> |
|**xs2013** <br/> |2  <br/> |2013 OneNoteを参照します。  <br/> |
|**xsCurrent** <br/> |2  <br/> |現在のバージョンのスキーマをOneNoteします。  <br/> <br/>**注**: ほとんどの場合 **、xsCurrent** を使用することをお勧めしません。これは、将来のバージョンのデバイスとの互換性の問題を引き起こす可能性OneNote。 代わりに、アプリが処理するために構築されたスキーマのバージョン (xs2013 など) を指定します。           |
   
## <a name="see-also"></a>関連項目

- [OneNote 開発者用リファレンス](onenote-developer-reference.md)

