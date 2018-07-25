---
title: InfoPath 2003 オブジェクト モデルを使用してフォーム イベントに応答する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- フォーム テンプレート [infopath 2007],イベントに応答する,InfoPath 2003 互換のフォーム テンプレート,フォーム イベントに応答する
localization_priority: Normal
ms.assetid: 59e9c1ed-32a8-4bcd-bdfc-9aa568a34d2a
description: ユーザーがフォームに入力する際に発生する各種イベントに応答するコードを書くことができます。InfoPath 内でイベントの作業を実行するには、InfoPath デザイン モードでイベント ハンドラーを作成します。
ms.openlocfilehash: dff7b4f1657b7d1450d8b345521a747c0594462b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799122"
---
# <a name="respond-to-form-events-using-the-infopath-2003-object-model"></a>InfoPath 2003 オブジェクト モデルを使用してフォーム イベントに応答する

ユーザーがフォームに入力する際に発生する各種イベントに応答するコードを書くことができます。InfoPath 内でイベントの作業を実行するには、InfoPath デザイン モードでイベント ハンドラーを作成します。
  
InfoPath イベント ハンドラーは、InfoPath デザイン モードで作成してください。これは、InfoPath 2003 互換のオブジェクト モデルを使用する際、InfoPath が、イベント ハンドラーを識別およびシンクするために、フォームのコード ファイル (FormCode.cs または FormCode.vb) 内で、自動的に正しい宣言を追加し、属性 ([InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) を適用するためです。イベント ハンドラーを作成した後は、フォームのコード ファイル内で宣言と属性を変更しないでください。 
  
InfoPath イベント ハンドラーの作成については、「[InfoPath 2003 オブジェクト モデルを使用してイベント ハンドラーを追加する方法](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)」を参照してください。
  
## <a name="overview-of-the-event-objects"></a>イベント オブジェクトの概要

InfoPath 2003 互換オブジェクト モデルには、[Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 名前空間で公開される 9 つのイベント オブジェクトが実装されています。次の表には、それぞれの InfoPath イベント オブジェクト、関連付けられているイベント ハンドラー、およびそれらが提供する機能の説明が一覧表示されています。 
  
|**名前**|**イベント ハンドラー**|**説明**|
|:-----|:-----|:-----|
|[DataDOMEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.aspx) <br/> |[OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx) <br/> [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) , [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) <br/> |XML Document Object Model (DOM) の変更中に、フォームの基になる XML ドキュメントへの参照、リターン状態、およびその他の XML ノードに関する情報を含むプロパティを返します。エラーを発生させるメソッドも含みます。  <br/> |
|[DocActionEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocActionEvent.aspx) <br/> |[OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) <br/> |フォーム領域内でのボタン クリック中に、フォームの基になる XML ドキュメントへの参照、リターン状態、およびソース XML ノードを返します。  <br/> |
|[DocContextChangeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocContextChangeEvent.aspx) <br/> |[OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx) <br/> |フォームの基になる XML ドキュメントの現在のコンテキストである XML Document Object Model (DOM) ノードに関する情報を返します。  <br/> |
|[DocEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocEvent.aspx) <br/> |[OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx) , [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) <br/> |ビューの切り替えやフォームの結合操作中に、フォームの基になる XML ドキュメントへの参照を返します。  <br/> |
|[DocReturnEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocReturnEvent.aspx) <br/> |[OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) , [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) <br/> |フォームの読み込みまたは送信中に、フォームの基になる XML ドキュメントへの参照と、リターン状態を返します。  <br/> |
|[MergeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MergeEvent.aspx) <br/> |[OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) <br/> |フォームの基となる XML ドキュメントをプログラムから操作したり、結合するファイルの数などの結合プロパティを調べたりするために、 **OnMergeRequest** イベント中に使用できるプロパティとメソッドを返します。  <br/> |
|[SaveEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SaveEvent.aspx) <br/> |[OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) <br/> |フォームの基となる XML ドキュメントをプログラムから操作したり、保存プロパティを指定したり、保存操作を実行したりするために、 **OnSaveRequest** イベント ハンドラーからの保存操作中に使用できるプロパティとメソッドの数を返します。  <br/> |
|[SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) <br/> |[OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |デジタル署名に追加データを追加するために使用します。  <br/> |
|[VersionUpgradeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.VersionUpgradeEvent.aspx) <br/> |[OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) <br/> |バージョン アップグレード操作中に、フォームの基となる XML ドキュメントへの参照、リターン状態、およびドキュメントとソリューションのバージョン番号を返します。  <br/> |
   
## <a name="using-the-event-objects"></a>イベント オブジェクトの使用

イベント ハンドラーを作成する際、InfoPath は、プロジェクトのフォーム コード ファイル (FormCode.cs または FormCode.vb) 内でイベント ハンドラーの宣言を作成します。イベント ハンドラーの宣言内で、InfoPath は、イベント ハンドラーに渡されるパラメーターの名前として **e** を使用します。このパラメーターには、イベント ハンドラーに関連付けられるイベント オブジェクトが含まれます。 
  
たとえば、[ **開発**] タブの [ **OnLoad イベント**] をクリックすることで、デザイン モードで **OnLoad** イベントのイベント ハンドラーを作成する際、InfoPath は、 **DocReturnEvent** オブジェクトを受け取るイベント ハンドラーの宣言をフォーム コード ファイルに追加し、以下のイベント ハンドラー宣言にコードを追加するためのコード エディターを開きます。 
  
```cs
// The following function handler is created by Microsoft Office 
// InfoPath. Do not modify the type or number of arguments.
[InfoPathEventHandler(EventType=InfoPathEventType.OnLoad)]
public void FormEvents_OnLoad(DocReturnEvent e)
{
   // Write your code here.
}
```

```vb
' The following function handler is created by Microsoft Office 
' InfoPath. Do not modify the type or number of arguments.
<InfoPathEventHandler(EventType:=InfoPathEventType.OnLoad)> _
Public Sub FormEvents_OnLoad(ByVal e As DocReturnEvent)
   ' Write your code here.
End Sub
```

イベント ハンドラーのコードを書く際、 **e** パラメーターを通じて渡されるイベント オブジェクトによって実装されるプロパティとメソッドを使用できます。たとえば、以下の **OnBeforeChange** イベント ハンドラーでは、 [DataDOMEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.NewValue.aspx) イベント オブジェクトの **NewValue** プロパティを使用して、変更されたフィールドの値が確認されます。それが空白の場合は、 [DataDOMEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnMessage.aspx) イベント オブジェクトの **ReturnMessage** プロパティを使用して、ユーザーに対してダイアログ ボックスでエラーが表示され、 [ReturnStatus](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnStatus.aspx) プロパティが **false** に設定されて、ユーザーが行った変更が受け入れられないことを示します。
  
```cs
[InfoPathEventHandler(MatchPath="/my:myFields/my:field1", 
    EventType=InfoPathEventType.OnBeforeChange)]
public void field1_OnBeforeChange(DataDOMEvent e)
{
   // Determine whether there is a new value.
   if ((string)e.NewValue == "")
   {
      // The value is blank, so display an error message and roll
      // back the changes.
      e.ReturnMessage = "You must supply a value for this field.";
      e.ReturnStatus = false;
      return;
   }
}
```

```vb
<InfoPathEventHandler(MatchPath:="/my:myFields/my:field1", _ EventType:=InfoPathEventType.OnBeforeChange)> _
Public Sub field1_OnBeforeChange(ByVal e As DataDOMEvent)
   ' Determine whether there is a new value.
   If (e.NewValue = "") Then
      ' The value is blank, so display an error message and roll back
      ' the changes.
      e.ReturnMessage = "You must supply a value for this field."
      e.ReturnStatus = False
      Return
   End If
End Sub
```

> [!NOTE]
> InfoPath 2003 互換オブジェクト モデルのそれぞれの InfoPath イベント オブジェクトは、異なるプロパティとメソッドを実装します。特定のイベント オブジェクトに関する詳細については、前に示したイベント オブジェクトの表でそれぞれのオブジェクトをクリックして参照してください。 
  

