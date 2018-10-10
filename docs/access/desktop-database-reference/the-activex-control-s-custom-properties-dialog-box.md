---
title: ActiveX コントロールのカスタム プロパティ] ダイアログ ボックス
TOCTitle: ActiveX Control's Custom Properties Dialog Box
ms:assetid: 124cf679-6efc-567a-84d1-8057dec93bde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15)
ms:contentKeyID: 48543338
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm4040
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6f5924d04e9ea4febee1434f6ef99f95b02eab6b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478213"
---
# <a name="activex-controls-custom-properties-dialog-box"></a><span data-ttu-id="d2cab-102">ActiveX コントロールのカスタム プロパティ] ダイアログ ボックス</span><span class="sxs-lookup"><span data-stu-id="d2cab-102">ActiveX Control's Custom Properties Dialog Box</span></span>

<span data-ttu-id="d2cab-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2cab-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d2cab-p101">ActiveX コントロールのプロパティを設定するときに、そのコントロールのカスタム プロパティ ダイアログ ボックスを使うこともできます。カスタム プロパティ ダイアログ ボックスは、デザイン ビューで ActiveX コントロールのプロパティを設定する場合、Microsoft Access のプロパティ シートのプロパティの一覧に代わる機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="d2cab-p101">When setting the properties of an ActiveX control, you may need or prefer to use the control's custom properties dialog box. This custom properties dialog box provides an alternative to the list of properties in the Microsoft Access property sheet for setting ActiveX control properties in Design view.</span></span>

> [!NOTE]
> <span data-ttu-id="d2cab-106">[!メモ] ここでの説明は Microsoft Access データベース環境で使用する ActiveX コントロールにのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="d2cab-106">This information only applies to ActiveX controls in a Microsoft Access database environment.</span></span>



## <a name="two-ways-to-set-properties"></a><span data-ttu-id="d2cab-107">プロパティを設定する 2 つの方法</span><span class="sxs-lookup"><span data-stu-id="d2cab-107">Two Ways to Set Properties</span></span>

<span data-ttu-id="d2cab-p102">カスタム プロパティ ダイアログ ボックスは、ActiveX コントロールを使用するアプリケーションで、Access のプロパティ シートのようなプロパティ シートが提供されていないことがあるために用意されています。カスタム プロパティ ダイアログ ボックスは、ホスト アプリケーションで提供されるインターフェイスに関係なく、キー コントロール プロパティを設定するインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="d2cab-p102">The reason for the custom properties dialog box is that not all applications that use ActiveX controls provide a property sheet like the one in Microsoft Access. The custom properties dialog box provides an interface for setting key control properties regardless of the interface supplied by the hosting application.</span></span>

<span data-ttu-id="d2cab-110">ActiveX コントロールのプロパティには、次の 2 つのプロパティ シートの両方で設定できるものがあります。</span><span class="sxs-lookup"><span data-stu-id="d2cab-110">For some ActiveX control properties, you can choose either of these two locations to set the property:</span></span>

  - <span data-ttu-id="d2cab-111">Access のプロパティ シート</span><span class="sxs-lookup"><span data-stu-id="d2cab-111">The Microsoft Access property sheet.</span></span>

  - <span data-ttu-id="d2cab-112">ActiveX コントロールのカスタム プロパティ ダイアログ ボックス</span><span class="sxs-lookup"><span data-stu-id="d2cab-112">The ActiveX control's custom properties dialog box.</span></span>

<span data-ttu-id="d2cab-p103">デザイン ビューでプロパティを設定するときに、カスタム プロパティ ダイアログ ボックスしか使用できない場合もあります。それは、プロパティを設定するために必要なインターフェイスが、Access のプロパティ シートでは機能しない場合です。たとえば、カレンダー コントロールの **GridFont** プロパティは複数の引数を持ちますが、Access のプロパティ シートでは 1 つのプロパティに対して複数の引数を設定できません。</span><span class="sxs-lookup"><span data-stu-id="d2cab-p103">In some cases, the custom properties dialog box is the only way to set a property in Design view. This is usually the situation when the interface needed to set a property doesn't work inside the Microsoft Access property sheet. For example, the **GridFont** property for the Calendar control has a number of arguments; you can't set more than one argument per property in the Microsoft Access property sheet.</span></span>

## <a name="finding-the-custom-properties-dialog-box"></a><span data-ttu-id="d2cab-116">カスタム プロパティ ダイアログ ボックスの有無の確認</span><span class="sxs-lookup"><span data-stu-id="d2cab-116">Finding the Custom Properties Dialog Box</span></span>

<span data-ttu-id="d2cab-p104">すべての ActiveX コントロールがカスタム プロパティ ダイアログ ボックスを提供するわけではありません。コントロールがカスタム プロパティ ダイアログ ボックスを提供するかどうかを確認するには、そのコントロールの Microsoft Office Access プロパティ シートで " **Custom** /カスタムコントロール" プロパティを確認します。プロパティの一覧に " **Custom** /カスタムコントロール" の項目があれば、そのコントロールはカスタム プロパティ ダイアログ ボックスを提供します。</span><span class="sxs-lookup"><span data-stu-id="d2cab-p104">Not all ActiveX controls provide a custom properties dialog box. To see whether a control provides this custom properties dialog box, look for the **Custom** property in the Microsoft Access property sheet for this control. If the list of properties contains the name **Custom**, then the control provides the custom properties dialog box.</span></span>

## <a name="using-the-custom-properties-dialog-box"></a><span data-ttu-id="d2cab-120">カスタム プロパティ ダイアログ ボックスの使用</span><span class="sxs-lookup"><span data-stu-id="d2cab-120">Using the Custom Properties Dialog Box</span></span>

<span data-ttu-id="d2cab-p105">コントロールのカスタム プロパティ ダイアログ ボックスを表示するには、Microsoft Office Access プロパティ シートの [ **Custom** /カスタムコントロール] プロパティ ボックスをクリックし、右側に表示される [ **...** ] (ビルド) ボタンをクリックします。このダイアログ ボックスは、通常、タブ付きのダイアログ ボックスとして表示されます。ここで、目的のプロパティを設定するタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="d2cab-p105">After you click the **Custom** property box in the Microsoft Access property sheet, click the **Build** button to the right of the property box to display the control's custom properties dialog box, often presented as a tabbed dialog box. Choose the tab that contains the interface for setting the properties that you want to set.</span></span>

<span data-ttu-id="d2cab-123">[1] タブで変更を加えた後多くの場合変更を適用できます、すぐに (存在する場合)、 **[適用**] ボタンをクリックすると、します。</span><span class="sxs-lookup"><span data-stu-id="d2cab-123">After you make changes on one tab, you can often apply those changes immediately by clicking the **Apply** button (if provided).</span></span> <span data-ttu-id="d2cab-124">必要に応じてその他のプロパティを設定するには、他のタブをクリックすることができます。</span><span class="sxs-lookup"><span data-stu-id="d2cab-124">You can click other tabs to set other properties as needed.</span></span> <span data-ttu-id="d2cab-125">カスタム プロパティ] ダイアログ ボックスで行った変更を承認するには、 **[OK** ] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2cab-125">To approve all changes made in the custom properties dialog box, click the **OK** button.</span></span> <span data-ttu-id="d2cab-126">戻るには、Microsoft Access のプロパティ シートにプロパティ設定を変更せず、 **[キャンセル**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2cab-126">To return to the Microsoft Access property sheet without changing any property settings, click the **Cancel** button.</span></span>

<span data-ttu-id="d2cab-127">[**編集**] メニューで、ActiveX コントロール**オブジェクト**のコマンド (たとえば、 **[カレンダー コントロール オブジェクト]**) の [**プロパティ**] サブコマンドをクリックするかで同じサブコマンドをクリックすると、[カスタム プロパティ] ダイアログ ボックスを表示することもActiveX コントロールのショートカット メニューです。</span><span class="sxs-lookup"><span data-stu-id="d2cab-127">You can also view the custom properties dialog box by clicking the **Properties** subcommand of the ActiveX control **Object** command (for example, **Calendar Control Object**) on the **Edit** menu, or by clicking this same subcommand on the shortcut menu for the ActiveX control.</span></span> <span data-ttu-id="d2cab-128">また、Access プロパティ シートに表示される ActiveX コントロール用のプロパティの中には、カレンダー コントロールの **GridFontColor** プロパティのように、プロパティ ボックスの右側に [ **ビルド** ] ボタンが表示されるプロパティもあります。</span><span class="sxs-lookup"><span data-stu-id="d2cab-128">In addition, some properties in the Microsoft Access property sheet for the ActiveX control, like the **GridFontColor** property of the Calendar control, have a **Build** button to the right of the property box.</span></span> <span data-ttu-id="d2cab-129">[**ビルド**] ボタンをクリックするの適切なタブ (たとえば、**色**)、ユーザー設定のプロパティ] ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d2cab-129">When you click the **Build** button, the custom properties dialog box is displayed, with the appropriate tab selected (for example, **Colors**).</span></span>

