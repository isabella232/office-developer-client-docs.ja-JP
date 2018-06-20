---
title: 列挙体 (OneNote の開発者用リファレンス)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 62912d6e-c39e-4f8b-8cdb-ae9b6376cbc0
description: このトピックでは、OneNote 2013 オブジェクト モデルの列挙体について説明します。
ms.openlocfilehash: ccd75843326ea5942aa80d02246e59e92331a7d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799286"
---
# <a name="enumerations-onenote-developer-reference"></a>列挙体 (OneNote の開発者用リファレンス)

このトピックでは、OneNote 2013 オブジェクト モデルの列挙体について説明します。
  
## <a name="createfiletype"></a>CreateFileType
<a name="odc_CreateFileType"> </a>

**OpenHierarchy**メソッドに渡されるとき、その場合は、メソッドに渡されるパスが存在しない場合、作成するオブジェクトの種類を指定します。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**cftNone** <br/> |0  <br/> |新しいオブジェクトは作成されません。  <br/> |
|**cftNotebook** <br/> |1  <br/> |指定した名前と場所を使用してノートブックを作成します。  <br/> |
|**cftFolder** <br/> |2  <br/> |指定した名前と場所を使用してセクション グループを作成します。  <br/> |
|**cftSection** <br/> |3  <br/> |指定した名前と場所を使用してセクションを作成します。  <br/> |
   
## <a name="docklocation"></a>DockLocation
<a name="odc_CreateFileType"> </a>

[ウィンドウ](window-interfaces-onenote.md)のインターフェイスを使用して OneNote 2013 ウィンドウのドッキング位置を示します。 **DockedLocation**に設定すると、プロパティは、OneNote ウィンドウをドッキングする位置を指定します。 この列挙体は、OneNote の 2013年の新機能です。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**dlDefault** <br/> |-1  <br/> |OneNote ウィンドウは、デスクトップの既定の場所に固定されます。  <br/> |
|**dlLeft** <br/> |1  <br/> |OneNote ウィンドウはデスクトップの左側にドッキングされます。  <br/> |
|**dlRight** <br/> |2  <br/> |OneNote ウィンドウはデスクトップの右側にドッキングされます。  <br/> |
|**dlTop** <br/> |3  <br/> |OneNote ウィンドウは、デスクトップの上部にドッキングされます。  <br/> |
|**dlBottom** <br/> |4  <br/> |OneNote ウィンドウは、デスクトップの下部にドッキングされます。  <br/> |
   
## <a name="filinglocation"></a>FilingLocation
<a name="odc_CreateFileType"> </a>

**SetFilingLocation**メソッドに渡されると、設定を指定コンテンツの種類ファイルの場所のコンテンツ タイプは、OneNote に送信されるとします。 この列挙体は、OneNote の 2013年の新機能です。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**flEMail** <br/> |0  <br/> |Outlook 電子メール メッセージの保存場所を設定します。  <br/> |
|**flContacts** <br/> |1  <br/> |Outlook の連絡先の保存場所を設定します。  <br/> |
|**flTasks** <br/> |2  <br/> |Outlook からのタスクの保存場所を設定します。  <br/> |
|**flMeetings** <br/> |3  <br/> |Outlook の会議の保存場所を設定します。  <br/> |
|**flWebContent** <br/> |4  <br/> |Internet Explorer のコンテンツの保存場所を設定します。  <br/> |
|**flPrintOuts** <br/> |5  <br/> |OneNote プリンターから印刷物の保存場所を設定します。  <br/> |
   
## <a name="filinglocationtype"></a>FilingLocationType
<a name="odc_CreateFileType"> </a>

**SetFilingLocation**メソッドに渡された場合は、OneNote に送信されるコンテンツの保存場所を指定します。 この列挙体は、OneNote の 2013年の新機能です。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**fltNamedSectionNewPage** <br/> |0  <br/> |指定のセクションの新しいページに提出される内容を設定します。  <br/> |
|**fltCurrentSectionNewPage** <br/> |1  <br/> |現在のセクションの新しいページに提出される内容を設定します。  <br/> |
|**fltCurrentPage** <br/> |2  <br/> |現在のページに提出される内容を設定します。  <br/> |
|**fltNamedPage** <br/> |4  <br/> |指定したページに提出される内容を設定します。  <br/> |
   
## <a name="hierarchyelement"></a>HierarchyElement
<a name="odc_CreateFileType"> </a>

[IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md)インターフェイスの**TreeDepth**プロパティに割り当てると、クイック ファイリング ダイアログ ボックスが表示されるときに表示するのには、OneNote のツリーの深さを指定します。 **IQuickFilingDialog**オブジェクトの**AddButton**メソッドに渡された場合は、OneNote の階層内の特定の要素を参照します。 この列挙体は、OneNote の 2013年の新機能です。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**heNone** <br/> |0  <br/> |要素を参照します。  <br/> |
|**heNotebooks** <br/> |1  <br/> |ノートブックの要素を参照します。  <br/> |
|**heSectionGroups** <br/> |2  <br/> |セクション グループの各要素を参照します。  <br/> |
|**heSections** <br/> |4  <br/> |セクションの要素を参照します。  <br/> |
|**hePages** <br/> |8  <br/> |ページ要素を参照します。  <br/> |
   
## <a name="hierarchyscope"></a>HierarchyScope
<a name="odc_HierarchyScope"> </a>

**GetHierarchy**メソッドに渡されるときは、ノートブックのノード階層を取得する最も低いレベルを指定します。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**hsSelf** <br/> |0  <br/> |取得の開始] ノードだけが指定されていない子.  <br/> |
|**hsChildren** <br/> |1  <br/> |サブセクションの上位または下位グループの直下の子ノードの [開始] ノードとなしの子を取得します。  <br/> |
|**hsNotebooks** <br/> |2  <br/> |[開始] ノードまたはルートの下のすべてのノートブックを取得します。  <br/> |
|**hsSections** <br/> |3  <br/> |グループのセクションとサブセクションのグループ内のセクションを含む、開始ノードの下のすべてのセクションを取得します。  <br/> |
|**hsPages** <br/> |4  <br/> |グループのセクションとサブセクションのグループのすべてのページを含む、開始ノードの下のすべてのページを取得します。  <br/> |
   
## <a name="newpagestyle"></a>NewPageStyle
<a name="odc_HierarchyScope"> </a>

**CreateNewPage**メソッドに渡されると、新しいページのスタイルを指定します。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**npsDefault** <br/> |0  <br/> |ページの既定のスタイルを持つページを作成します。  <br/> |
|**npsBlankPageWithTitle** <br/> |1  <br/> |タイトルを空白のページを作成します。  <br/> |
|**npsBlankPageNoTitle** <br/> |2  <br/> |タイトルがまったくない空白のページを作成します。  <br/> |
   
## <a name="notebookfilterouttype"></a>NotebookFilterOutType
<a name="odc_HierarchyScope"> </a>

**QFD**オブジェクトの**NotebookFilterOut**メソッドに渡されるときは、QFD のボックスが表示されるときに表示するには、どのようなノートブックを指定します。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**nfoLocal** <br/> |1  <br/> |ローカル ノートブックのみを許可します。  <br/> |
|**nfoNetwork** <br/> |2  <br/> |UNC または SharePoint のノートブックを使用できます。  <br/> |
|**nfoWeb** <br/> |4  <br/> |OneDrive のノートブックを使用できます。  <br/> |
|**nfoNoWacUrl** <br/> |8  <br/> |Web クライアントがない場所で、ノート パソコン。  <br/> |
   
## <a name="pageinfo-updated-for-onenote-2013"></a>PageInfo の (OneNote 2013 の更新)
<a name="odc_PageInfo"> </a>

**GetPageContent**メソッドに渡されると、ページのコンテンツを取得する情報の種類を指定します。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**piBasic** <br/> |0  <br/> |のみ基本的なページのコンテンツ、マークアップを選択せず、ファイルの種類のオブジェクトのバイナリ データとバイナリ データ オブジェクトを返します。 これは、標準的な値を渡すことです。  <br/> |
|**piBinaryData** <br/> |1  <br/> |返します。 ページのコンテンツのすべてのバイナリ データを持つが、選択範囲のマークアップがないと。  <br/> |
|**piSelection** <br/> |2  <br/> |返します。 ページのコンテンツ、マークアップの選択ですが、バイナリ データがありません。  <br/> |
|**piBinaryDataSelection** <br/> |3  <br/> |返します。 ページのマークアップを選択し、すべてのバイナリ データのコンテンツ。  <br/> |
|**piFileType** <br/> |4  <br/> |返しますは、バイナリ データ オブジェクトの型情報をファイルのコンテンツをページします。  <br/> |
|**piBinaryDataFileType** <br/> |5  <br/> |返すは、オブジェクトのバイナリ データとバイナリ データ オブジェクトの型情報をファイルのコンテンツをページします。  <br/> |
|**piSelectionFileType** <br/> |6  <br/> |返しますは、バイナリ データの選択範囲マークアップとファイルの種類の情報を持つコンテンツをページします。  <br/> |
|**piAll** <br/> |7  <br/> |ページのすべてのコンテンツを返します。  <br/> |
   
## <a name="publishformat"></a>PublishFormat
<a name="odc_PublishFormat"> </a>

**Publish**メソッドに渡されると、発行されたページを表示する形式を指定します。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**pfOneNote** <br/> |0  <br/> |.One の形式では、公開したページです。  <br/> |
|**pfOneNotePackage** <br/> |1  <br/> |.Onepkg 形式では、公開したページです。  <br/> |
|**pfMHTML** <br/> |2  <br/> |.Mht 形式では、公開したページです。  <br/> |
|**pfPDF** <br/> |3  <br/> |.Pdf 形式では、公開したページです。  <br/> |
|**pfXPS** <br/> |4  <br/> |.Xps 形式では、公開したページです。  <br/> |
|**pfWord** <br/> |5  <br/> |.Doc または .docx 形式では、公開したページです。  <br/> |
|**pfEMF** <br/> |6  <br/> |拡張メタファイル (.emf) 形式では、公開したページです。  <br/> |
|**pfHTML** <br/> |7  <br/> |.Html 形式では、公開したページです。 このメンバーは、OneNote の 2013年の新機能です。  <br/> |
|**pfOneNote2007** <br/> |8  <br/> |2007 .one の形式では、公開されているページです。 このメンバーは、OneNote の 2013年の新機能です。  <br/> |
   
## <a name="recentresulttype"></a>RecentResultType
<a name="odc_RecentResultType"> </a>

**IQuickFilingDialog**オブジェクトの**SetRecentResults**メソッドに渡された場合は、クイック ファイリング ダイアログ ボックスが表示されるときに表示するのにはどのような最近の結果リストを指定します。 クイック ファイリング ダイアログ ボックスでユーザーが選択した OneNote の保存場所の設定を追跡するために最新の結果の一覧表示されます。 2013 の OneNote で整理、検索、およびアクションのリンクを追跡する 3 つの最近の結果リストがあります。 この列挙体は、OneNote の 2013年の新機能です。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**rrtNone** <br/> |0  <br/> |最近の結果リストを表示するのには設定されません。  <br/> |
|**rrtFiling** <br/> |1  <br/> |レンダリングする「ファイリング」最近の結果リストをを設定します。  <br/> |
|**rrtSearch** <br/> |2  <br/> |表示する [検索] の最近の結果リストを設定します。  <br/> |
|**rrtLinks** <br/> |3  <br/> |表示する [リンク] の最近の結果リストを設定します。  <br/> |
   
## <a name="speciallocation"></a>SpecialLocation
<a name="odc_SpecialLocation"> </a>

**GetSpecialLocation**メソッドに渡されると、取得する特別な場所のパスを指定します。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**slBackupFolder** <br/> |0  <br/> |バックアップ フォルダーのフォルダーの場所へのパスを取得します。  <br/> |
|**slUnfiledNotesSection** <br/> |1  <br/> |落書きノート フォルダーの場所へのパスを取得します。  <br/> |
|**slDefaultNotebookFolder** <br/> |2  <br/> |既定のノートブック フォルダーの場所へのパスを取得します。  <br/> |
   
## <a name="treecollapsedstatetype"></a>TreeCollapsedStateType
<a name="odc_SpecialLocation"> </a>

**QFD**オブジェクトの**TreeCollapsedState**メソッドに渡された場合は、階層ツリーを展開または折りたたまれているかどうかを指定します。 
  
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**tcsExpanded** <br/> |0  <br/> |階層ツリーを展開するを設定します。  <br/> |
|**tcsCollapsed** <br/> |1  <br/> |階層ツリーが折りたたまれているを設定します。  <br/> |
   
## <a name="xmlschema-updated-for-onenote-2013"></a>XMLSchema を (OneNote 2013 の更新)
<a name="odc_SpecialLocation"> </a>

次の方法のいずれかに渡されると、使用する OneNote の XML スキーマのバージョンを指定します。
  
- **OneNote15.Application.GetPageContent**
    
- **OneNote15.Application.FindMeta**
    
- **OneNote15.Application.FindPages**
    
- **OneNote15.Application.GetHierarchy**
    
- **OneNote15.Application.GetPageContent**
    
- **OneNote15.Application.UpdateHierarchy**
    
- **OneNote15.Application.UpdatePageContent**
    
|**メンバー**|**値**|**説明**|
|:-----|:-----|:-----|
|**xs2007** <br/> |0  <br/> |OneNote 2007 のスキーマを参照します。  <br/> |
|**xs2010** <br/> |1  <br/> |OneNote 2010 のスキーマを参照します。  <br/> |
|**xs2013** <br/> |2  <br/> |OneNote 2013 スキーマを参照します。  <br/> |
|**xsCurrent** <br/> |2  <br/> |OneNote の現在のバージョンのスキーマを参照します。  <br/> <br/>**注**: お勧めしません、ほとんどの場合**xsCurrent**を使用して OneNote の将来のバージョンとの互換性の問題が生じるようです。 代わりにアプリは、xs2013 のように、処理するために構築されたスキーマのバージョンを指定します。           |
   
## <a name="see-also"></a>関連項目

- [OneNote の開発者用リファレンス](onenote-developer-reference.md)

