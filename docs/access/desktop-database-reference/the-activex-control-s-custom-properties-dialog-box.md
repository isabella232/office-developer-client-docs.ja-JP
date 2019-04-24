---
title: ActiveX コントロールのカスタム プロパティ ダイアログ ボックス
TOCTitle: ActiveX control custom properties dialog box
description: カスタム プロパティ ダイアログ ボックスは、デザイン ビューで ActiveX コントロールのプロパティを設定する場合、Microsoft Access のプロパティ シートのプロパティの一覧に代わる機能を提供します。
ms:assetid: 124cf679-6efc-567a-84d1-8057dec93bde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15)
ms:contentKeyID: 48543338
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm4040
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f4574abc86e6eacd38721e601d26c8b8fbf0a0d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314106"
---
# <a name="activex-control-custom-properties-dialog-box"></a><span data-ttu-id="fff84-103">ActiveX コントロールのカスタム プロパティ ダイアログ ボックス</span><span class="sxs-lookup"><span data-stu-id="fff84-103">ActiveX control custom properties dialog box</span></span>

<span data-ttu-id="fff84-104">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="fff84-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fff84-p101">ActiveX コントロールのプロパティを設定するときに、そのコントロールのカスタム プロパティ ダイアログ ボックスを使うこともできます。カスタム プロパティ ダイアログ ボックスは、デザイン ビューで ActiveX コントロールのプロパティを設定する場合、Microsoft Access のプロパティ シートのプロパティの一覧に代わる機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="fff84-p101">When setting the properties of an ActiveX control, you may need or prefer to use the control's custom properties dialog box. This custom properties dialog box provides an alternative to the list of properties in the Microsoft Access property sheet for setting ActiveX control properties in Design view.</span></span>

> [!NOTE]
> <span data-ttu-id="fff84-107">[!メモ] ここでの説明は Microsoft Access データベース環境で使用する ActiveX コントロールにのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="fff84-107">This information only applies to ActiveX controls in a Microsoft Access database environment.</span></span>

## <a name="two-ways-to-set-properties"></a><span data-ttu-id="fff84-108">プロパティを設定する2つの方法</span><span class="sxs-lookup"><span data-stu-id="fff84-108">Two ways to set properties</span></span>

<span data-ttu-id="fff84-p102">カスタム プロパティ ダイアログ ボックスは、ActiveX コントロールを使用するアプリケーションで、Access のプロパティ シートのようなプロパティ シートが提供されていないことがあるために用意されています。カスタム プロパティ ダイアログ ボックスは、ホスト アプリケーションで提供されるインターフェイスに関係なく、キー コントロール プロパティを設定するインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="fff84-p102">The reason for the custom properties dialog box is that not all applications that use ActiveX controls provide a property sheet like the one in Microsoft Access. The custom properties dialog box provides an interface for setting key control properties regardless of the interface supplied by the hosting application.</span></span>

<span data-ttu-id="fff84-111">ActiveX コントロールのプロパティには、次の 2 つのプロパティ シートの両方で設定できるものがあります。</span><span class="sxs-lookup"><span data-stu-id="fff84-111">For some ActiveX control properties, you can choose either of these two locations to set the property:</span></span>

- <span data-ttu-id="fff84-112">Microsoft Office Access のプロパティ シート</span><span class="sxs-lookup"><span data-stu-id="fff84-112">The Microsoft Access property sheet.</span></span>
- <span data-ttu-id="fff84-113">ActiveX コントロールのカスタム プロパティ ダイアログ ボックス</span><span class="sxs-lookup"><span data-stu-id="fff84-113">The ActiveX control's custom properties dialog box.</span></span>

<span data-ttu-id="fff84-p103">デザイン ビューでプロパティを設定するときに、カスタム プロパティ ダイアログ ボックスしか使用できない場合もあります。それは、プロパティの設定に必要なインターフェイスが、Microsoft Office Access のプロパティ シートでは機能しない場合です。たとえば、カレンダー コントロールの **GridFont** プロパティは複数の引数を持ちますが、Microsoft Office Access のプロパティ シートでは 1 つのプロパティに対して複数の引数を設定できません。</span><span class="sxs-lookup"><span data-stu-id="fff84-p103">In some cases, the custom properties dialog box is the only way to set a property in Design view. This is usually the situation when the interface needed to set a property doesn't work inside the Microsoft Access property sheet. For example, the **GridFont** property for the Calendar control has a number of arguments; you can't set more than one argument per property in the Microsoft Access property sheet.</span></span>

## <a name="finding-the-custom-properties-dialog-box"></a><span data-ttu-id="fff84-117">カスタムプロパティダイアログボックスの検索</span><span class="sxs-lookup"><span data-stu-id="fff84-117">Finding the custom properties dialog box</span></span>

<span data-ttu-id="fff84-118">すべての ActiveX コントロールがカスタム プロパティ ダイアログ ボックスを提供するわけではありません。</span><span class="sxs-lookup"><span data-stu-id="fff84-118">Not all ActiveX controls provide a custom properties dialog box.</span></span> <span data-ttu-id="fff84-119">コントロールがカスタム プロパティ ダイアログ ボックスを提供するかどうかを確認するには、そのコントロールの Microsoft Office Access プロパティ シートで " **Custom** /カスタムコントロール" プロパティを確認します。</span><span class="sxs-lookup"><span data-stu-id="fff84-119">To see whether a control provides this custom properties dialog box, look for the **Custom** property in the Microsoft Access property sheet for this control.</span></span> <span data-ttu-id="fff84-120">プロパティのリストに**custom**という名前が含まれている場合、コントロールはカスタムプロパティダイアログボックスを提供します。</span><span class="sxs-lookup"><span data-stu-id="fff84-120">If the list of properties contains the name **Custom**, the control provides the custom properties dialog box.</span></span>

## <a name="using-the-custom-properties-dialog-box"></a><span data-ttu-id="fff84-121">カスタムプロパティダイアログボックスを使用する</span><span class="sxs-lookup"><span data-stu-id="fff84-121">Using the custom properties dialog box</span></span>

<span data-ttu-id="fff84-122">access のプロパティシートで [**カスタム**プロパティ] ボックスを選択したら、プロパティボックスの右側にある [ **.** ..] ボタンをクリックして、コントロールのカスタムプロパティダイアログボックスを表示します。これは、多くの場合、タブ付きダイアログボックスとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="fff84-122">After you choose the **Custom** property box in the Microsoft Access property sheet, choose the **Build** button to the right of the property box to display the control's custom properties dialog box, often presented as a tabbed dialog box.</span></span> <span data-ttu-id="fff84-123">Choose the tab that contains the interface for setting the properties that you want to set.</span><span class="sxs-lookup"><span data-stu-id="fff84-123">Choose the tab that contains the interface for setting the properties that you want to set.</span></span>

<span data-ttu-id="fff84-124">1つのタブで変更を行った後、[**適用**] ボタン (指定されている場合) を選択することで、それらの変更をすぐに適用することができます。</span><span class="sxs-lookup"><span data-stu-id="fff84-124">After you make changes on one tab, you can often apply those changes immediately by choosing the **Apply** button (if provided).</span></span> <span data-ttu-id="fff84-125">他のタブを選択して、必要に応じて他のプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="fff84-125">You can choose other tabs to set other properties as needed.</span></span> <span data-ttu-id="fff84-126">[カスタムプロパティ] ダイアログボックスで行ったすべての変更を承認するには、[ **OK** ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fff84-126">To approve all changes made in the custom properties dialog box, choose the **OK** button.</span></span> <span data-ttu-id="fff84-127">プロパティの設定を変更せずに、access のプロパティシートに戻るには、[**キャンセル**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fff84-127">To return to the Microsoft Access property sheet without changing any property settings, choose the **Cancel** button.</span></span>

<span data-ttu-id="fff84-128">[カスタムプロパティ] ダイアログボックスを表示するには、[**編集**] メニューの [ActiveX コントロール**オブジェクト**] コマンド (たとえば、[**カレンダーコントロールオブジェクト**]) の**プロパティ**サブコマンドを選択するか、または [同じサブコマンドを選択します。ActiveX コントロールのショートカットメニュー。</span><span class="sxs-lookup"><span data-stu-id="fff84-128">You can also view the custom properties dialog box by choosing the **Properties** subcommand of the ActiveX control **Object** command (for example, **Calendar Control Object**) on the **Edit** menu, or by choosing this same subcommand on the shortcut menu for the ActiveX control.</span></span> <span data-ttu-id="fff84-129">また、Access プロパティ シートに表示される ActiveX コントロール用のプロパティの中には、カレンダー コントロールの **GridFontColor** プロパティのように、プロパティ ボックスの右側に [ **ビルド** ] ボタンが表示されるプロパティもあります。</span><span class="sxs-lookup"><span data-stu-id="fff84-129">In addition, some properties in the Microsoft Access property sheet for the ActiveX control, like the **GridFontColor** property of the Calendar control, have a **Build** button to the right of the property box.</span></span> <span data-ttu-id="fff84-130">[**ビルド**] ボタンをクリックすると、[カスタムプロパティ] ダイアログボックスが表示され、適切なタブ (たとえば、**色**) が選択されます。</span><span class="sxs-lookup"><span data-stu-id="fff84-130">When you choose the **Build** button, the custom properties dialog box is displayed, with the appropriate tab selected (for example, **Colors**).</span></span>

