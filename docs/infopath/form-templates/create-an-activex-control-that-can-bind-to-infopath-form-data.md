---
title: InfoPath フォームのデータにバインドできる ActiveX コントロールを作成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0d62047-bf08-9f70-de00-7f81ef1331f1
description: InfoPath エディターで開くように設計された InfoPath フォームの中で、ActiveX コントロールをホストできます。これらのコントロールは、既存のもの (いくつかの制約があります) を利用するか、または InfoPath 用に特別に作成できます。
ms.openlocfilehash: 90378533a7c3cde4a1927753c0325fdd8d0b3ce5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799102"
---
# <a name="create-an-activex-control-that-can-bind-to-infopath-form-data"></a><span data-ttu-id="eb52a-104">InfoPath フォームのデータにバインドできる ActiveX コントロールを作成する</span><span class="sxs-lookup"><span data-stu-id="eb52a-104">Create an ActiveX Control that can Bind to InfoPath Form Data</span></span>

<span data-ttu-id="eb52a-p102">InfoPath エディターで開くように設計された InfoPath フォームの中で、ActiveX コントロールをホストできます。これらのコントロールは、既存のもの (いくつかの制約があります) を利用するか、または InfoPath 用に特別に作成できます。</span><span class="sxs-lookup"><span data-stu-id="eb52a-p102">You can host ActiveX controls in InfoPath forms that are designed to be opened in the InfoPath editor. These controls can be preexisting (with some constraints) or can be written specifically for InfoPath.</span></span>
  
## <a name="write-an-activex-control"></a><span data-ttu-id="eb52a-107">ActiveX コントロールの作成</span><span class="sxs-lookup"><span data-stu-id="eb52a-107">Write an ActiveX Control</span></span>

<span data-ttu-id="eb52a-108">InfoPath の他のコントロールと同様に、ActiveX コントロールでも既存のコンポーネント オブジェクト モデル (COM) インターフェイスをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb52a-108">As with other controls in InfoPath, ActiveX controls should support existing Component Object Model (COM) interfaces:</span></span>
  
- <span data-ttu-id="eb52a-109">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="eb52a-109">**IDispatch**</span></span>
    
- <span data-ttu-id="eb52a-110">**IPersistPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="eb52a-110">**IPersistPropertyBag**</span></span>
    
- <span data-ttu-id="eb52a-111">**初期化**</span><span class="sxs-lookup"><span data-stu-id="eb52a-111">**IPersistStreamInit**</span></span>
    
- <span data-ttu-id="eb52a-112">**IPropertyPage**</span><span class="sxs-lookup"><span data-stu-id="eb52a-112">**IPropertyPage**</span></span>
    
- <span data-ttu-id="eb52a-113">**IObjectSafety**</span><span class="sxs-lookup"><span data-stu-id="eb52a-113">**IObjectSafety**</span></span>
    
- <span data-ttu-id="eb52a-114">**IPropertyNotifySink**</span><span class="sxs-lookup"><span data-stu-id="eb52a-114">**IPropertyNotifySink**</span></span>
    
- <span data-ttu-id="eb52a-115">**IViewObject**</span><span class="sxs-lookup"><span data-stu-id="eb52a-115">**IViewObject**</span></span>
    
- <span data-ttu-id="eb52a-116">**IOleObject**</span><span class="sxs-lookup"><span data-stu-id="eb52a-116">**IOleObject**</span></span>
    
- <span data-ttu-id="eb52a-117">**IOleInPlaceObject**</span><span class="sxs-lookup"><span data-stu-id="eb52a-117">**IOleInPlaceObject**</span></span>
    
<span data-ttu-id="eb52a-118">ドキュメント オブジェクト モデル (DOM) のプロパティがコントロール内で変更されたときに InfoPath によってそれらのプロパティが更新されるように、次のインターフェイスをコントロールで実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb52a-118">In order for InfoPath to update properties in the Document Object Model (DOM) at the time that they change in the control, the control should implement the following interfaces:</span></span>
  
- <span data-ttu-id="eb52a-119">**コネクション**</span><span class="sxs-lookup"><span data-stu-id="eb52a-119">**IConnectionPointContainer**</span></span>
    
- <span data-ttu-id="eb52a-120">**IEnumConnectionPoints**</span><span class="sxs-lookup"><span data-stu-id="eb52a-120">**IEnumConnectionPoints**</span></span>
    
- <span data-ttu-id="eb52a-121">**IConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="eb52a-121">**IConnectionPoint**</span></span>
    
- <span data-ttu-id="eb52a-122">**IEnumConnections**</span><span class="sxs-lookup"><span data-stu-id="eb52a-122">**IEnumConnections**</span></span>
    
<span data-ttu-id="eb52a-123">また、コントロールとの統合をさらに密接にする、InfoPath 固有の 2 つの COM インターフェイスがあります。</span><span class="sxs-lookup"><span data-stu-id="eb52a-123">Also, there are two InfoPath-specific COM interfaces that provide tighter integration of controls:</span></span>
  
- [<span data-ttu-id="eb52a-124">IInfoPathControl</span><span class="sxs-lookup"><span data-stu-id="eb52a-124">IInfoPathControl</span></span>](http://msdn.microsoft.com/ja-jp/library/bb264625.aspx)
    
- [<span data-ttu-id="eb52a-125">IInfoPathControlSite</span><span class="sxs-lookup"><span data-stu-id="eb52a-125">IInfoPathControlSite</span></span>](http://msdn.microsoft.com/ja-jp/library/bb264627.aspx)
    
## <a name="add-an-activex-control-to-the-infopath-design-environment"></a><span data-ttu-id="eb52a-126">InfoPath デザイン環境に ActiveX コントロールを追加する</span><span class="sxs-lookup"><span data-stu-id="eb52a-126">Add an ActiveX Control to the InfoPath Design Environment</span></span>

<span data-ttu-id="eb52a-p103">[ **コントロール**] 作業ウィンドウの [ **カスタム コントロールの追加または削除**] コマンドを使用すると、 **カスタム コントロールの追加ウィザード**を実行してカスタム コントロールを追加できます。ウィザードでは、既に登録済みの ActiveX コントロールを選択したり、Office Marketplace でその他のカスタム コントロールを検索したりできます。コントロールを選択した後、次のことを指定できます。</span><span class="sxs-lookup"><span data-stu-id="eb52a-p103">The **Add or Remove Custom Controls** command on the **Controls** task pane enables you to use the **Add Custom Control Wizard** to add a custom control. By using the wizard, you can select an ActiveX control that has already been registered or find additional custom controls on Office Marketplace. After you select a control, you can specify the following items.</span></span> 
  
- <span data-ttu-id="eb52a-130">CAB を指定して ActiveX コントロールをフォーム テンプレートと一緒にインストールする。</span><span class="sxs-lookup"><span data-stu-id="eb52a-130">Specify a CAB to install the ActiveX control with your form template.</span></span>
    
- <span data-ttu-id="eb52a-131">バインディング プロパティを指定して XML にバインドする。</span><span class="sxs-lookup"><span data-stu-id="eb52a-131">Specify a binding property to bind to the XML.</span></span>
    
- <span data-ttu-id="eb52a-132">ルールまたはデジタル署名に応答してコントロールを有効または無効にするのに使用されるプロパティを指定する。たとえば、XML が存在しない場合や条件付き書式を使用する場合などに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="eb52a-132">Specify a property that is used to enable or disable the control in response to rules or digital signatures, which can be useful, for example, when the XML is not present or when conditional formatting is used.</span></span>
    
- <span data-ttu-id="eb52a-133">データ型バインディングを指定する。</span><span class="sxs-lookup"><span data-stu-id="eb52a-133">Specify data type binding.</span></span>
    
> [!NOTE]
> <span data-ttu-id="eb52a-134">ActiveX コントロールを作成していて、既に InfoPath の [ **コントロール**] 作業ウィンドウに追加している場合は、InfoPath を閉じるまで ActiveX コントロールをビルドし直すことができなくなります。</span><span class="sxs-lookup"><span data-stu-id="eb52a-134">If you are developing an ActiveX control and have added it to the **Controls** task pane in InfoPath, you will be unable to rebuild the ActiveX control until InfoPath is closed.</span></span> 
  
## <a name="deploy-an-activex-control"></a><span data-ttu-id="eb52a-135">ActiveX コントロールを展開する</span><span class="sxs-lookup"><span data-stu-id="eb52a-135">Deploy an ActiveX Control</span></span>

<span data-ttu-id="eb52a-p104">ActiveX コントロールを配布するにはインストーラーを作成します。インストーラーでは、コントロールを目的のコンピューターにインストールし、InfoPath コントロール テンプレート (ICT) ファイルと CAB ファイルをユーザーのフォルダー \Users\\<ユーザー名\>\AppData\Local\Microsoft\InfoPath\Controls にコピーします。複数の開発者が、ActiveX コントロールを使用するフォームを共同で開発する場合は、InfoPath デザイン環境に追加されたコントロールをそれぞれの開発者が所有してください。そうしないと、InfoPath からコントロールのプロパティを変更できなくなります。</span><span class="sxs-lookup"><span data-stu-id="eb52a-p104">To distribute an ActiveX control, you can write an installer that installs the control on the target computer and copies the InfoPath Control Template (ICT) file and the CAB file to the user's folder, \Users\\<username\>\AppData\Local\Microsoft\InfoPath\Controls. Note that if two or more developers are collaborating on developing forms that use ActiveX controls, each developer should have the controls that were added to the InfoPath design environment, or they will be unable to modify the properties of the controls from InfoPath.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eb52a-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb52a-138">See also</span></span>



<span data-ttu-id="eb52a-139">演習 6: InfoPath 2003 で ActiveX コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="eb52a-139">Lab 6: Adding ActiveX Controls in InfoPath 2003</span></span>
  
[<span data-ttu-id="eb52a-140">Creating an InfoPath Custom Control using C# and .NET (InfoPath Team Blog)</span><span class="sxs-lookup"><span data-stu-id="eb52a-140">Creating an InfoPath Custom Control using C# and .NET (InfoPath Team Blog)</span></span>](http://blogs.msdn.com/infopath/archive/2005/04/15/creating-an-infopath-custom-control-using-c-and-net.aspx)

