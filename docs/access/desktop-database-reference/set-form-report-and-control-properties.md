---
<span data-ttu-id="42a42-101">タイトル: フォーム、レポートを設定し、コントロールのプロパティ TOCTitle: 設定のフォーム、レポート、およびコントロールのプロパティの <<<<<<< ヘッド ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735 ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15) ms:contentKeyID: 48542977 ms.date: 09/18/2015 === 説明: 各フォーム、レポート、セクション、およびコントロールは、外観や Access 2013 内の特定のアイテムの動作を変更するのには変更可能なプロパティの設定値を持ちます。</span><span class="sxs-lookup"><span data-stu-id="42a42-101">title: Set form, report, and control properties TOCTitle: Set form, report, and control properties <<<<<<< HEAD ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735 ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15) ms:contentKeyID: 48542977 ms.date: 09/18/2015 ======= description: Each form, report, section, and control has property settings that you can change to alter the look or behavior of that particular item in Access 2013.</span></span>
<span data-ttu-id="42a42-102">ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735 ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15) ms:contentKeyID: 48542977 ms.date: 2018/10/16</span><span class="sxs-lookup"><span data-stu-id="42a42-102">ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735 ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15) ms:contentKeyID: 48542977 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="42a42-103">マスター mtps_version: v=office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="42a42-103">master mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="42a42-104">vbaac10.chm12286 f1_categories。</span><span class="sxs-lookup"><span data-stu-id="42a42-104">vbaac10.chm12286 f1_categories:</span></span>
- <span data-ttu-id="42a42-105">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="42a42-105">Office.Version=v15</span></span>
---

# <a name="set-form-report-and-control-properties"></a><span data-ttu-id="42a42-106">セット フォーム、レポート、およびコントロールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="42a42-106">Set form, report, and control properties</span></span>

<span data-ttu-id="42a42-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="42a42-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="42a42-p102">フォーム、レポート、フォームやレポートのセクション、およびコントロールにはそれぞれプロパティがあり、プロパティの設定値を変更すると、特定のアイテムの外観や動作を変更することができます。プロパティの表示や変更は、プロパティ シート、マクロ、または Visual Basic で行います。</span><span class="sxs-lookup"><span data-stu-id="42a42-p102">Each form, report, section, and control has property settings that you can change to alter the look or behavior of that particular item. You view and change properties by using the property sheet, macro, or Visual Basic.</span></span>

## <a name="set-properties"></a><span data-ttu-id="42a42-110">プロパティの設定</span><span class="sxs-lookup"><span data-stu-id="42a42-110">Set properties</span></span>

1. <span data-ttu-id="42a42-p103">フォームのデザイン ビューまたはレポートのデザイン ビューで、プロパティを設定するコントロール、セクション、フォーム、またはレポートを選択します。次のものが選択できます。</span><span class="sxs-lookup"><span data-stu-id="42a42-p103">In form Design view or report Design view, select the control, section, form, or report for which you want to set the property. You can select:</span></span>
    
<span data-ttu-id="42a42-113"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="42a42-113"><<<<<<< HEAD</span></span>
   - <span data-ttu-id="42a42-p104">1 つまたは複数のコントロール。複数のコントロールを選択するには、Shift キーを押しながらコントロールをクリックするか、またはマウスをクリックしてからドラッグして目的のコントロールを囲みます。複数のコントロールを選択した場合は、各コントロールで共通のプロパティのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="42a42-p104">One or more controls. To select multiple controls, hold down the SHIFT key and click the controls, or drag the mouse pointer over the controls you wish to select. If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span></span>
    
   - <span data-ttu-id="42a42-p105">1 つのセクション。目的のセクションのセクション セレクターをクリックして選択します。</span><span class="sxs-lookup"><span data-stu-id="42a42-p105">One section. Click the section selector of the section you wish to select.</span></span>
    
   - <span data-ttu-id="42a42-p106">フォーム全体またはレポート全体。フォームまたはレポートの左上隅のフォーム セレクターまたはレポート セレクターをクリックして選択します。</span><span class="sxs-lookup"><span data-stu-id="42a42-p106">The entire form or report. Click the form selector or report selector in the upper-left corner of the form or report.</span></span>

2. <span data-ttu-id="42a42-121">オブジェクトまたはセクションを右クリックし、ショートカット メニューの [**プロパティ**] をクリックしてまたはツールバーの [**プロパティ**] をクリックしてプロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="42a42-121">Display the property sheet by right-clicking the object or section and then clicking **Properties** on the shortcut menu, or by clicking **Properties** on the toolbar.</span></span>

3. <span data-ttu-id="42a42-122">値を設定するプロパティをクリックし、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="42a42-122">Click the property for which you want to set the value, and then do one of the following:</span></span>
    
   - <span data-ttu-id="42a42-123">プロパティ ボックスで、適切な設定値または式を入力します。</span><span class="sxs-lookup"><span data-stu-id="42a42-123">In the property box, type the appropriate setting or expression.</span></span>
    
   - <span data-ttu-id="42a42-124">プロパティ ボックスに矢印が含まれる場合はその矢印をクリックし、表示された一覧から値を選択します。</span><span class="sxs-lookup"><span data-stu-id="42a42-124">If the property box contains an arrow, click the arrow and then click a value in the list.</span></span>
    
   - <span data-ttu-id="42a42-125">プロパティ ボックスの右側に、[**ビルド**] ボタンが表示されている場合は、ビルダーを表示するか、ビルダーの選択を求めるダイアログ ボックスを表示をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42a42-125">If a **Build** button appears to the right of the property box, click it to display a builder or to display a dialog box giving you a choice of builders.</span></span> <span data-ttu-id="42a42-126">たとえば、いくつかのプロパティを設定するのには [コード ビルダー、マクロ ビルダー、またはクエリ ビルダーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="42a42-126">For example, you can use the Code Builder, Macro Builder, or Query Builder to set some properties.</span></span>

## <a name="tips"></a><span data-ttu-id="42a42-127">ヒント</span><span class="sxs-lookup"><span data-stu-id="42a42-127">Tips</span></span>

- <span data-ttu-id="42a42-128">Access には、入力式またはその他の long 型のプロパティの設定を表示したりするためには、[**ズーム**] ボックスが用意されています。</span><span class="sxs-lookup"><span data-stu-id="42a42-128">Microsoft Access provides a **Zoom** box for typing and viewing expressions or other long property settings.</span></span> <span data-ttu-id="42a42-129">[**ズーム**] ボックスを表示するには、プロパティ シートのプロパティ ボックスをクリックします。</span><span class="sxs-lookup"><span data-stu-id="42a42-129">To display the **Zoom** box, click a property box in the property sheet.</span></span> <span data-ttu-id="42a42-130">[SHIFT + f2 キーを押しまたは右クリックし、ショートカット メニューの [**ズーム**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42a42-130">Then press SHIFT+F2, or right-click and then click **Zoom** on the shortcut menu.</span></span>
=======
   - <span data-ttu-id="42a42-131">1 つまたは複数のコントロール。</span><span class="sxs-lookup"><span data-stu-id="42a42-131">One or more controls.</span></span> <span data-ttu-id="42a42-132">複数のコントロールを選択、SHIFT キーを押しながら、コントロールを選択またはを選択するコントロールをマウス ポインターをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="42a42-132">To select multiple controls, hold down the SHIFT key and choose the controls, or drag the mouse pointer over the controls you wish to select.</span></span> <span data-ttu-id="42a42-133">複数のコントロールを選択すると、プロパティ シートで選択したコントロールに共通するプロパティのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="42a42-133">If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span></span>
    
   - <span data-ttu-id="42a42-134">1 つのセクション。</span><span class="sxs-lookup"><span data-stu-id="42a42-134">One section.</span></span> <span data-ttu-id="42a42-135">選択するセクションのセクション セレクターを選択します。</span><span class="sxs-lookup"><span data-stu-id="42a42-135">Choose the section selector of the section you wish to select.</span></span>
    
   - <span data-ttu-id="42a42-136">フォーム全体またはレポート全体。</span><span class="sxs-lookup"><span data-stu-id="42a42-136">The entire form or report.</span></span> <span data-ttu-id="42a42-137">フォームまたはレポートの左上隅のフォーム セレクターまたはレポート セレクターを選択します。</span><span class="sxs-lookup"><span data-stu-id="42a42-137">Choose the form selector or report selector in the upper-left corner of the form or report.</span></span>

2. <span data-ttu-id="42a42-138">オブジェクトまたはセクションを右クリックし、[ショートカット] メニュー**のプロパティ**を選択またはツールバーの**プロパティ**を選択してプロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="42a42-138">Display the property sheet by right-clicking the object or section and then choosing **Properties** on the shortcut menu, or by choosing **Properties** on the toolbar.</span></span>

3. <span data-ttu-id="42a42-139">プロパティの値を設定する] を選択し、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="42a42-139">Choose the property for which you want to set the value, and then do one of the following:</span></span>
    
   - <span data-ttu-id="42a42-140">プロパティ ボックスで、適切な設定値または式を入力します。</span><span class="sxs-lookup"><span data-stu-id="42a42-140">In the property box, type the appropriate setting or expression.</span></span>
    
   - <span data-ttu-id="42a42-141">プロパティ ボックスに矢印が含まれている場合、矢印を選択し、リストで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="42a42-141">If the property box contains an arrow, choose the arrow and then choose a value in the list.</span></span>
    
   - <span data-ttu-id="42a42-142">プロパティ ボックスの右側に、[**ビルド**] ボタンが表示されている場合は、ビルダーを表示するか、ビルダーの選択を求めるダイアログ ボックスを表示を選択します。</span><span class="sxs-lookup"><span data-stu-id="42a42-142">If a **Build** button appears to the right of the property box, choose it to display a builder or to display a dialog box giving you a choice of builders.</span></span> <span data-ttu-id="42a42-143">たとえば、いくつかのプロパティを設定するのには [コード ビルダー、マクロ ビルダー、またはクエリ ビルダーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="42a42-143">For example, you can use the Code Builder, Macro Builder, or Query Builder to set some properties.</span></span>

## <a name="tips"></a><span data-ttu-id="42a42-144">ヒント</span><span class="sxs-lookup"><span data-stu-id="42a42-144">Tips</span></span>

- <span data-ttu-id="42a42-145">Access には、入力式またはその他の long 型のプロパティの設定を表示したりするためには、[**ズーム**] ボックスが用意されています。</span><span class="sxs-lookup"><span data-stu-id="42a42-145">Microsoft Access provides a **Zoom** box for typing and viewing expressions or other long property settings.</span></span> <span data-ttu-id="42a42-146">[**ズーム**] ボックスを表示するには、プロパティ シートのプロパティ ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="42a42-146">To display the **Zoom** box, choose a property box in the property sheet.</span></span> <span data-ttu-id="42a42-147">SHIFT + f2 キー、または右クリックしを押し、ショートカット メニューの [**拡大/縮小**をします。</span><span class="sxs-lookup"><span data-stu-id="42a42-147">Press SHIFT+F2, or right-click, and then choose **Zoom** on the shortcut menu.</span></span>
>>>>>>> <span data-ttu-id="42a42-148">master</span><span class="sxs-lookup"><span data-stu-id="42a42-148">master</span></span>

- <span data-ttu-id="42a42-149">コントロールの " **ControlSource** /コントロール ソース" プロパティを設定するには、そのコントロールで設定値を入力します。</span><span class="sxs-lookup"><span data-stu-id="42a42-149">You can set the **ControlSource** property for some controls by typing the property setting in the control itself.</span></span>

- <span data-ttu-id="42a42-150">コントロールの種類ごとに既定のプロパティを変更して、作成するコントロールに別の既定値が設定されるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="42a42-150">You can change the default property settings for a type of control so that future controls you create will have the new default settings.</span></span>

<span data-ttu-id="42a42-151"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="42a42-151"><<<<<<< HEAD</span></span>
- <span data-ttu-id="42a42-152">連結コントロールのプロパティの設定値が、基になっているテーブルまたはクエリのフィールドの対応する設定値と一致しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="42a42-152">The property settings of a bound control might not match the corresponding settings in the field in the underlying table or query to which the control is bound.</span></span> <span data-ttu-id="42a42-153">設定値が異なる場合は、通常、テーブルやクエリの設定値よりも、フォームやレポートの設定値が優先されます。</span><span class="sxs-lookup"><span data-stu-id="42a42-153">If the settings are different, the form or report settings typically override those in the table or query.</span></span> <span data-ttu-id="42a42-154">プロパティを継承させる方法の詳細については、「コントロール プロパティと基になるフィールドのプロパティとの関係」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="42a42-154">For more information about how properties are inherited, see How control properties relate to properties in their underlying fields.</span></span>
=======
- <span data-ttu-id="42a42-155">連結コントロールのプロパティの設定値が、基になっているテーブルまたはクエリのフィールドの対応する設定値と一致しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="42a42-155">The property settings of a bound control might not match the corresponding settings in the field in the underlying table or query to which the control is bound.</span></span> <span data-ttu-id="42a42-156">設定値が異なる場合は、通常、テーブルやクエリの設定値よりも、フォームやレポートの設定値が優先されます。</span><span class="sxs-lookup"><span data-stu-id="42a42-156">If the settings are different, the form or report settings typically override those in the table or query.</span></span>
>>>>>>> <span data-ttu-id="42a42-157">master</span><span class="sxs-lookup"><span data-stu-id="42a42-157">master</span></span>

