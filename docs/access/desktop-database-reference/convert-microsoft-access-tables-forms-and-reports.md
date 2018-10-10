---
title: Access のテーブル、フォーム、およびレポートの変換
TOCTitle: Convert Microsoft Access Tables, Forms, and Reports
ms:assetid: cc170e62-a663-60e8-4446-07a7a874b747
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834413(v=office.15)
ms:contentKeyID: 48547731
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5187104
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6f3928f3f0378c32737bc4881779b113c5d03774
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479672"
---
# <a name="convert-microsoft-access-tables-forms-and-reports"></a><span data-ttu-id="fa95c-102">Access のテーブル、フォーム、およびレポートの変換</span><span class="sxs-lookup"><span data-stu-id="fa95c-102">Convert Microsoft Access Tables, Forms, and Reports</span></span>

<span data-ttu-id="fa95c-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa95c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fa95c-104">Microsoft Access 2002 で導入されたいくつかの変更、バージョン 1 の動作に影響を与える可能性があります。*x*または 2.0 のアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="fa95c-104">Several changes introduced by Microsoft Access 2002 might affect the behavior of your version 1.*x* or 2.0 applications.</span></span> <span data-ttu-id="fa95c-105">次のセクションでは、これらの変更の詳細についてを説明します。</span><span class="sxs-lookup"><span data-stu-id="fa95c-105">The following sections provide more information about those changes.</span></span>

## <a name="indexes-and-relationships"></a><span data-ttu-id="fa95c-106">インデックスとリレーションシップ</span><span class="sxs-lookup"><span data-stu-id="fa95c-106">Indexes and Relationships</span></span>

<span data-ttu-id="fa95c-p102">Microsoft Access テーブルに含めることができるインデックスは最大 32 個です。リレーションシップの "多" 側の複雑なテーブルでは、インデックスの制限値を超える可能性があり、このようなテーブルを含むデータベースは、変換することができません。Microsoft Access データベース エンジンはリレーションシップの両側のテーブルにインデックスを作成します。データベースを変換できない場合は、いくつかのリレーションシップを削除してからデータベースを変換し直してください。</span><span class="sxs-lookup"><span data-stu-id="fa95c-p102">A Microsoft Access table can contain up to 32 indexes. Very complex tables that are a part of many relationships may exceed the index limit, and you won't be able to convert the database that contains these tables. The Microsoft Access database engine creates indexes on both sides of relationships between tables. If your database won't convert, delete some relationships and try again to convert the database.</span></span>

## <a name="the-limittolist-property-of-combo-boxes"></a><span data-ttu-id="fa95c-111">コンボ ボックスの "LimitToList/入力チェック" プロパティ</span><span class="sxs-lookup"><span data-stu-id="fa95c-111">The LimitToList Property of Combo Boxes</span></span>

<span data-ttu-id="fa95c-112">**Microsoft Access 2002 以降では、コンボ ボックス Null**値を受け入れるに**True** (-1)、**このプロパティ**が設定されている場合、リストに**Null**値が含まれているかどうか。</span><span class="sxs-lookup"><span data-stu-id="fa95c-112">In Microsoft Access 2002 or later, combo boxes accept **Null** values when the **LimitToList** property is set to **True** (–1), whether or not the list contains **Null** values.</span></span> <span data-ttu-id="fa95c-113">バージョン 2.0 では、**プロパティを**True**に設定**を持つコンボ ボックスを受け付けません**Null**値リストには、 **Null**値が含まれている場合を除き、します。</span><span class="sxs-lookup"><span data-stu-id="fa95c-113">In version 2.0, a combo box that has the **LimitToList** property set to **True** won't accept a **Null** value unless the list contains a **Null** value.</span></span> <span data-ttu-id="fa95c-114">コンボ ボックスを使用して**Null**値を入力できないようにする場合は、 **[はい]** に、テーブルのフィールドの**ために必要な**プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="fa95c-114">If you want to prevent users from entering a **Null** value by using a combo box, set the **Required** property of the field in the table to **Yes**.</span></span>

## <a name="menus-and-in-place-activation-of-ole-objects"></a><span data-ttu-id="fa95c-115">OLE オブジェクトのメニューとインプレース アクティブ化</span><span class="sxs-lookup"><span data-stu-id="fa95c-115">Menus and In-Place Activation of OLE Objects</span></span>

<span data-ttu-id="fa95c-116">OLE オブジェクトをインプレース アクティブ化しているときでもその他の機能を使用できるように、いくつかのメニュー コマンドは、OLE サーバーがアクティブになっても置き換えられないメニューに移動されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fa95c-116">In order to make additional functionality available to you while activating OLE objects in place, some menu commands may have been moved to a menu that isn't replaced when you activate an OLE server.</span></span>

<span data-ttu-id="fa95c-p104">この変更は、以前のバージョンのアプリケーションのマクロを変換するときには影響しません。以前のバージョンのマクロで、OLE サーバーがアクティブになったときに "DoMenuItem/メニューの実行" アクションを使って Version 2.0 のメニュー コマンドを実行していた場合、アプリケーションを変換すると、Version 2.0 のコマンドは新しいバージョンの Access の同等のコマンドと置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="fa95c-p104">Macros in your converted application that use a DoMenuItem action to carry out a version 2.0 menu command when a component is activated won't be affected by the changes. Version 2.0 commands are mapped to their equivalents in later versions of Microsoft Access.</span></span>

## <a name="referencing-a-control-on-a-read-only-form"></a><span data-ttu-id="fa95c-119">読み取り専用フォームのコントロールの参照</span><span class="sxs-lookup"><span data-stu-id="fa95c-119">Referencing a Control on a Read-Only Form</span></span>

<span data-ttu-id="fa95c-p105">Access 2002 以降では、空のレコード ソースに連結されている読み取り専用フォームのコントロールの値を、式を使って参照することはできません。以前のバージョンでは、このような式は **Null** 値を返しました。読み取り専用フォームのコントロールを参照するときは、フォームのレコード ソースにレコードが含まれているかどうかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa95c-p105">In Microsoft Access 2002 or later, you can't use an expression to refer to the value of a control on a read-only form that's bound to an empty record source. In previous versions, the expression returns a **Null** value. Before you reference a control on a read-only form, you should make sure that the form's record source contains records.</span></span>

## <a name="date-fields-and-data-entry"></a><span data-ttu-id="fa95c-123">日付フィールドへのデータ入力</span><span class="sxs-lookup"><span data-stu-id="fa95c-123">Date Fields and Data Entry</span></span>

<span data-ttu-id="fa95c-124">フォームまたはテーブルのデータシートで、日付型のフィールドに**3/3**を入力すると Access 2002 以降で現在の年は自動的に追加します。</span><span class="sxs-lookup"><span data-stu-id="fa95c-124">If you enter **3/3** in a field of type Date on a form or a table datasheet, the current year is automatically added in Microsoft Access 2002 or later.</span></span> <span data-ttu-id="fa95c-125">ただし、入力する場合は**3/3/** 同じフィールドに、Microsoft Access がエラー メッセージを返します。</span><span class="sxs-lookup"><span data-stu-id="fa95c-125">However, if you enter **3/3/** in the same field, Microsoft Access returns an error message.</span></span> <span data-ttu-id="fa95c-126">Microsoft Access は適切な形式に、日付を変換できるように、最後の日付の区切り記号を省略する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa95c-126">You must omit the last date delimiter so that Microsoft Access can translate the date into the proper format.</span></span>

## <a name="buttons-created-with-the-command-button-wizard"></a><span data-ttu-id="fa95c-127">コマンド ボタン ウィザードで作成したボタン</span><span class="sxs-lookup"><span data-stu-id="fa95c-127">Buttons Created with the Command Button Wizard</span></span>

<span data-ttu-id="fa95c-128">Access Version 2.0 または 7.0 のコマンド ボタン ウィザードを使って、別のアプリケーションを呼び出すコードが記述されたボタンを作成した場合、そのボタンを削除し、Access 2002 以降のコマンド ボタン ウィザードを使って作成し直す必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa95c-128">If you used the Command Button Wizard in version 2.0 or 7.0 of Microsoft Access to generate code that called another application, you should delete the button and re-create it by using the Command Button Wizard in Microsoft Access 2002 or later.</span></span>

## <a name="form-and-report-class-modules"></a><span data-ttu-id="fa95c-129">フォームおよびレポートのクラス モジュール</span><span class="sxs-lookup"><span data-stu-id="fa95c-129">Form and Report Class Modules</span></span>

<span data-ttu-id="fa95c-130">以前のバージョンの Microsoft Access 2002 での**フォーム**および**レポート**のオブジェクトが関連付けられているクラス モジュールのオブジェクトの背後のコードがない場合でも。</span><span class="sxs-lookup"><span data-stu-id="fa95c-130">In versions of Microsoft Access prior to 2002, **Form** and **Report** objects have associated class modules even if there's no code behind the object.</span></span> <span data-ttu-id="fa95c-131">Microsoft Access 2002 以降では、 **false を指定**する**フォームやレポートのプロパティ**を設定できます。</span><span class="sxs-lookup"><span data-stu-id="fa95c-131">In Microsoft Access 2002 or later, you can set a form's or report's **HasModule** property to **False**.</span></span> <span data-ttu-id="fa95c-132">**HasModule**プロパティを**False**に設定するときに必要なディスク領域が少なく、フォームまたはレポートと読み込みが速くなります、関連付けられたクラス モジュールがある不要になったため。</span><span class="sxs-lookup"><span data-stu-id="fa95c-132">When you set the **HasModule** property to **False**, the form or report will take up less disk space and will load faster because it will no longer have an associated class module.</span></span>

## <a name="converted-version-20-report-has-different-margins"></a><span data-ttu-id="fa95c-133">変換された Version 2.0 のレポートでの余白の相違</span><span class="sxs-lookup"><span data-stu-id="fa95c-133">Converted Version 2.0 Report Has Different Margins</span></span>

<span data-ttu-id="fa95c-p108">Access 2.0 から変換された Access 2002 以降のレポートの印刷またはプレビューを試みたときに、"0" に設定した余白がレポートにあると問題が発生する場合があります。Access 2.0 のレポートを変換する場合、余白が 0 に設定されず、既定のプリンターで有効な最小の余白が設定されます。これは、レポートのデータがプリンターで印刷できない位置に印刷されるのを防ぐためです。</span><span class="sxs-lookup"><span data-stu-id="fa95c-p108">You may encounter problems when trying to print or preview a report in Microsoft Access 2002 or later that has been converted from Microsoft Access 2.0 if the report has some margins set to 0. When you convert a Microsoft Access 2.0 report, margins aren't set to 0; they are instead set to the minimum margin that's valid for the default printer. This prevents the report from printing data in the unprintable region of the printer.</span></span>

<span data-ttu-id="fa95c-137">この問題を解決するには、列幅と既定値の余白の幅を加えると用紙の幅と同じかまたはそれに収まる幅になるように、レポートの列幅、列の間隔、または列数を減らします。</span><span class="sxs-lookup"><span data-stu-id="fa95c-137">To resolve this problem, reduce the column width, column spacing, or number of columns in the report so that the width of the columns plus the width of the default margins is equal to or less than the width of your paper.</span></span>

## <a name="cant-use-the-format-property-to-distinguish-null-values-and-zero-length-strings"></a><span data-ttu-id="fa95c-138">値および長さ 0 の文字列の識別ができない "Format/書式" プロパティ</span><span class="sxs-lookup"><span data-stu-id="fa95c-138">Can't Use the Format Property to Distinguish Null Values and Zero-Length Strings</span></span>

<span data-ttu-id="fa95c-139">バージョン 1 です。**Null**値と長さ 0 の文字列に異なる値を表示するコントロールの**書式**プロパティを使用するには*x*と 2.0 では、("")。</span><span class="sxs-lookup"><span data-stu-id="fa95c-139">In versions 1.*x* and 2.0, you can use the **Format** property of a control to display different values for **Null** values and zero-length strings (" ").</span></span> <span data-ttu-id="fa95c-140">Microsoft Access 2002 以降では、 **Null**値と長さ 0 の文字列では、フォーム上のコントロールを区別するに、 **Null**値である場合をテストする式をコントロールの**ControlSource**プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="fa95c-140">In Microsoft Access 2002 or later, to distinguish between **Null** values and zero-length strings in a control on a form, set the control's **ControlSource** property to an expression that tests for the **Null** value case.</span></span> <span data-ttu-id="fa95c-141">などのコントロールに"Null"または"ZLS"を表示するのには次のように、[**コントロール ソース**] プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="fa95c-141">For example, to display "Null" or "ZLS" in a control, set its **ControlSource** property to the following expression:</span></span>

<span data-ttu-id="fa95c-142">\=IIf (IsNull (\[MyControl\]) の書式を設定、"Null"(\[MyControl\]、"@ です。ZLS"))</span><span class="sxs-lookup"><span data-stu-id="fa95c-142">\=IIf(IsNull(\[MyControl\]), "Null", Format(\[MyControl\], "@;ZLS"))</span></span>

