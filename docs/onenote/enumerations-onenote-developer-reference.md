---
title: 列挙体 (OneNote 開発者用リファレンス)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 62912d6e-c39e-4f8b-8cdb-ae9b6376cbc0
description: このトピックでは、OneNote 2013 オブジェクトモデルの列挙体について説明します。
ms.openlocfilehash: 3338e444e5b0bfd0239e363c3161aeb1914b2d53
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299868"
---
# <a name="enumerations-onenote-developer-reference"></a>列挙体 (OneNote 開発者用リファレンス)

このトピックでは、OneNote 2013 オブジェクトモデルの列挙体について説明します。
  
## <a name="createfiletype"></a>createfiletype
<a name="odc_CreateFileType"> </a>

**openhierarchy**メソッドに渡された場合、メソッドに渡されたパスが存在しない場合は、作成するオブジェクトの種類を指定します (存在する場合)。 
  
|**Member**|**値**|**説明**|
|:-----|:-----|:-----|
|**cftnone** <br/> |.0  <br/> |新しいオブジェクトを作成しません。  <br/> |
|**cftnotebook** <br/> |1-d  <br/> |指定された名前と場所を使用してノートブックを作成します。  <br/> |
|**cftfolder** <br/> |pbm-2  <br/> |指定された名前と場所を使用して、セクショングループを作成します。  <br/> |
|**cftsection** <br/> |1/3  <br/> |指定された名前と場所を使用してセクションを作成します。  <br/> |
   
## <a name="docklocation"></a>DockLocation
<a name="odc_CreateFileType"> </a>

[window](window-interfaces-onenote.md)インターフェイスを使用して OneNote 2013 ウィンドウのドッキング場所を示します。 **docの location**プロパティに設定されている場合は、OneNote ウィンドウをドッキングする位置を指定します。 この列挙は OneNote 2013 で新しく追加されたものです。 
  
|**Member**|**値**|**説明**|
|:-----|:-----|:-----|
|**dldefault** <br/> |-1  <br/> |OneNote ウィンドウは、デスクトップ上の既定の場所に固定されます。  <br/> |
|**dlleft** <br/> |1-d  <br/> |OneNote ウィンドウは、デスクトップの左側に固定されます。  <br/> |
|**dlright** <br/> |pbm-2  <br/> |OneNote ウィンドウは、デスクトップの右側に固定されます。  <br/> |
|**dltop** <br/> |1/3  <br/> |OneNote ウィンドウは、デスクトップの上部に固定されています。  <br/> |
|**dlbottom** <br/> |2/4  <br/> |OneNote ウィンドウは、デスクトップの下部に固定されています。  <br/> |
   
## <a name="filinglocation"></a>filinglocation
<a name="odc_CreateFileType"> </a>

**setfilinglocation**メソッドに渡されると、コンテンツタイプが OneNote に送信されるときに、ファイリングの場所に設定されるコンテンツの種類を指定します。 この列挙は OneNote 2013 で新しく追加されたものです。 
  
|**Member**|**値**|**説明**|
|:-----|:-----|:-----|
|**flemail** <br/> |.0  <br/> |Outlook 電子メールメッセージがファイリングされる場所を設定します。  <br/> |
|**flcontacts** <br/> |1-d  <br/> |Outlook の連絡先をファイリングする場所を設定します。  <br/> |
|**fltasks** <br/> |pbm-2  <br/> |Outlook のタスクをファイリングする場所を設定します。  <br/> |
|**flmeetings** <br/> |1/3  <br/> |Outlook 会議がファイリングされる場所を設定します。  <br/> |
|**flwebcontent** <br/> |2/4  <br/> |Internet Explorer の内容がファイリングされる場所を設定します。  <br/> |
|**flprintouts** <br/> |5  <br/> |OneNote プリンターからの印刷物がファイリングされる場所を設定します。  <br/> |
   
## <a name="filinglocationtype"></a>FilingLocationType
<a name="odc_CreateFileType"> </a>

**setfilinglocation**メソッドに渡されると、OneNote に送信されるコンテンツが保存される場所を指定します。 この列挙は OneNote 2013 で新しく追加されたものです。 
  
|**Member**|**値**|**説明**|
|:-----|:-----|:-----|
|**fltnamedsectionnewpage** <br/> |.0  <br/> |指定したセクションの新しいページにファイリングするコンテンツを設定します。  <br/> |
|**fltcurrentsectionnewpage** <br/> |1-d  <br/> |現在のセクションの新しいページにファイリングするコンテンツを設定します。  <br/> |
|**fltCurrentPage** <br/> |pbm-2  <br/> |現在のページにファイリングするコンテンツを設定します。  <br/> |
|**fltnamedpage** <br/> |2/4  <br/> |指定したページにファイリングされるコンテンツを設定します。  <br/> |
   
## <a name="hierarchyelement"></a>HierarchyElement
<a name="odc_CreateFileType"> </a>

[iquickfilingdialog](quick-filing-dialog-box-interfaces-onenote.md)インターフェイスの**treedepth**プロパティに割り当てられている場合、クイックファイリングダイアログがレンダリングされるときに表示する OneNote ツリーの深さを指定します。 **iquickfilingdialog**オブジェクトの**addbutton**メソッドに渡されると、OneNote 階層の特定の要素を参照します。 この列挙は OneNote 2013 で新しく追加されたものです。 
  
|**Member**|**値**|**説明**|
|:-----|:-----|:-----|
|**heNone** <br/> |.0  <br/> |要素を参照しません。  <br/> |
|**henotebooks** <br/> |1-d  <br/> |ノートブックの要素を参照します。  <br/> |
|**heSectionGroups** <br/> |pbm-2  <br/> |セクショングループ要素を参照します。  <br/> |
|**heSections** <br/> |2/4  <br/> |Section 要素を参照します。  <br/> |
|**hepages** <br/> |~  <br/> |ページ要素を参照します。  <br/> |
   
## <a name="hierarchyscope"></a>HierarchyScope
<a name="odc_HierarchyScope"> </a>

**GetHierarchy**メソッドに渡されたときに、ノートブックノード階層で取得する最下位のレベルを指定します。 
  
|**Member**|**値**|**説明**|
|:-----|:-----|:-----|
|**hsself** <br/> |.0  <br/> |指定された開始ノードのみを取得し、子孫は取得しません。  <br/> |
|**hsChildren** <br/> |1-d  <br/> |開始ノードの直下の子ノードを取得し、上位または下位のサブセクショングループに子孫は含まれません。  <br/> |
|**hsnotebooks** <br/> |pbm-2  <br/> |開始ノードまたはルートの下にあるすべてのノートブックを取得します。  <br/> |
|**hssections** <br/> |1/3  <br/> |セクショングループとサブセクショングループのセクションを含む、開始ノードの下にあるすべてのセクションを取得します。  <br/> |
|**hspages** <br/> |2/4  <br/> |セクショングループとサブセクショングループ内のすべてのページを含む、開始ノードの下にあるすべてのページを取得します。  <br/> |
   
## <a name="newpagestyle"></a>newpagestyle
<a name="odc_HierarchyScope"> </a>

**CreateNewPage**メソッドに渡されると、新しいページのスタイルを指定します。 
  
|**Member**|**値**|**説明**|
|:-----|:-----|:-----|
|**npsdefault** <br/> |.0  <br/> |既定のページスタイルを持つページを作成します。  <br/> |
|**nps空白ページ withtitle** <br/> |1-d  <br/> |タイトルを含む空白のページを作成します。  <br/> |
|**nps空白 pagpagtitle** <br/> |pbm-2  <br/> |タイトルのない空白のページを作成します。  <br/> |
   
## <a name="notebookfilterouttype"></a>NotebookFilterOutType
<a name="odc_HierarchyScope"> </a>

**qfd**オブジェクトの**NotebookFilterOut**メソッドに渡されたときに、qfd ボックスがレンダリングされるときに表示するノートブックを指定します。 
  
|**Member**|**値**|**説明**|
|:-----|:-----|:-----|
|**n¥ local** <br/> |1-d  <br/> |ローカルノートブックのみを許可します。  <br/> |
|**nfoNetwork** <br/> |pbm-2  <br/> |UNC または SharePoint ノートブックを許可します。  <br/> |
|**n・ web** <br/> |2/4  <br/> |OneDrive ノートブックを許可します。  <br/> |
|**nfonowacurl** <br/> |~  <br/> |web クライアントを持たない場所にあるノートブック。  <br/> |
   
## <a name="pageinfo-updated-for-onenote-2013"></a>PageInfo (OneNote 2013 用に更新)
<a name="odc_PageInfo"> </a>

**GetPageContent**メソッドに渡されたときに、ページコンテンツと共に返す情報の種類を指定します。 
  
|**Member**|**値**|**説明**|
|:-----|:-----|:-----|
|**pibasic** <br/> |.0  <br/> |選択マークアップを含まない基本的なページコンテンツのみを返します。バイナリデータオブジェクトおよびバイナリデータオブジェクトのファイルの種類を指定します。 これは、渡す標準的な値です。  <br/> |
|**pibinarydata** <br/> |1-d  <br/> |選択マークがなく、すべてのバイナリデータを含むページコンテンツを返します。  <br/> |
|**piselection** <br/> |pbm-2  <br/> |選択マークアップを使用して、バイナリデータを持たないページコンテンツを返します。  <br/> |
|**pibinarydataselection** <br/> |1/3  <br/> |選択マークアップとすべてのバイナリデータを使用してページコンテンツを返します。  <br/> |
|**piFileType** <br/> |2/4  <br/> |バイナリデータオブジェクトのファイルタイプ情報を持つページコンテンツを返します。  <br/> |
|**pibinarydatafiletype** <br/> |5  <br/> |binary data オブジェクトおよび binary data オブジェクトのファイルの種類情報を使用してページの内容を返します。  <br/> |
|**piselectionfiletype** <br/> |シックス  <br/> |バイナリデータの選択マークアップとファイルの種類の情報を使用してページコンテンツを返します。  <br/> |
|**piall** <br/> |7  <br/> |すべてのページコンテンツを返します。  <br/> |
   
## <a name="publishformat"></a>publishformat
<a name="odc_PublishFormat"> </a>

**Publish**メソッドに渡されると、発行されたページの表示形式を指定します。 
  
|**Member**|**値**|**説明**|
|:-----|:-----|:-----|
|**pfOneNote** <br/> |.0  <br/> |発行されたページは、. 1 の形式です。  <br/> |
|**pティー/パッケージ** <br/> |1-d  <br/> |公開されたページは. onepkg 形式です。  <br/> |
|**pfmhtml** <br/> |pbm-2  <br/> |公開されたページは、.mht 形式です。  <br/> |
|**pfpdf** <br/> |1/3  <br/> |発行されたページは .pdf 形式です。  <br/> |
|**pfxps** <br/> |2/4  <br/> |発行されたページは、.xps 形式です。  <br/> |
|**pfword** <br/> |5  <br/> |発行されたページは .doc または .docx 形式です。  <br/> |
|**pfEMF** <br/> |シックス  <br/> |公開されたページは、拡張メタファイル (.emf) 形式になっています。  <br/> |
|**pfhtml** <br/> |7  <br/> |発行されたページは .html 形式です。 このメンバーは OneNote 2013 で新しく追加されたものです。  <br/> |
|**pfOneNote2007** <br/> |~  <br/> |公開されたページは、2007の1つの形式になっています。 このメンバーは OneNote 2013 で新しく追加されたものです。  <br/> |
   
## <a name="recentresulttype"></a>RecentResultType
<a name="odc_RecentResultType"> </a>

**iquickfilingdialog**オブジェクトの**SetRecentResults**メソッドに渡されると、[クイックファイリング] ダイアログボックスを表示したときに表示される最近の結果の一覧を指定します。 最近の結果リストは、ユーザーが [クイックファイリング] ダイアログボックスで選択した OneNote の場所のセットを追跡するために使用されます。 OneNote 2013 には、ファイリング、検索、リンクアクションを追跡する3つの最近の結果リストがあります。 この列挙は OneNote 2013 で新しく追加されたものです。 
  
|**Member**|**値**|**説明**|
|:-----|:-----|:-----|
|**rrtnone** <br/> |.0  <br/> |レンダリングされる最新の結果リストがないように設定します。  <br/> |
|**rrtfiling** <br/> |1-d  <br/> |表示される "最近の" 結果リストの "ファイリング" を設定します。  <br/> |
|**rrtsearch** <br/> |pbm-2  <br/> |レンダリングされる "最近の検索結果" リストを設定します。  <br/> |
|**rrtlinks** <br/> |1/3  <br/> |レンダリングされる "最近の結果" リンクを設定します。  <br/> |
   
## <a name="speciallocation"></a>SpecialLocation
<a name="odc_SpecialLocation"> </a>

**GetSpecialLocation**メソッドに渡されると、取得する特別な場所のパスを指定します。 
  
|**Member**|**値**|**説明**|
|:-----|:-----|:-----|
|**slbackupfolder** <br/> |.0  <br/> |バックアップフォルダーフォルダーの場所へのパスを取得します。  <br/> |
|**slUnfiledNotesSection** <br/> |1-d  <br/> |落書きノートフォルダーの場所へのパスを取得します。  <br/> |
|**slDefaultNotebookFolder** <br/> |pbm-2  <br/> |既定のノートブックフォルダーの場所へのパスを取得します。  <br/> |
   
## <a name="treecollapsedstatetype"></a>TreeCollapsedStateType
<a name="odc_SpecialLocation"> </a>

**qfd**オブジェクトの**TreeCollapsedState**メソッドに渡された場合、階層ツリーを展開するか折りたたむかを指定します。 
  
|**Member**|**値**|**説明**|
|:-----|:-----|:-----|
|**tcsexpanded あります** <br/> |.0  <br/> |階層ツリーを展開済みに設定します。  <br/> |
|**tcscollapsed** <br/> |1-d  <br/> |階層ツリーを折りたたみに設定します。  <br/> |
   
## <a name="xmlschema-updated-for-onenote-2013"></a>XMLSchema (OneNote 2013 用に更新)
<a name="odc_SpecialLocation"> </a>

次のいずれかのメソッドに渡された場合は、使用する OneNote XML スキーマのバージョンを指定します。
  
- **OneNote15 GetPageContent**
    
- **OneNote15 メタ**
    
- **OneNote15 ページ**
    
- **OneNote15 GetHierarchy**
    
- **OneNote15 GetPageContent**
    
- **OneNote15 階層**
    
- **OneNote15 UpdatePageContent**
    
|**Member**|**値**|**説明**|
|:-----|:-----|:-----|
|**xs2007** <br/> |.0  <br/> |OneNote 2007 スキーマを参照します。  <br/> |
|**xs2010** <br/> |1-d  <br/> |OneNote 2010 スキーマを参照します。  <br/> |
|**xs2013** <br/> |pbm-2  <br/> |OneNote 2013 スキーマを参照します。  <br/> |
|**xscurrent** <br/> |pbm-2  <br/> |現在の OneNote のバージョンのスキーマを参照します。  <br/> <br/>**注**: ほとんどの場合、 **xscurrent**を使用することはお勧めしません。今後のバージョンの OneNote での互換性の問題が発生する可能性があります。 代わりに、xs2013 のように、アプリが処理するために作成されたスキーマのバージョンを指定します。           |
   
## <a name="see-also"></a>関連項目

- [OneNote の開発者用リファレンス](onenote-developer-reference.md)

