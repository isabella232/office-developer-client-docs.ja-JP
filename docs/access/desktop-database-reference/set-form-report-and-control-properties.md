---
title: フォーム、レポート、コントロールのプロパティを設定する
TOCTitle: Set form, report, and control properties
description: 各フォーム、レポート、セクション、およびコントロールには、Access 2013でその特定の要素の外観や動作を変更するために変更できるプロパティ設定があります。
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: bacbdc100d147be8bf4327a5a775b199c79347bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308737"
---
# <a name="set-form-report-and-control-properties"></a><span data-ttu-id="b37fa-103">フォーム、レポート、コントロールのプロパティを設定する</span><span class="sxs-lookup"><span data-stu-id="b37fa-103">Set form, report, and control properties</span></span>

<span data-ttu-id="b37fa-104">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="b37fa-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b37fa-p101">フォーム、レポート、フォームやレポートのセクション、およびコントロールにはそれぞれプロパティがあり、プロパティの設定値を変更すると、特定のアイテムの外観や動作を変更することができます。プロパティの表示や変更は、プロパティ シート、マクロ、または Visual Basic で行います。</span><span class="sxs-lookup"><span data-stu-id="b37fa-p101">Each form, report, section, and control has property settings that you can change to alter the look or behavior of that particular item. You view and change properties by using the property sheet, macro, or Visual Basic.</span></span>

## <a name="set-properties"></a><span data-ttu-id="b37fa-107">プロパティの設定</span><span class="sxs-lookup"><span data-stu-id="b37fa-107">Set properties</span></span>

1. <span data-ttu-id="b37fa-p102">フォームのデザイン ビューまたはレポートのデザイン ビューで、プロパティを設定するコントロール、セクション、フォーム、またはレポートを選択します。次のものが選択できます。</span><span class="sxs-lookup"><span data-stu-id="b37fa-p102">In form Design view or report Design view, select the control, section, form, or report for which you want to set the property. You can select:</span></span>
    
   - <span data-ttu-id="b37fa-110">1つ以上のコントロール</span><span class="sxs-lookup"><span data-stu-id="b37fa-110">One or more controls.</span></span> <span data-ttu-id="b37fa-111">複数のコントロールを選択するには、SHIFTキーを押しながらコントロールを選択するか、選択したいコントロールの上にマウスポインタをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="b37fa-111">To select multiple controls, hold down the SHIFT key and click the controls, or drag the mouse pointer over the controls you wish to select.</span></span> <span data-ttu-id="b37fa-112">If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span><span class="sxs-lookup"><span data-stu-id="b37fa-112">If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span></span>
    
   - <span data-ttu-id="b37fa-113">1 つのセクション。</span><span class="sxs-lookup"><span data-stu-id="b37fa-113">One section.</span></span> <span data-ttu-id="b37fa-114">選択したいセクションのセクションセレクタを選択してください。</span><span class="sxs-lookup"><span data-stu-id="b37fa-114">Click the section selector of the section you wish to select.</span></span>
    
   - <span data-ttu-id="b37fa-115">フォーム全体またはレポート</span><span class="sxs-lookup"><span data-stu-id="b37fa-115">The entire form or report.</span></span> <span data-ttu-id="b37fa-116">フォームまたはレポートの左上隅にあるフォームセレクタまたはレポートセレクタを選択します。</span><span class="sxs-lookup"><span data-stu-id="b37fa-116">Click the form selector or report selector in the upper-left corner of the form or report.</span></span>

2. <span data-ttu-id="b37fa-117">オブジェクトまたはセクションを右クリックしてショートカットメニューから**プロパティ**を選択するか、ツールバーの**プロパティ**を選択してプロパティシートを表示します。</span><span class="sxs-lookup"><span data-stu-id="b37fa-117">Display the property sheet by right-clicking the object or section and then clicking **Properties** on the shortcut menu, or by clicking **Properties** on the toolbar.</span></span>

3. <span data-ttu-id="b37fa-118">値を設定するプロパティを選択して、次のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="b37fa-118">Click the property for which you want to set the value, and then do one of the following:</span></span>
    
   - <span data-ttu-id="b37fa-119">プロパティボックスに適切な設定または式を入力します。</span><span class="sxs-lookup"><span data-stu-id="b37fa-119">In the property box, type the appropriate setting or expression.</span></span>
    
   - <span data-ttu-id="b37fa-120">プロパティボックスに矢印が含まれている場合は、矢印を選択してからリスト内の値を選択します。</span><span class="sxs-lookup"><span data-stu-id="b37fa-120">If the property box contains an arrow, click the arrow and then click a value in the list.</span></span>
    
   - <span data-ttu-id="b37fa-121">プロパティーボックスの右側に**ビルド**ボタンが表示されている場合は、選択してビルダーを表示するか、ダイアログボックスを表示してビルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="b37fa-121">If a **Build** button appears to the right of the property box, click it to display a builder or to display a dialog box giving you a choice of builders.</span></span> <span data-ttu-id="b37fa-122">たとえば、コードビルダー、マクロビルダー、またはクエリビルダーを使用していくつかのプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="b37fa-122">For example, you can use the Code Builder, Macro Builder, or Query Builder to set some properties.</span></span>

## <a name="tips"></a><span data-ttu-id="b37fa-123">ヒント</span><span class="sxs-lookup"><span data-stu-id="b37fa-123">Tips</span></span>

- <span data-ttu-id="b37fa-124">Microsoft Accessには、式やその他の長いプロパティ設定を入力および表示するための**ズーム**ボックスがあります。</span><span class="sxs-lookup"><span data-stu-id="b37fa-124">Microsoft Access provides a **Zoom** box for typing and viewing expressions or other long property settings.</span></span> <span data-ttu-id="b37fa-125">**ズーム**ボックスを表示するには、プロパティシートでプロパティボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="b37fa-125">To display the **Zoom** box, choose a property box in the property sheet.</span></span> <span data-ttu-id="b37fa-126">SHIFT + F2を押すか、右クリックでショートカットメニューから**ズーム**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b37fa-126">Press SHIFT+F2, or right-click, and then choose **Zoom** on the shortcut menu.</span></span>

- <span data-ttu-id="b37fa-127">コントロールの " **ControlSource** /コントロール ソース" プロパティを設定するには、そのコントロールで設定値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b37fa-127">You can set the **ControlSource** property for some controls by typing the property setting in the control itself.</span></span>

- <span data-ttu-id="b37fa-128">コントロールの種類ごとに既定のプロパティを変更して、作成するコントロールに別の既定値が設定されるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="b37fa-128">You can change the default property settings for a type of control so that future controls you create will have the new default settings.</span></span>

- <span data-ttu-id="b37fa-129">連結コントロールのプロパティの設定値が、基になっているテーブルまたはクエリのフィールドの対応する設定値と一致しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="b37fa-129">The property settings of a bound control might not match the corresponding settings in the field in the underlying table or query to which the control is bound.</span></span> <span data-ttu-id="b37fa-130">設定値が異なる場合は、通常、テーブルやクエリの設定値よりも、フォームやレポートの設定値が優先されます。</span><span class="sxs-lookup"><span data-stu-id="b37fa-130">If the settings are different, the form or report settings typically override those in the table or query.</span></span>

