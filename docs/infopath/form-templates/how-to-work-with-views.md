---
title: ビューを操作する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- ビュー クラス [infopath 2007],InfoPath 2007,ビューを操作する,ビュー [InfoPath 2007]
localization_priority: Normal
ms.assetid: 947b33c3-2acc-45d2-a89d-a712b6bc53df
description: InfoPath フォーム テンプレートで作業する場合、フォームのビューにアクセスし、ビューに含まれるデータにさまざまな操作を行うコードを書くことができます。Microsoft.Office.InfoPath 名前空間によって提供される InfoPath オブジェクト モデルでは、View クラスのメンバーを使用して、フォームのビューにアクセスできます。
ms.openlocfilehash: 829375a87513634ef0b38b6d92de9f33a605e89f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406298"
---
# <a name="work-with-views"></a><span data-ttu-id="f220d-105">ビューを操作する</span><span class="sxs-lookup"><span data-stu-id="f220d-105">Work with Views</span></span>

<span data-ttu-id="f220d-p102">InfoPath フォーム テンプレートで作業する場合、フォームのビューにアクセスし、ビューに含まれるデータにさまざまな操作を行うコードを書くことができます。[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間によって提供される InfoPath オブジェクト モデルでは、 [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) クラスのメンバーを使用して、フォームのビューにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f220d-p102">When working with an InfoPath form template, you can write code to access the form's views, and then perform a variety of actions on the data that the views contain. The InfoPath object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace supports access to a form's views through the use of the members of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class.</span></span> 
  
## <a name="overview-of-the-view-class"></a><span data-ttu-id="f220d-108">View クラスの概要</span><span class="sxs-lookup"><span data-stu-id="f220d-108">Overview of the View Class</span></span>

<span data-ttu-id="f220d-109">[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) クラスには、次のメソッドとプロパティがあります。フォームの開発者は、これらを使用することにより、InfoPath ビューを操作できます。</span><span class="sxs-lookup"><span data-stu-id="f220d-109">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class provides the following methods and properties, which form developers can use to interact with an InfoPath view.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f220d-110">[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) クラスのメソッドとプロパティは [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) イベント中には利用できません。</span><span class="sxs-lookup"><span data-stu-id="f220d-110">The methods and properties of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class are not available during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event.</span></span> 
  
|<span data-ttu-id="f220d-111">**名前**</span><span class="sxs-lookup"><span data-stu-id="f220d-111">**Name**</span></span>|<span data-ttu-id="f220d-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="f220d-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f220d-113">[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="f220d-113">[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="f220d-114">フォームの基になる XML ドキュメントと、それに関連付けられているビューが自動的に同期しないようにします。</span><span class="sxs-lookup"><span data-stu-id="f220d-114">Disables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="f220d-115">[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="f220d-115">[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="f220d-116">フォームの基になる XML ドキュメントと、それに関連付けられているビューが自動的に同期するようにします。</span><span class="sxs-lookup"><span data-stu-id="f220d-116">Enables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="f220d-117">[ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="f220d-117">[ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="f220d-118">ビューで現在選択されているデータに基づいて、フォームの基になる XML ドキュメントに対して編集コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f220d-118">Executes an editing command against a form's underlying XML document, based on the data currently selected in the view.</span></span>  <br/> |
|<span data-ttu-id="f220d-119">[ExecuteAction(ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="f220d-119">[ExecuteAction(ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="f220d-120">指定したフィールドまたはグループに基づいて、フォームの基になる XML ドキュメントに対して編集コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f220d-120">Executes an editing command against a form's underlying XML document, based on the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="f220d-121">[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="f220d-121">[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) method</span></span>  <br/> |<span data-ttu-id="f220d-122">指定された形式のファイルにビューをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="f220d-122">Exports the view to a file of the specified format.</span></span>  <br/> |
|<span data-ttu-id="f220d-123">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="f220d-123">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="f220d-124">フォームの基になる XML ドキュメントと、それに関連付けられているビューを強制的に同期させます。</span><span class="sxs-lookup"><span data-stu-id="f220d-124">Forces synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="f220d-125">[GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="f220d-125">[GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="f220d-126">指定したノードから開始する、返された XML ノードに対して反復処理を行うための **XPathNodeIterator** オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="f220d-126">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes starting from the specified node.</span></span>  <br/> |
|<span data-ttu-id="f220d-127">[GetContextNodes(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="f220d-127">[GetContextNodes(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="f220d-128">指定したフィールドまたはグループにバインドされているコントロール内にある、現在の選択範囲内の返された XML ノードに対して反復処理を行うための **XPathNodeIterator** オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="f220d-128">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes in the current selection within the control bound to the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="f220d-129">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="f220d-129">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="f220d-130">ビューで現在選択されている項目内のすべての XML ノードに対して反復処理を行うための **XPathNodeIterator** オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="f220d-130">Gets a reference to an **XPathNodeIterator** object for iterating over all XML nodes in the current selection of items in a view.</span></span>  <br/> |
|<span data-ttu-id="f220d-131">[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="f220d-131">[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="f220d-132">指定した開始 XML ノードに基づいて、ビュー内の一定範囲内のノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="f220d-132">Selects a range of nodes in a view based on the specified starting XML node.</span></span>  <br/> |
|<span data-ttu-id="f220d-133">[SelectNodes(XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="f220d-133">[SelectNodes(XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="f220d-134">指定した開始 XML ノードと終了 XML ノードに基づいて、ビュー内の一定範囲内のノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="f220d-134">Selects a range of nodes in a view based on the specified starting XML node and ending XML node.</span></span>  <br/> |
|<span data-ttu-id="f220d-135">[SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="f220d-135">[SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="f220d-136">指定した開始 XML ノード、終了 XML ノード、および指定されたコントロールに基づいて、ビュー内の一定範囲のノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="f220d-136">Selects a range of nodes in a view based on the specified starting XML node, the ending XML node, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="f220d-137">[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="f220d-137">[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="f220d-138">このメソッドに渡された **XPathNavigator** オブジェクトで指定されるノードにバインドされた編集可能なコントロールに格納されているテキストを選択します。</span><span class="sxs-lookup"><span data-stu-id="f220d-138">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method.</span></span>  <br/> |
|<span data-ttu-id="f220d-139">[SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="f220d-139">[SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="f220d-140">このメソッドに渡された **XPathNavigator** オブジェクトで指定されるノードにバインドされた編集可能なコントロールに格納されているテキスト、および指定されたコントロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="f220d-140">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="f220d-141">[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="f220d-141">[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) method</span></span>  <br/> |<span data-ttu-id="f220d-142">現在のビューが含まれる電子メール メッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="f220d-142">Creates an email message containing the current view.</span></span>  <br/> |
|<span data-ttu-id="f220d-143">[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="f220d-143">[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) property</span></span>  <br/> |<span data-ttu-id="f220d-144">ビューに関連付けられている [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="f220d-144">Gets a reference to a [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span>  <br/> |
|<span data-ttu-id="f220d-145">[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="f220d-145">[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) property</span></span>  <br/> |<span data-ttu-id="f220d-146">ビューに関連付けられている [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) オブジェクトへの参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="f220d-146">Gets a reference to a [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) object associated with the view.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="f220d-147">InfoPath オブジェクト モデルには、[ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) クラスと [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) クラスもあります。これらを使用して、フォームに実装されているすべてのビューに関する情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="f220d-147">The InfoPath object model also provides the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) and [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) classes, which can be used to get information about all of the views implemented in a form.</span></span> 
  
## <a name="using-the-view-class"></a><span data-ttu-id="f220d-148">View クラスを使用する</span><span class="sxs-lookup"><span data-stu-id="f220d-148">Using the View Class</span></span>

<span data-ttu-id="f220d-p103">[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) クラスにアクセスするには、 [this](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) (C#) または [Me](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) (Visual Basic) キーワードを使用してアクセスする **XmlForm** クラスの **CurrentView** プロパティを使用します。ビューの名前にアクセスするには、ビューに関連付けられている [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) オブジェクトにアクセスする必要があります。次の例では、現在アクティブなビューの名前をメッセージ ボックスに表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f220d-p103">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class is accessed through the [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class, which is accessed using the **this** (C#) or **Me** (Visual Basic) keyword. To access the name of the view, you need to access the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view. The following example demonstrates how to display a message box with the name of the view that is currently active.</span></span> 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

<span data-ttu-id="f220d-p104">すべての InfoPath フォーム テンプレートには、少なくとも 1 つの既定のビューがありますが、InfoPath ではフォームの基になる XML ドキュメントの複数のビューを作成することもできます。複数のビューがある場合、[ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) を使用して、フォーム テンプレートに実装されたすべてのビューで作業できます。フォーム テンプレートの [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) にアクセスするには、 [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) クラスの [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) プロパティを使用します。現在アクティブなビューをプログラムで変更するには、次のコード サンプルで示すように [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) の [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f220d-p104">All InfoPath form templates contain at least one default view; however, InfoPath also supports the creation of multiple views of a form's underlying XML document. When you have multiple views, the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) can be used to work with all of the views implemented in the form template. To access the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) of a form template, use the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class. You can programmatically change the view that is currently active by using the [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) method of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , as the following code sample demonstrates.</span></span> 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

<span data-ttu-id="f220d-p105">ビューを切り替える前の例は、フォームが開かれた後にのみ動作します。[Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) イベント中の既定のビューを設定するには、次の例で示すように、 [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) クラスの [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) プロパティを使用します。ただし、この値は、フォームが保存され、もう一度開かれた後にのみ有効になることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f220d-p105">The previous example for switching a view will work only after the form is opened. To set a default view during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event, use the [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) property of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) class as shown in the following example. Note, however, that this value will only take effect after the form is saved and re-opened.</span></span> 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a><span data-ttu-id="f220d-159">ビューでコントロールを選択する</span><span class="sxs-lookup"><span data-stu-id="f220d-159">Selecting Controls in a View</span></span>

<span data-ttu-id="f220d-p106">InfoPath では、現在のビューでプログラムからコントロールを選択するために、[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) クラスの 2 つのメソッド、 [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) と [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) が用意されており、両方ともオーバーロードされます。 [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) メソッドはデータ入力用のコントロール ( **テキスト ボックス**など) に使用され、 **SelectNodes** メソッドは構造用のコントロール ( **省略可能セクション**など) に使用されます。ビューで特定のコントロールを選択するには、ノードとオプションでコントロールの ViewContext ID を指定する必要があります。ViewContext ID は、複数のコントロールがデータ ソース内の同じノードにバインドされている場合に必須となります。ViewContext ID 情報は、フォームのデザイン時に InfoPath により提供されます。</span><span class="sxs-lookup"><span data-stu-id="f220d-p106">InfoPath provides two methods of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class, both of which are overloaded, to programmatically select a control in the current view: the [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) and [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods. The [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method is used for data entry controls, such as a **Text Box**, while the **SelectNodes** method is used for structural controls, such as an **Optional Section**. To select a particular control in the view, you need to provide the node and, optionally, the control's ViewContext ID. The ViewContext ID is needed when you have multiple controls bound to the same node in the data source. InfoPath provides the ViewContext ID information when you design the form.</span></span>
  
<span data-ttu-id="f220d-165">コントロールの ViewContext ID は、コントロールのプロパティ ダイアログ ボックスの **[詳細設定]** タブに表示されます。これを確認するには、コントロールを右クリックし、[_コントロール名_ **プロパティ**] をクリックして、**[詳細設定]** タブをクリックします。これで、コントロールの ViewContext ID が **[詳細設定]** タブの **[コード]** セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f220d-165">A control's ViewContext ID is displayed on the **Advanced** tab of the control's properties dialog box, which is accessed by right-clicking the control, clicking  _ControlName_ **Properties**, and then clicking the **Advanced** tab. The ViewContext ID of the control is listed in the **Code** section of the **Advanced** tab.</span></span> 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a><span data-ttu-id="f220d-166">SelectText および SelectNodes の使用方法</span><span class="sxs-lookup"><span data-stu-id="f220d-166">When to use SelectText and SelectNodes</span></span>

<span data-ttu-id="f220d-167">[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) メソッドを使用して、以下のデータ入力用のコントロールをプログラムから選択できます。</span><span class="sxs-lookup"><span data-stu-id="f220d-167">You can programmatically select the following data entry controls by using the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method:</span></span> 
  
- <span data-ttu-id="f220d-168">テキスト ボックス</span><span class="sxs-lookup"><span data-stu-id="f220d-168">Text Box</span></span>
    
- <span data-ttu-id="f220d-169">リッチ テキスト ボックス</span><span class="sxs-lookup"><span data-stu-id="f220d-169">Rich Text Box</span></span>
    
- <span data-ttu-id="f220d-170">日付の選択</span><span class="sxs-lookup"><span data-stu-id="f220d-170">Date Picker</span></span>
    
<span data-ttu-id="f220d-171">[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) メソッドを使用して、以下の構造用のコントロールをプログラムから選択できます。</span><span class="sxs-lookup"><span data-stu-id="f220d-171">You can programmatically select the following structural controls by using the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method:</span></span> 
  
- <span data-ttu-id="f220d-172">省略可能セクション</span><span class="sxs-lookup"><span data-stu-id="f220d-172">Optional Section</span></span>
    
- <span data-ttu-id="f220d-173">選択肢セクション</span><span class="sxs-lookup"><span data-stu-id="f220d-173">Choice Section</span></span>
    
- <span data-ttu-id="f220d-174">繰り返しセクション (項目)</span><span class="sxs-lookup"><span data-stu-id="f220d-174">Repeating Section (items)</span></span>
    
- <span data-ttu-id="f220d-175">繰り返しテーブル (行)</span><span class="sxs-lookup"><span data-stu-id="f220d-175">Repeating Table (rows)</span></span>
    
- <span data-ttu-id="f220d-176">繰り返し再帰セクション (項目)</span><span class="sxs-lookup"><span data-stu-id="f220d-176">Repeating Recursive Section (items)</span></span>
    
- <span data-ttu-id="f220d-177">箇条書き、段落番号、および標準リスト</span><span class="sxs-lookup"><span data-stu-id="f220d-177">Bulleted, Numbered, and Plain List</span></span>
    
- <span data-ttu-id="f220d-178">横方向の繰り返しテーブル</span><span class="sxs-lookup"><span data-stu-id="f220d-178">Horizontal Repeating Table</span></span>
    
<span data-ttu-id="f220d-179">以下のコントロールは、プログラムから選択またはフォーカスの設定を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="f220d-179">You cannot programmatically select, or set focus to, the following controls:</span></span>
  
- <span data-ttu-id="f220d-180">ドロップダウン リスト ボックス</span><span class="sxs-lookup"><span data-stu-id="f220d-180">Drop-Down List Box</span></span>
    
- <span data-ttu-id="f220d-181">リスト ボックス</span><span class="sxs-lookup"><span data-stu-id="f220d-181">List Box</span></span>
    
- <span data-ttu-id="f220d-182">チェック ボックス</span><span class="sxs-lookup"><span data-stu-id="f220d-182">Check Box</span></span>
    
- <span data-ttu-id="f220d-183">オプション ボタン</span><span class="sxs-lookup"><span data-stu-id="f220d-183">Option Button</span></span>
    
- <span data-ttu-id="f220d-184">ボタン</span><span class="sxs-lookup"><span data-stu-id="f220d-184">Button</span></span>
    
- <span data-ttu-id="f220d-185">画像 (リンクまたは埋め込み)</span><span class="sxs-lookup"><span data-stu-id="f220d-185">Picture (linked or included)</span></span>
    
- <span data-ttu-id="f220d-186">インク描画</span><span class="sxs-lookup"><span data-stu-id="f220d-186">Ink Picture</span></span>
    
- <span data-ttu-id="f220d-187">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="f220d-187">Hyperlink</span></span>
    
- <span data-ttu-id="f220d-188">式ボックス</span><span class="sxs-lookup"><span data-stu-id="f220d-188">Expression Box</span></span>
    
- <span data-ttu-id="f220d-189">縦書きラベル</span><span class="sxs-lookup"><span data-stu-id="f220d-189">Vertical Label</span></span>
    
- <span data-ttu-id="f220d-190">ActiveX セクション</span><span class="sxs-lookup"><span data-stu-id="f220d-190">ActiveX Section</span></span>
    
- <span data-ttu-id="f220d-191">横方向領域</span><span class="sxs-lookup"><span data-stu-id="f220d-191">Horizontal Region</span></span>
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a><span data-ttu-id="f220d-192">SelectText および SelectNodes メソッドを使用する</span><span class="sxs-lookup"><span data-stu-id="f220d-192">Using the SelectText and SelectNodes Methods</span></span>

<span data-ttu-id="f220d-193">次の例では、1 つのパラメーター  [xmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) を持つ **SelectText** メソッドの _SelectText(XPathNavigator)_ オーバーロードを使用して、"my:field1" にバインドされている **テキスト ボックス**を選択しています。</span><span class="sxs-lookup"><span data-stu-id="f220d-193">In the following example, the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides one  _xmlNode_ parameter, is used to select a **Text Box** that is bound to "my:field1".</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

<span data-ttu-id="f220d-p107">複数のコントロールが "my:field1" にバインドされている場合は、個別のコントロールを選択するための追加の  [viewContext](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) パラメーターを提供する **SelectText** メソッドの _SelectText(XPathNavigator, String)_ オーバーロードを使用する必要があります。次の例では、"my:field1" にバインドされている 2 つの **テキスト ボックス** コントロールがあることを想定しています。1 番目のコントロールの ViewContext ID は "CTRL1" で、2 番目のコントロールの ViewContext ID は "CTRL8" です。2 番目のコントロールが選択されています。</span><span class="sxs-lookup"><span data-stu-id="f220d-p107">If you have multiple controls bound to "my:field1", you must use the [SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides an additional  _viewContext_ parameter to select a specific control. The following example assumes that there are two **Text Box** controls bound to "my:field1", with the first control having a ViewContext ID of "CTRL1" and the second control having a ViewContext ID of "CTRL8". The second control is selected.</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

<span data-ttu-id="f220d-197">次の例では、1 つのパラメーター  [startNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) のみを持つ **SelectNodes** メソッドの _SelectNodes(XPathNavigator)_ オーバーロードを使用して、繰り返しグループ "my:employee" にバインドされている繰り返しテーブル内の最初の行を選択しています。</span><span class="sxs-lookup"><span data-stu-id="f220d-197">In the following example, the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides only one  _startNode_ parameter, is used to select the first row in a repeating table bound to the repeating group "my:employee".</span></span> 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

<span data-ttu-id="f220d-p108">繰り返しテーブル内の複数の行を選択することもできます。次の例では、繰り返しグループ "my:employee" にバインドされている繰り返しテーブル内の最初の 3 行が、 [startNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)パラメーターと  **endNode** パラメーターを持つ _SelectNodes_ メソッドの _SelectNodes(XPathNavigator, XPathNavigator, String)_ オーバーロードを使用して選択されています。</span><span class="sxs-lookup"><span data-stu-id="f220d-p108">You can also select multiple rows in a repeating table. In the following example, the first three rows of a repeating table bound to the repeating group "my:employee" are selected using the [SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides  _startNode_ and  _endNode_ parameters:</span></span> 
  
```cs
// Create XPathNavigators to specify range of nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
XPathNavigator repeatingTableRow3 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:myemployee[3]", NamespaceManager);
// Select range of nodes in specified XPathNavigators.
CurrentView.SelectNodes(repeatingTableRow1, repeatingTableRow3);
```


