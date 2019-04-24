---
title: access のテーブル、フォーム、およびレポートを変換する
TOCTitle: Convert Microsoft Access tables, forms, and reports
description: Microsoft access 2002 で導入された変更は、バージョン 1. x または2.0 アプリケーションの動作に影響を与える可能性があります。
ms:assetid: cc170e62-a663-60e8-4446-07a7a874b747
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834413(v=office.15)
ms:contentKeyID: 48547731
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5187104
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9c1ff7584269ce073a805edf8710bb3ea4eb1a36
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295584"
---
# <a name="convert-microsoft-access-tables-forms-and-reports"></a><span data-ttu-id="b3c13-103">access のテーブル、フォーム、およびレポートを変換する</span><span class="sxs-lookup"><span data-stu-id="b3c13-103">Convert Microsoft Access tables, forms, and reports</span></span>

<span data-ttu-id="b3c13-104">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3c13-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b3c13-p101">Access 2002 で導入された変更点が、Access Version 1.1 または 2.0 のアプリケーションの動作に影響を与える場合があります。以下に、変更の詳細を説明します。</span><span class="sxs-lookup"><span data-stu-id="b3c13-p101">Several changes introduced by Microsoft Access 2002 might affect the behavior of your version 1.*x* or 2.0 applications. The following sections provide more information about those changes.</span></span>

## <a name="indexes-and-relationships"></a><span data-ttu-id="b3c13-107">インデックスとリレーションシップ</span><span class="sxs-lookup"><span data-stu-id="b3c13-107">Indexes and relationships</span></span>

<span data-ttu-id="b3c13-p102">Microsoft Access テーブルに含めることができるインデックスは最大 32 個です。リレーションシップの "多" 側の複雑なテーブルでは、インデックスの制限値を超える可能性があり、このようなテーブルを含むデータベースは、変換することができません。Microsoft Access データベース エンジンはリレーションシップの両側のテーブルにインデックスを作成します。データベースを変換できない場合は、いくつかのリレーションシップを削除してからデータベースを変換し直してください。</span><span class="sxs-lookup"><span data-stu-id="b3c13-p102">A Microsoft Access table can contain up to 32 indexes. Very complex tables that are a part of many relationships may exceed the index limit, and you won't be able to convert the database that contains these tables. The Microsoft Access database engine creates indexes on both sides of relationships between tables. If your database won't convert, delete some relationships and try again to convert the database.</span></span>

## <a name="the-limittolist-property-of-combo-boxes"></a><span data-ttu-id="b3c13-112">コンボボックスの "LimitToList/入力チェック" プロパティ</span><span class="sxs-lookup"><span data-stu-id="b3c13-112">The LimitToList property of combo boxes</span></span>

<span data-ttu-id="b3c13-113">access 2002 以降では、"LimitToList/入力**チェック**" プロパティが**True** (-1) に設定されている場合、またはリストに**null**値が含まれている場合、このコンボボックスは**null**値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="b3c13-113">In Microsoft Access 2002 or later, combo boxes accept **Null** values when the **LimitToList** property is set to **True** (–1), whether or not the list contains **Null** values.</span></span> <span data-ttu-id="b3c13-114">In version 2.0, a combo box that has the **LimitToList** property set to **True** won't accept a **Null** value unless the list contains a **Null** value.</span><span class="sxs-lookup"><span data-stu-id="b3c13-114">In version 2.0, a combo box that has the **LimitToList** property set to **True** won't accept a **Null** value unless the list contains a **Null** value.</span></span> <span data-ttu-id="b3c13-115">If you want to prevent users from entering a **Null** value by using a combo box, set the **Required** property of the field in the table to **Yes**.</span><span class="sxs-lookup"><span data-stu-id="b3c13-115">If you want to prevent users from entering a **Null** value by using a combo box, set the **Required** property of the field in the table to **Yes**.</span></span>

## <a name="menus-and-in-place-activation-of-ole-objects"></a><span data-ttu-id="b3c13-116">OLE オブジェクトのメニューとインプレースアクティブ化</span><span class="sxs-lookup"><span data-stu-id="b3c13-116">Menus and in-place activation of OLE objects</span></span>

<span data-ttu-id="b3c13-117">ole オブジェクトを適切にアクティブ化しているときに追加の機能を使用できるように、一部のメニューコマンドは、ole サーバーをアクティブ化したときに置き換えられないメニューに移動されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="b3c13-117">To make additional functionality available to you while activating OLE objects in place, some menu commands may have been moved to a menu that isn't replaced when you activate an OLE server.</span></span>

<span data-ttu-id="b3c13-p104">この変更は、以前のバージョンのアプリケーションのマクロを変換するときには影響しません。以前のバージョンのマクロで、OLE サーバーがアクティブになったときに "DoMenuItem/メニューの実行" アクションを使って Version 2.0 のメニュー コマンドを実行していた場合、アプリケーションを変換すると、Version 2.0 のコマンドは新しいバージョンの Access の同等のコマンドと置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="b3c13-p104">Macros in your converted application that use a DoMenuItem action to carry out a version 2.0 menu command when a component is activated won't be affected by the changes. Version 2.0 commands are mapped to their equivalents in later versions of Microsoft Access.</span></span>

## <a name="referencing-a-control-on-a-read-only-form"></a><span data-ttu-id="b3c13-120">読み取り専用フォームでコントロールを参照する</span><span class="sxs-lookup"><span data-stu-id="b3c13-120">Referencing a control on a read-only form</span></span>

<span data-ttu-id="b3c13-p105">Access 2002 以降では、空のレコード ソースに連結されている読み取り専用フォームのコントロールの値を、式を使って参照することはできません。以前のバージョンでは、このような式は **Null** 値を返しました。読み取り専用フォームのコントロールを参照するときは、フォームのレコード ソースにレコードが含まれているかどうかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3c13-p105">In Microsoft Access 2002 or later, you can't use an expression to refer to the value of a control on a read-only form that's bound to an empty record source. In previous versions, the expression returns a **Null** value. Before you reference a control on a read-only form, you should make sure that the form's record source contains records.</span></span>

## <a name="date-fields-and-data-entry"></a><span data-ttu-id="b3c13-124">日付フィールドとデータ入力</span><span class="sxs-lookup"><span data-stu-id="b3c13-124">Date fields and data entry</span></span>

<span data-ttu-id="b3c13-p106">If you enter **3/3** in a field of type Date on a form or a table datasheet, the current year is automatically added in Microsoft Access 2002 or later. However, if you enter **3/3/** in the same field, Microsoft Access returns an error message. You must omit the last date delimiter so that Microsoft Access can translate the date into the proper format.</span><span class="sxs-lookup"><span data-stu-id="b3c13-p106">If you enter **3/3** in a field of type Date on a form or a table datasheet, the current year is automatically added in Microsoft Access 2002 or later. However, if you enter **3/3/** in the same field, Microsoft Access returns an error message. You must omit the last date delimiter so that Microsoft Access can translate the date into the proper format.</span></span>

## <a name="buttons-created-with-the-command-button-wizard"></a><span data-ttu-id="b3c13-128">コマンドボタンウィザードで作成されたボタン</span><span class="sxs-lookup"><span data-stu-id="b3c13-128">Buttons created with the Command Button Wizard</span></span>

<span data-ttu-id="b3c13-129">Access Version 2.0 または 7.0 のコマンド ボタン ウィザードを使って、別のアプリケーションを呼び出すコードが記述されたボタンを作成した場合、そのボタンを削除し、Access 2002 以降のコマンド ボタン ウィザードを使って作成し直す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3c13-129">If you used the Command Button Wizard in version 2.0 or 7.0 of Microsoft Access to generate code that called another application, you should delete the button and re-create it by using the Command Button Wizard in Microsoft Access 2002 or later.</span></span>

## <a name="form-and-report-class-modules"></a><span data-ttu-id="b3c13-130">フォームおよびレポートのクラスモジュール</span><span class="sxs-lookup"><span data-stu-id="b3c13-130">Form and report class modules</span></span>

<span data-ttu-id="b3c13-p107">In versions of Microsoft Access prior to 2002, **Form** and **Report** objects have associated class modules even if there's no code behind the object. In Microsoft Access 2002 or later, you can set a form's or report's **HasModule** property to **False**. When you set the **HasModule** property to **False**, the form or report will take up less disk space and will load faster because it will no longer have an associated class module.</span><span class="sxs-lookup"><span data-stu-id="b3c13-p107">In versions of Microsoft Access prior to 2002, **Form** and **Report** objects have associated class modules even if there's no code behind the object. In Microsoft Access 2002 or later, you can set a form's or report's **HasModule** property to **False**. When you set the **HasModule** property to **False**, the form or report will take up less disk space and will load faster because it will no longer have an associated class module.</span></span>

## <a name="converted-version-20-report-has-different-margins"></a><span data-ttu-id="b3c13-134">変換されたバージョン2.0 レポートの余白が異なる</span><span class="sxs-lookup"><span data-stu-id="b3c13-134">Converted version 2.0 report has different margins</span></span>

<span data-ttu-id="b3c13-p108">Access 2.0 から変換された Access 2002 以降のレポートの印刷またはプレビューを試みたときに、"0" に設定した余白がレポートにあると問題が発生する場合があります。Access 2.0 のレポートを変換する場合、余白が 0 に設定されず、既定のプリンターで有効な最小の余白が設定されます。これは、レポートのデータがプリンターで印刷できない位置に印刷されるのを防ぐためです。</span><span class="sxs-lookup"><span data-stu-id="b3c13-p108">You may encounter problems when trying to print or preview a report in Microsoft Access 2002 or later that has been converted from Microsoft Access 2.0 if the report has some margins set to 0. When you convert a Microsoft Access 2.0 report, margins aren't set to 0; they are instead set to the minimum margin that's valid for the default printer. This prevents the report from printing data in the unprintable region of the printer.</span></span>

<span data-ttu-id="b3c13-138">この問題を解決するには、列幅と既定値の余白の幅を加えると用紙の幅と同じかまたはそれに収まる幅になるように、レポートの列幅、列の間隔、または列数を減らします。</span><span class="sxs-lookup"><span data-stu-id="b3c13-138">To resolve this problem, reduce the column width, column spacing, or number of columns in the report so that the width of the columns plus the width of the default margins is equal to or less than the width of your paper.</span></span>

## <a name="cant-use-the-format-property-to-distinguish-null-values-and-zero-length-strings"></a><span data-ttu-id="b3c13-139">書式プロパティを使用して Null 値と長さ0の文字列を区別することはできません</span><span class="sxs-lookup"><span data-stu-id="b3c13-139">Can't use the Format property to distinguish Null values and zero-length strings</span></span>

<span data-ttu-id="b3c13-140">バージョン1。*x*および2.0 では、コントロールの " **Format/書式**" プロパティを使用して、 **Null**値と長さ0の文字列 ("") に異なる値を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="b3c13-140">In versions 1.*x* and 2.0, you can use the **Format** property of a control to display different values for **Null** values and zero-length strings (" ").</span></span> <span data-ttu-id="b3c13-141">In Microsoft Access 2002 or later, to distinguish between **Null** values and zero-length strings in a control on a form, set the control's **ControlSource** property to an expression that tests for the **Null** value case.</span><span class="sxs-lookup"><span data-stu-id="b3c13-141">In Microsoft Access 2002 or later, to distinguish between **Null** values and zero-length strings in a control on a form, set the control's **ControlSource** property to an expression that tests for the **Null** value case.</span></span> <span data-ttu-id="b3c13-142">For example, to display "Null" or "ZLS" in a control, set its **ControlSource** property to the following expression:</span><span class="sxs-lookup"><span data-stu-id="b3c13-142">For example, to display "Null" or "ZLS" in a control, set its **ControlSource** property to the following expression:</span></span>

`=IIf(IsNull([MyControl]), "Null", Format([MyControl], "@;ZLS"))`

