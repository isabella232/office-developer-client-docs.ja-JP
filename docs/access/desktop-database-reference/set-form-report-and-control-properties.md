---
title: セット フォーム、レポート、およびコントロールのプロパティ
TOCTitle: Set form, report, and control properties
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f839ab2e2c6dfab32c49248f1be1878bf289eb6b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477386"
---
# <a name="set-form-report-and-control-properties"></a><span data-ttu-id="761fa-102">セット フォーム、レポート、およびコントロールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="761fa-102">Set form, report, and control properties</span></span>

<span data-ttu-id="761fa-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="761fa-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="761fa-p101">フォーム、レポート、フォームやレポートのセクション、およびコントロールにはそれぞれプロパティがあり、プロパティの設定値を変更すると、特定のアイテムの外観や動作を変更することができます。プロパティの表示や変更は、プロパティ シート、マクロ、または Visual Basic で行います。</span><span class="sxs-lookup"><span data-stu-id="761fa-p101">Each form, report, section, and control has property settings that you can change to alter the look or behavior of that particular item. You view and change properties by using the property sheet, macro, or Visual Basic.</span></span>

## <a name="set-properties"></a><span data-ttu-id="761fa-106">プロパティの設定</span><span class="sxs-lookup"><span data-stu-id="761fa-106">Set properties</span></span>

1. <span data-ttu-id="761fa-p102">フォームのデザイン ビューまたはレポートのデザイン ビューで、プロパティを設定するコントロール、セクション、フォーム、またはレポートを選択します。次のものが選択できます。</span><span class="sxs-lookup"><span data-stu-id="761fa-p102">In form Design view or report Design view, select the control, section, form, or report for which you want to set the property. You can select:</span></span>
    
   - <span data-ttu-id="761fa-p103">1 つまたは複数のコントロール。複数のコントロールを選択するには、Shift キーを押しながらコントロールをクリックするか、またはマウスをクリックしてからドラッグして目的のコントロールを囲みます。複数のコントロールを選択した場合は、各コントロールで共通のプロパティのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="761fa-p103">One or more controls. To select multiple controls, hold down the SHIFT key and click the controls, or drag the mouse pointer over the controls you wish to select. If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span></span>
    
   - <span data-ttu-id="761fa-p104">1 つのセクション。目的のセクションのセクション セレクターをクリックして選択します。</span><span class="sxs-lookup"><span data-stu-id="761fa-p104">One section. Click the section selector of the section you wish to select.</span></span>
    
   - <span data-ttu-id="761fa-p105">フォーム全体またはレポート全体。フォームまたはレポートの左上隅のフォーム セレクターまたはレポート セレクターをクリックして選択します。</span><span class="sxs-lookup"><span data-stu-id="761fa-p105">The entire form or report. Click the form selector or report selector in the upper-left corner of the form or report.</span></span>

2. <span data-ttu-id="761fa-116">オブジェクトまたはセクションを右クリックし、ショートカット メニューの [**プロパティ**] をクリックしてまたはツールバーの [**プロパティ**] をクリックしてプロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="761fa-116">Display the property sheet by right-clicking the object or section and then clicking **Properties** on the shortcut menu, or by clicking **Properties** on the toolbar.</span></span>

3. <span data-ttu-id="761fa-117">値を設定するプロパティをクリックし、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="761fa-117">Click the property for which you want to set the value, and then do one of the following:</span></span>
    
   - <span data-ttu-id="761fa-118">プロパティ ボックスで、適切な設定値または式を入力します。</span><span class="sxs-lookup"><span data-stu-id="761fa-118">In the property box, type the appropriate setting or expression.</span></span>
    
   - <span data-ttu-id="761fa-119">プロパティ ボックスに矢印が含まれる場合はその矢印をクリックし、表示された一覧から値を選択します。</span><span class="sxs-lookup"><span data-stu-id="761fa-119">If the property box contains an arrow, click the arrow and then click a value in the list.</span></span>
    
   - <span data-ttu-id="761fa-120">プロパティ ボックスの右側に、[**ビルド**] ボタンが表示されている場合は、ビルダーを表示するか、ビルダーの選択を求めるダイアログ ボックスを表示をクリックします。</span><span class="sxs-lookup"><span data-stu-id="761fa-120">If a **Build** button appears to the right of the property box, click it to display a builder or to display a dialog box giving you a choice of builders.</span></span> <span data-ttu-id="761fa-121">たとえば、いくつかのプロパティを設定するのには [コード ビルダー、マクロ ビルダー、またはクエリ ビルダーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="761fa-121">For example, you can use the Code Builder, Macro Builder, or Query Builder to set some properties.</span></span>

## <a name="tips"></a><span data-ttu-id="761fa-122">ヒント</span><span class="sxs-lookup"><span data-stu-id="761fa-122">Tips</span></span>

- <span data-ttu-id="761fa-p107">プロパティに式や長い設定値を入力または表示するときに、[ズーム] ウィンドウを使用できます。[ズーム] ウィンドウを表示するには、プロパティ シートのプロパティ ボックスをクリックします。次に、 **Shift\*\*\*\*\*\*\*\*F2** キーを押すか、マウスの右ボタンをクリックして表示されるショートカット メニューの [ズーム] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="761fa-p107">Microsoft Access provides a **Zoom** box for typing and viewing expressions or other long property settings. To display the **Zoom** box, click a property box in the property sheet. Then press SHIFT+F2, or right-click and then click **Zoom** on the shortcut menu.</span></span>

- <span data-ttu-id="761fa-126">コントロールの " **ControlSource** /コントロール ソース" プロパティを設定するには、そのコントロールで設定値を入力します。</span><span class="sxs-lookup"><span data-stu-id="761fa-126">You can set the **ControlSource** property for some controls by typing the property setting in the control itself.</span></span>

- <span data-ttu-id="761fa-127">コントロールの種類ごとに既定のプロパティを変更して、作成するコントロールに別の既定値が設定されるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="761fa-127">You can change the default property settings for a type of control so that future controls you create will have the new default settings.</span></span>

- <span data-ttu-id="761fa-p108">連結コントロールのプロパティの設定値が、基になっているテーブルまたはクエリのフィールドの対応する設定値と一致しない場合があります。設定値が異なる場合は、通常、テーブルやクエリの設定値よりも、フォームやレポートの設定値が優先されます。プロパティを継承させる方法の詳細については、「コントロール プロパティと基になるフィールドのプロパティとの関係」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="761fa-p108">The property settings of a bound control might not match the corresponding settings in the field in the underlying table or query to which the control is bound. If the settings are different, the form or report settings typically override those in the table or query. For more information about how properties are inherited, see How control properties relate to properties in their underlying fields.</span></span>

