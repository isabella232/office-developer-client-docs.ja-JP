---
title: InfoPath 2003 オブジェクト モデルを使用してビューを操作する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003 互換のフォーム テンプレート,ビュー,ビュー [InfoPath 2007], InfoPath 2003 互換のフォーム テンプレート
localization_priority: Normal
ms.assetid: feb1bfcb-1cb1-4d5c-bc84-df86a33a5934
description: InfoPath フォーム テンプレートの作業を行うときは、フォームのビューにアクセスし、ビューに格納されているデータに対してさまざまな操作を実行するためのコードを書くことができます。InfoPath 2003 互換のオブジェクト モデルでは、ViewObject インターフェイスのメンバーを使用してフォームのビューにアクセスできます。
ms.openlocfilehash: 6a2dd408ba51e5c8394120944e0c28897e768738
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411884"
---
# <a name="work-with-views-using-the-infopath-2003-object-model"></a><span data-ttu-id="53b55-105">InfoPath 2003 オブジェクト モデルを使用してビューを操作する</span><span class="sxs-lookup"><span data-stu-id="53b55-105">Work with Views Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="53b55-p102">InfoPath フォーム テンプレートの作業を行うときは、フォームのビューにアクセスし、ビューに格納されているデータに対してさまざまな操作を実行するためのコードを書くことができます。InfoPath 2003 互換のオブジェクト モデルでは、[ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) インターフェイスのメンバーを使用してフォームのビューにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="53b55-p102">When working with an InfoPath form template, you can write code to access the form's views, and then perform a variety of actions on the data that the views contain. The InfoPath 2003-compatible object model supports access to a form's views through the use of the members of the [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) interface.</span></span> 
  
## <a name="overview-of-the-viewobject-interface"></a><span data-ttu-id="53b55-108">ViewObject インターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="53b55-108">Overview of the ViewObject Interface</span></span>

<span data-ttu-id="53b55-109">[ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) インターフェイスには、次のメソッドとプロパティがあります。フォームの開発者は、これらを使用して、InfoPath のビューを操作できます。</span><span class="sxs-lookup"><span data-stu-id="53b55-109">The [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) interface provides the following methods and properties, which form developers can use to interact with an InfoPath view.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="53b55-110">[ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) インターフェイスのメソッドとプロパティは、 [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) イベント中には利用できません。</span><span class="sxs-lookup"><span data-stu-id="53b55-110">The methods and properties of the [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) interface are not available during the [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) event.</span></span> 
  
|<span data-ttu-id="53b55-111">**名前**</span><span class="sxs-lookup"><span data-stu-id="53b55-111">**Name**</span></span>|<span data-ttu-id="53b55-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="53b55-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53b55-113">[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.DisableAutoUpdate.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="53b55-113">[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.DisableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="53b55-114">XML Document Object Model (DOM) とビューの同期を無効にします。</span><span class="sxs-lookup"><span data-stu-id="53b55-114">Disables synchronization of the XML Document Object Model (DOM) and the view.</span></span>  <br/> |
|<span data-ttu-id="53b55-115">[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.EnableAutoUpdate.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="53b55-115">[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.EnableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="53b55-116">XML DOM とビューの同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="53b55-116">Enables synchronization of the XML DOM and the view.</span></span>  <br/> |
|<span data-ttu-id="53b55-117">[ExecuteAction](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ExecuteAction.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="53b55-117">[ExecuteAction](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="53b55-118">InfoPath の編集操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="53b55-118">Executes an InfoPath editing action.</span></span>  <br/> |
|<span data-ttu-id="53b55-119">[Export](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Export.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="53b55-119">[Export](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Export.aspx) method</span></span>  <br/> |<span data-ttu-id="53b55-120">指定した形式のファイルとしてビューをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="53b55-120">Exports the view as a file of the specified format.</span></span>  <br/> |
|<span data-ttu-id="53b55-121">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ForceUpdate.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="53b55-121">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ForceUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="53b55-122">XML DOM とビューを同期します。</span><span class="sxs-lookup"><span data-stu-id="53b55-122">Synchronizes the XML DOM and the view.</span></span>  <br/> |
|<span data-ttu-id="53b55-123">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetContextNodes.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="53b55-123">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="53b55-124">指定した XML ノードとビュー コンテキストまたはビュー内の現在の選択範囲に基づいて、[XMLNodesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLNodesCollection.aspx) インターフェイスへの参照を返します。</span><span class="sxs-lookup"><span data-stu-id="53b55-124">Returns a reference to the [XMLNodesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLNodesCollection.aspx) interface, based on the specified XML node and view context or on the current selection in the view.</span></span>  <br/> |
|<span data-ttu-id="53b55-125">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetSelectedNodes.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="53b55-125">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetSelectedNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="53b55-126">ビュー内の現在の選択範囲に基づいて、 **XMLNodesCollection** インターフェイスへの参照を返します。</span><span class="sxs-lookup"><span data-stu-id="53b55-126">Returns a reference to the **XMLNodesCollection** interface, based on the current selection in the view.</span></span>  <br/> |
|<span data-ttu-id="53b55-127">[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="53b55-127">[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="53b55-128">ビュー内の XML ノードの範囲を選択します。</span><span class="sxs-lookup"><span data-stu-id="53b55-128">Selects a range of XML nodes in the view.</span></span>  <br/> |
|<span data-ttu-id="53b55-129">[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectText.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="53b55-129">[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="53b55-130">ビュー内の指定した XML ノードに含まれるテキストを選択します。</span><span class="sxs-lookup"><span data-stu-id="53b55-130">Selects the text contained in the specified XML node in the view.</span></span>  <br/> |
|<span data-ttu-id="53b55-131">[SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SwitchView.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="53b55-131">[SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SwitchView.aspx) method</span></span>  <br/> |<span data-ttu-id="53b55-132">InfoPath のフォームを、指定したビューに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="53b55-132">Switches an InfoPath form to the specified view</span></span>  <br/> |
|<span data-ttu-id="53b55-133">[Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Name.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="53b55-133">[Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Name.aspx) property</span></span>  <br/> |<span data-ttu-id="53b55-134">現在のビューの名前を示す文字列値を返します。</span><span class="sxs-lookup"><span data-stu-id="53b55-134">Returns a string value indicating the name of the current view.</span></span>  <br/> |
|<span data-ttu-id="53b55-135">[Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="53b55-135">[Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) property</span></span>  <br/> |<span data-ttu-id="53b55-136">ビューに関連付けられている [Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) にアクセスする **WindowObject** インターフェイスへの参照を返します。</span><span class="sxs-lookup"><span data-stu-id="53b55-136">Returns a reference to the [WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) interface which accesses the **Window** associated with the view.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="53b55-137">InfoPath 2003 互換オブジェクト モデルには、[ViewInfosCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfosCollection.aspx) インターフェイスもあります。これを使用して、フォーム内で実装されているすべてのビューに関する情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="53b55-137">The InfoPath 2003-compatible object model also provides the [ViewInfosCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfosCollection.aspx) interface, which can be used to get information about all of the views implemented in a form.</span></span> 
  
## <a name="using-the-viewobject-interface"></a><span data-ttu-id="53b55-138">ViewObject インターフェイスを使用する</span><span class="sxs-lookup"><span data-stu-id="53b55-138">Using the ViewObject Interface</span></span>

<span data-ttu-id="53b55-p103">[ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) インターフェイスは、 [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) インターフェイス (フォーム コード クラスの  [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) メソッドで初期化される  `thisXDocument` 変数を通じてアクセス) の `_Startup` プロパティを通じてアクセスされます。たとえば、次のコード例では、 [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) インターフェイスの [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) メソッドを使用して、フォームの基になる XML ドキュメントに関連付けられている現在のビューの名前を示すメッセージ ボックスを表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="53b55-p103">The [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) interface is accessed through the [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface (which is accessed through the  `thisXDocument` variable that is initialized in the  `_Startup` method of the form code class). For example, the following code sample demonstrates how to use the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface to display a message box with the name of the current view that is associated with a form's underlying XML document.</span></span> 
  
```cs
thisXDocument.UI.Alert("Current view name: " + 
   thisXDocument.View.Name);
```

```vb
thisXDocument.UI.Alert("Current view name: " &amp; _
   thisXDocument.View.Name)
```

<span data-ttu-id="53b55-p104">すべての InfoPath フォームには既定のビューが 1 つ以上含まれますが、フォームの基になる XML ドキュメントのビューを複数作成することもできます。フォーム内に複数のビューがあるときは、 **View** オブジェクトを使用して、現在アクティブなビューを操作できます。現在アクティブなビューをプログラムによって変更するには、次のコード例に示すとおり、 **View** オブジェクトの **SwitchView** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="53b55-p104">All InfoPath forms contain at least one default view; however, InfoPath also supports the creation of multiple views of a form's underlying XML document. When you have multiple views in a form, the **View** object can be used to work with the view that is currently active. You can programmatically change the view that is currently active by using the **SwitchView** method of the **View** object, as the following code sample demonstrates.</span></span> 
  
```cs
thisXDocument.View.SwitchView("MySecondView");
```

```vb
thisXDocument.View.SwitchView("MySecondView")
```

<span data-ttu-id="53b55-p105">ビューを切り替えるこの例は、フォームを開いた後にのみ動作します。 **OnLoad** イベントの発生中に既定のビューを設定するには、次の例に示すとおり、 [ViewInfoObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.IsDefault.aspx) インターフェイスの [IsDefault](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfoObject.aspx) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="53b55-p105">The previous example for switching a view will work only after the form is opened. To set a default view during the **OnLoad** event, use the [IsDefault](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.IsDefault.aspx) property of the [ViewInfoObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfoObject.aspx) interface, as shown in the following example.</span></span> 
  
```cs
thisXDocument.ViewInfos["MyDefaultView"].IsDefault = true;
```

```vb
thisXDocument.ViewInfos("MyDefaultView").IsDefault = True
```


