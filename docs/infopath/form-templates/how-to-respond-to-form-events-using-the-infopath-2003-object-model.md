---
title: フォーム、InfoPath 2003 オブジェクト モデルを使用してイベントに応答します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- form templates [infopath 2007], responding to events,InfoPath 2003-compatible form templates, responding to form events
localization_priority: Normal
ms.assetid: 59e9c1ed-32a8-4bcd-bdfc-9aa568a34d2a
description: ユーザーがフォームに入力する際に発生する各種イベントに応答するコードを書くことができます。InfoPath 内でイベントの作業を実行するには、InfoPath デザイン モードでイベント ハンドラーを作成します。
ms.openlocfilehash: dff7b4f1657b7d1450d8b345521a747c0594462b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799122"
---
# <a name="respond-to-form-events-using-the-infopath-2003-object-model"></a><span data-ttu-id="792d9-105">フォーム、InfoPath 2003 オブジェクト モデルを使用してイベントに応答します。</span><span class="sxs-lookup"><span data-stu-id="792d9-105">Respond to Form Events Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="792d9-p102">ユーザーがフォームに入力する際に発生する各種イベントに応答するコードを書くことができます。InfoPath 内でイベントの作業を実行するには、InfoPath デザイン モードでイベント ハンドラーを作成します。</span><span class="sxs-lookup"><span data-stu-id="792d9-p102">You can write code to respond to various events that can occur as a user fills out a form. To work with events in InfoPath, you create event handlers in the InfoPath designer.</span></span>
  
<span data-ttu-id="792d9-p103">InfoPath イベント ハンドラーは、InfoPath デザイン モードで作成してください。これは、InfoPath 2003 互換のオブジェクト モデルを使用する際、InfoPath が、イベント ハンドラーを識別およびシンクするために、フォームのコード ファイル (FormCode.cs または FormCode.vb) 内で、自動的に正しい宣言を追加し、属性 ([InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) を適用するためです。イベント ハンドラーを作成した後は、フォームのコード ファイル内で宣言と属性を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="792d9-p103">InfoPath event handlers should be created in the InfoPath designer because, when using the InfoPath 2003-compatible object model, InfoPath automatically adds the correct declaration and applies an attribute ([InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) in a form's code file (FormCode.cs or FormCode.vb) to identify and sink the event handler. After you have created an event handler, you should not alter its declaration and attribute in the form's code file.</span></span> 
  
<span data-ttu-id="792d9-110">InfoPath のイベント ハンドラーを作成する方法の詳細については、[追加のイベント ハンドラーを使用して InfoPath 2003 オブジェクト モデル](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="792d9-110">For information about creating the InfoPath event handlers, see [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span>
  
## <a name="overview-of-the-event-objects"></a><span data-ttu-id="792d9-111">イベント オブジェクトの概要</span><span class="sxs-lookup"><span data-stu-id="792d9-111">Overview of the Event Objects</span></span>

<span data-ttu-id="792d9-p104">InfoPath 2003 互換オブジェクト モデルには、[Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 名前空間で公開される 9 つのイベント オブジェクトが実装されています。次の表には、それぞれの InfoPath イベント オブジェクト、関連付けられているイベント ハンドラー、およびそれらが提供する機能の説明が一覧表示されています。</span><span class="sxs-lookup"><span data-stu-id="792d9-p104">The InfoPath 2003-compatible object model implements nine event objects that are exposed in the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace. The following table lists each of the InfoPath event objects, the event handlers they are associated with, and a description of the functionality they provide.</span></span> 
  
|<span data-ttu-id="792d9-114">**名前**</span><span class="sxs-lookup"><span data-stu-id="792d9-114">**Name**</span></span>|<span data-ttu-id="792d9-115">**イベント ハンドラー**</span><span class="sxs-lookup"><span data-stu-id="792d9-115">**Event handlers**</span></span>|<span data-ttu-id="792d9-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="792d9-116">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="792d9-117">リーフ</span><span class="sxs-lookup"><span data-stu-id="792d9-117">DataDOMEvent</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.aspx) <br/> |[<span data-ttu-id="792d9-118">OnBeforeChange</span><span class="sxs-lookup"><span data-stu-id="792d9-118">OnBeforeChange</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx) <br/> <span data-ttu-id="792d9-119">[OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) , [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx)</span><span class="sxs-lookup"><span data-stu-id="792d9-119">[OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) , [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx)</span></span> <br/> |<span data-ttu-id="792d9-p105">XML Document Object Model (DOM) の変更中に、フォームの基になる XML ドキュメントへの参照、リターン状態、およびその他の XML ノードに関する情報を含むプロパティを返します。エラーを発生させるメソッドも含みます。</span><span class="sxs-lookup"><span data-stu-id="792d9-p105">Returns a reference to a form's underlying XML document, the return status, and other properties that contain information about the XML node during an XML Document Object Model (DOM) change. Also includes a method for raising an error.</span></span>  <br/> |
|[<span data-ttu-id="792d9-122">DocActionEvent</span><span class="sxs-lookup"><span data-stu-id="792d9-122">DocActionEvent</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocActionEvent.aspx) <br/> |[<span data-ttu-id="792d9-123">OnClick</span><span class="sxs-lookup"><span data-stu-id="792d9-123">OnClick</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) <br/> |<span data-ttu-id="792d9-124">フォーム領域内でのボタン クリック中に、フォームの基になる XML ドキュメントへの参照、リターン状態、およびソース XML ノードを返します。</span><span class="sxs-lookup"><span data-stu-id="792d9-124">Returns a reference to a form's underlying XML document, the return status, and the source XML node during a button click in the form area.</span></span>  <br/> |
|[<span data-ttu-id="792d9-125">DocContextChangeEvent</span><span class="sxs-lookup"><span data-stu-id="792d9-125">DocContextChangeEvent</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocContextChangeEvent.aspx) <br/> |[<span data-ttu-id="792d9-126">OnContextChange</span><span class="sxs-lookup"><span data-stu-id="792d9-126">OnContextChange</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx) <br/> |<span data-ttu-id="792d9-127">フォームの基になる XML ドキュメントの現在のコンテキストである XML Document Object Model (DOM) ノードに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="792d9-127">Returns information about the XML Document Object Model (DOM) node that is the current context of the form's underlying XML document.</span></span>  <br/> |
|[<span data-ttu-id="792d9-128">DocEvent</span><span class="sxs-lookup"><span data-stu-id="792d9-128">DocEvent</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocEvent.aspx) <br/> |<span data-ttu-id="792d9-129">[OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx) , [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx)</span><span class="sxs-lookup"><span data-stu-id="792d9-129">[OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx) , [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx)</span></span> <br/> |<span data-ttu-id="792d9-130">ビューの切り替えやフォームの結合操作中に、フォームの基になる XML ドキュメントへの参照を返します。</span><span class="sxs-lookup"><span data-stu-id="792d9-130">Returns a reference to a form's underlying XML document during a switch view or form merge operation.</span></span>  <br/> |
|[<span data-ttu-id="792d9-131">DocReturnEvent</span><span class="sxs-lookup"><span data-stu-id="792d9-131">DocReturnEvent</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocReturnEvent.aspx) <br/> |<span data-ttu-id="792d9-132">[OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) , [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx)</span><span class="sxs-lookup"><span data-stu-id="792d9-132">[OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) , [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx)</span></span> <br/> |<span data-ttu-id="792d9-133">フォームの読み込みまたは送信中に、フォームの基になる XML ドキュメントへの参照と、リターン状態を返します。</span><span class="sxs-lookup"><span data-stu-id="792d9-133">Returns a reference to a form's underlying XML document and the return status during the loading or submission of a form.</span></span>  <br/> |
|[<span data-ttu-id="792d9-134">MergeEvent</span><span class="sxs-lookup"><span data-stu-id="792d9-134">MergeEvent</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MergeEvent.aspx) <br/> |[<span data-ttu-id="792d9-135">OnMergeRequest</span><span class="sxs-lookup"><span data-stu-id="792d9-135">OnMergeRequest</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) <br/> |<span data-ttu-id="792d9-136">フォームの基となる XML ドキュメントをプログラムから操作したり、結合するファイルの数などの結合プロパティを調べたりするために、 **OnMergeRequest** イベント中に使用できるプロパティとメソッドを返します。</span><span class="sxs-lookup"><span data-stu-id="792d9-136">Returns properties and methods that can be used during an **OnMergeRequest** event to programmatically interact with a form's underlying XML document and to determine merge properties such as the number of files being merged.</span></span>  <br/> |
|[<span data-ttu-id="792d9-137">SaveEvent</span><span class="sxs-lookup"><span data-stu-id="792d9-137">SaveEvent</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SaveEvent.aspx) <br/> |[<span data-ttu-id="792d9-138">OnSaveRequest</span><span class="sxs-lookup"><span data-stu-id="792d9-138">OnSaveRequest</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) <br/> |<span data-ttu-id="792d9-139">フォームの基となる XML ドキュメントをプログラムから操作したり、保存プロパティを指定したり、保存操作を実行したりするために、 **OnSaveRequest** イベント ハンドラーからの保存操作中に使用できるプロパティとメソッドの数を返します。</span><span class="sxs-lookup"><span data-stu-id="792d9-139">Returns a number of properties and methods that can be used during a save operation from the **OnSaveRequest** event handler to programmatically interact with a form's underlying XML document, determine save properties, and perform the save operation.</span></span>  <br/> |
|[<span data-ttu-id="792d9-140">SignEvent</span><span class="sxs-lookup"><span data-stu-id="792d9-140">SignEvent</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) <br/> |[<span data-ttu-id="792d9-141">OnSign</span><span class="sxs-lookup"><span data-stu-id="792d9-141">OnSign</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |<span data-ttu-id="792d9-142">デジタル署名に追加データを追加するために使用します。</span><span class="sxs-lookup"><span data-stu-id="792d9-142">Used to add additional data to the digital signature.</span></span>  <br/> |
|[<span data-ttu-id="792d9-143">VersionUpgradeEvent</span><span class="sxs-lookup"><span data-stu-id="792d9-143">VersionUpgradeEvent</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.VersionUpgradeEvent.aspx) <br/> |[<span data-ttu-id="792d9-144">OnVersionUpgrade</span><span class="sxs-lookup"><span data-stu-id="792d9-144">OnVersionUpgrade</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) <br/> |<span data-ttu-id="792d9-145">バージョン アップグレード操作中に、フォームの基となる XML ドキュメントへの参照、リターン状態、およびドキュメントとソリューションのバージョン番号を返します。</span><span class="sxs-lookup"><span data-stu-id="792d9-145">Returns a reference to a form's underlying XML document, the return status, and the document and solution version numbers during the version upgrade operation.</span></span>  <br/> |
   
## <a name="using-the-event-objects"></a><span data-ttu-id="792d9-146">イベント オブジェクトの使用</span><span class="sxs-lookup"><span data-stu-id="792d9-146">Using the Event Objects</span></span>

<span data-ttu-id="792d9-p106">イベント ハンドラーを作成する際、InfoPath は、プロジェクトのフォーム コード ファイル (FormCode.cs または FormCode.vb) 内でイベント ハンドラーの宣言を作成します。イベント ハンドラーの宣言内で、InfoPath は、イベント ハンドラーに渡されるパラメーターの名前として **e** を使用します。このパラメーターには、イベント ハンドラーに関連付けられるイベント オブジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="792d9-p106">When you create an event handler, InfoPath creates the event handler's declaration in the project's form code file (FormCode.cs or FormCode.vb). In the declaration of the event handler, InfoPath uses **e** as the name of the parameter that is passed to the event handler. This parameter contains the event object that is associated with the event handler.</span></span> 
  
<span data-ttu-id="792d9-150">たとえば、[ **開発**] タブの [ **OnLoad イベント**] をクリックすることで、デザイン モードで **OnLoad** イベントのイベント ハンドラーを作成する際、InfoPath は、 **DocReturnEvent** オブジェクトを受け取るイベント ハンドラーの宣言をフォーム コード ファイルに追加し、以下のイベント ハンドラー宣言にコードを追加するためのコード エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="792d9-150">For example, when you create an event handler for the **OnLoad** event in design mode (by clicking **On Load Event** on the **Developer** tab), InfoPath adds the declaration for the event handler that receives the **DocReturnEvent** object to the form code file, and then opens the Code Editor so that you can add your code to the following event handler declaration.</span></span> 
  
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

<span data-ttu-id="792d9-p107">イベント ハンドラーのコードを書く際、 **e** パラメーターを通じて渡されるイベント オブジェクトによって実装されるプロパティとメソッドを使用できます。たとえば、以下の **OnBeforeChange** イベント ハンドラーでは、 [DataDOMEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.NewValue.aspx) イベント オブジェクトの **NewValue** プロパティを使用して、変更されたフィールドの値が確認されます。それが空白の場合は、 [DataDOMEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnMessage.aspx) イベント オブジェクトの **ReturnMessage** プロパティを使用して、ユーザーに対してダイアログ ボックスでエラーが表示され、 [ReturnStatus](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnStatus.aspx) プロパティが **false** に設定されて、ユーザーが行った変更が受け入れられないことを示します。</span><span class="sxs-lookup"><span data-stu-id="792d9-p107">When writing code for an event handler, you can use the properties and methods implemented by the event object that is passed through the **e** parameter. For example, in the following **OnBeforeChange** event handler, the [NewValue](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.NewValue.aspx) property of the **DataDOMEvent** event object is used to check the value of the field that was just changed. If it is blank, the [ReturnMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnMessage.aspx) property of the **DataDOMEvent** event object is used to display an error to the user in a dialog box, and the [ReturnStatus](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnStatus.aspx) property is set to **false**, indicating that the changes the user made should not be accepted.</span></span>
  
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
> <span data-ttu-id="792d9-p108">InfoPath 2003 互換オブジェクト モデルのそれぞれの InfoPath イベント オブジェクトは、異なるプロパティとメソッドを実装します。特定のイベント オブジェクトに関する詳細については、前に示したイベント オブジェクトの表でそれぞれのオブジェクトをクリックして参照してください。</span><span class="sxs-lookup"><span data-stu-id="792d9-p108">Each of the InfoPath event objects in the InfoPath 2003-compatible object model implements different properties and methods. For more information about a particular event object, click the appropriate object in the Event Objects table shown earlier.</span></span> 
  

