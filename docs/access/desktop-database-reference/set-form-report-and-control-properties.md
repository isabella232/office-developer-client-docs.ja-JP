---
title: フォーム、レポート、コントロールのプロパティを設定する
TOCTitle: Set form, report, and control properties
description: 各フォーム、レポート、セクション、およびコントロールは、外観や Access 2013 内の特定のアイテムの動作を変更するのには変更可能なプロパティの設定値を持ちます。
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701691"
---
# <a name="set-form-report-and-control-properties"></a><span data-ttu-id="a18b9-103">フォーム、レポート、コントロールのプロパティを設定する</span><span class="sxs-lookup"><span data-stu-id="a18b9-103">Set form, report, and control properties</span></span>

<span data-ttu-id="a18b9-104">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a18b9-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a18b9-p101">フォーム、レポート、フォームやレポートのセクション、およびコントロールにはそれぞれプロパティがあり、プロパティの設定値を変更すると、特定のアイテムの外観や動作を変更することができます。プロパティの表示や変更は、プロパティ シート、マクロ、または Visual Basic で行います。</span><span class="sxs-lookup"><span data-stu-id="a18b9-p101">Each form, report, section, and control has property settings that you can change to alter the look or behavior of that particular item. You view and change properties by using the property sheet, macro, or Visual Basic.</span></span>

## <a name="set-properties"></a><span data-ttu-id="a18b9-107">プロパティの設定</span><span class="sxs-lookup"><span data-stu-id="a18b9-107">Set properties</span></span>

1. <span data-ttu-id="a18b9-p102">フォームのデザイン ビューまたはレポートのデザイン ビューで、プロパティを設定するコントロール、セクション、フォーム、またはレポートを選択します。次のものが選択できます。</span><span class="sxs-lookup"><span data-stu-id="a18b9-p102">In form Design view or report Design view, select the control, section, form, or report for which you want to set the property. You can select:</span></span>
    
   - <span data-ttu-id="a18b9-110">1 つまたは複数のコントロール。</span><span class="sxs-lookup"><span data-stu-id="a18b9-110">One or more controls.</span></span> <span data-ttu-id="a18b9-111">複数のコントロールを選択、SHIFT キーを押しながら、コントロールを選択またはを選択するコントロールをマウス ポインターをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="a18b9-111">To select multiple controls, hold down the SHIFT key and choose the controls, or drag the mouse pointer over the controls you wish to select.</span></span> <span data-ttu-id="a18b9-112">複数のコントロールを選択すると、プロパティ シートで選択したコントロールに共通するプロパティのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a18b9-112">If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span></span>
    
   - <span data-ttu-id="a18b9-113">1 つのセクション。</span><span class="sxs-lookup"><span data-stu-id="a18b9-113">One section.</span></span> <span data-ttu-id="a18b9-114">選択するセクションのセクション セレクターを選択します。</span><span class="sxs-lookup"><span data-stu-id="a18b9-114">Choose the section selector of the section you wish to select.</span></span>
    
   - <span data-ttu-id="a18b9-115">フォーム全体またはレポート全体。</span><span class="sxs-lookup"><span data-stu-id="a18b9-115">The entire form or report.</span></span> <span data-ttu-id="a18b9-116">フォームまたはレポートの左上隅のフォーム セレクターまたはレポート セレクターを選択します。</span><span class="sxs-lookup"><span data-stu-id="a18b9-116">Choose the form selector or report selector in the upper-left corner of the form or report.</span></span>

2. <span data-ttu-id="a18b9-117">オブジェクトまたはセクションを右クリックし、[ショートカット] メニュー**のプロパティ**を選択またはツールバーの**プロパティ**を選択してプロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="a18b9-117">Display the property sheet by right-clicking the object or section and then choosing **Properties** on the shortcut menu, or by choosing **Properties** on the toolbar.</span></span>

3. <span data-ttu-id="a18b9-118">プロパティの値を設定する] を選択し、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a18b9-118">Choose the property for which you want to set the value, and then do one of the following:</span></span>
    
   - <span data-ttu-id="a18b9-119">プロパティ ボックスで、適切な設定値または式を入力します。</span><span class="sxs-lookup"><span data-stu-id="a18b9-119">In the property box, type the appropriate setting or expression.</span></span>
    
   - <span data-ttu-id="a18b9-120">プロパティ ボックスに矢印が含まれている場合、矢印を選択し、リストで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="a18b9-120">If the property box contains an arrow, choose the arrow and then choose a value in the list.</span></span>
    
   - <span data-ttu-id="a18b9-121">プロパティ ボックスの右側に、[**ビルド**] ボタンが表示されている場合は、ビルダーを表示するか、ビルダーの選択を求めるダイアログ ボックスを表示を選択します。</span><span class="sxs-lookup"><span data-stu-id="a18b9-121">If a **Build** button appears to the right of the property box, choose it to display a builder or to display a dialog box giving you a choice of builders.</span></span> <span data-ttu-id="a18b9-122">たとえば、いくつかのプロパティを設定するのには [コード ビルダー、マクロ ビルダー、またはクエリ ビルダーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="a18b9-122">For example, you can use the Code Builder, Macro Builder, or Query Builder to set some properties.</span></span>

## <a name="tips"></a><span data-ttu-id="a18b9-123">ヒント</span><span class="sxs-lookup"><span data-stu-id="a18b9-123">Tips</span></span>

- <span data-ttu-id="a18b9-124">Access には、入力式またはその他の long 型のプロパティの設定を表示したりするためには、[**ズーム**] ボックスが用意されています。</span><span class="sxs-lookup"><span data-stu-id="a18b9-124">Microsoft Access provides a **Zoom** box for typing and viewing expressions or other long property settings.</span></span> <span data-ttu-id="a18b9-125">[**ズーム**] ボックスを表示するには、プロパティ シートのプロパティ ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="a18b9-125">To display the **Zoom** box, choose a property box in the property sheet.</span></span> <span data-ttu-id="a18b9-126">SHIFT + f2 キー、または右クリックしを押し、ショートカット メニューの [**拡大/縮小**をします。</span><span class="sxs-lookup"><span data-stu-id="a18b9-126">Press SHIFT+F2, or right-click, and then choose **Zoom** on the shortcut menu.</span></span>

- <span data-ttu-id="a18b9-127">コントロールの " **ControlSource** /コントロール ソース" プロパティを設定するには、そのコントロールで設定値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a18b9-127">You can set the **ControlSource** property for some controls by typing the property setting in the control itself.</span></span>

- <span data-ttu-id="a18b9-128">コントロールの種類ごとに既定のプロパティを変更して、作成するコントロールに別の既定値が設定されるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="a18b9-128">You can change the default property settings for a type of control so that future controls you create will have the new default settings.</span></span>

- <span data-ttu-id="a18b9-129">連結コントロールのプロパティの設定値が、基になっているテーブルまたはクエリのフィールドの対応する設定値と一致しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a18b9-129">The property settings of a bound control might not match the corresponding settings in the field in the underlying table or query to which the control is bound.</span></span> <span data-ttu-id="a18b9-130">設定値が異なる場合は、通常、テーブルやクエリの設定値よりも、フォームやレポートの設定値が優先されます。</span><span class="sxs-lookup"><span data-stu-id="a18b9-130">If the settings are different, the form or report settings typically override those in the table or query.</span></span>

