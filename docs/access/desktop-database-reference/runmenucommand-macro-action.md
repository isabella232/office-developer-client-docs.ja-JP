---
title: RunMenuCommand マクロ アクション
TOCTitle: RunMenuCommand macro action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c2b5a19b7a92fb68dfb774afeec5cd6ba456f38d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306504"
---
# <a name="runmenucommand-macro-action"></a><span data-ttu-id="ef14d-102">RunMenuCommand マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="ef14d-102">RunMenuCommand macro action</span></span>

<span data-ttu-id="ef14d-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef14d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ef14d-104">"RunMenuCommand/メニューコマンドの実行" アクションを使用すると、組み込みの Microsoft Access コマンドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="ef14d-104">You can use the **RunMenuCommand** action to run a built-in Microsoft Access command.</span></span>

## <a name="setting"></a><span data-ttu-id="ef14d-105">Setting</span><span class="sxs-lookup"><span data-stu-id="ef14d-105">Setting</span></span>

<span data-ttu-id="ef14d-106">"RunMenuCommand/メニューコマンドの実行" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ef14d-106">The **RunMenuCommand** action has the following action argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef14d-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="ef14d-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ef14d-108">説明</span><span class="sxs-lookup"><span data-stu-id="ef14d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef14d-109"><strong>Command</strong></span><span class="sxs-lookup"><span data-stu-id="ef14d-109"><strong>Command</strong></span></span></p></td>
<td><p><span data-ttu-id="ef14d-p101">実行するコマンドの名前を指定します。[<strong>コマンド</strong>] ボックスには、Access の使用可能な組み込みのコマンドが五十音順で表示されます。この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="ef14d-p101">The name of the command you want to run. The <strong>Command</strong> box shows the available built-in commands in Access, in alphabetical order. This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="ef14d-113">注釈</span><span class="sxs-lookup"><span data-stu-id="ef14d-113">Remarks</span></span>

<span data-ttu-id="ef14d-114">"RunMenuCommand/メニューコマンドの実行" アクションを使用すると、Access コマンドをカスタム メニュー バー、グローバル メニュー バー、カスタム ショートカット メニュー、またはグローバル ショートカット メニューから実行できます。</span><span class="sxs-lookup"><span data-stu-id="ef14d-114">You can use the **RunMenuCommand** action to run an Access command from a custom menu bar, global menu bar, custom shortcut menu, or global shortcut menu.</span></span>

<span data-ttu-id="ef14d-115">You can use the **RunMenuCommand** action in a macro with conditional expressions to run a command depending on certain conditions.</span><span class="sxs-lookup"><span data-stu-id="ef14d-115">You can use the **RunMenuCommand** action in a macro with conditional expressions to run a command depending on certain conditions.</span></span>

> [!NOTE]
> <span data-ttu-id="ef14d-p102">Clicking the **File** tab and then clicking **Recent** shows the most recently used databases. You can click one of these databases instead of clicking **Open**. These database items don't appear in the drop-down list box for the **Command** argument, and aren't available by using the **RunMenuCommand** action in a macro.</span><span class="sxs-lookup"><span data-stu-id="ef14d-p102">Clicking the **File** tab and then clicking **Recent** shows the most recently used databases. You can click one of these databases instead of clicking **Open**. These database items don't appear in the drop-down list box for the **Command** argument, and aren't available by using the **RunMenuCommand** action in a macro.</span></span>

<span data-ttu-id="ef14d-p103">When you convert an Access database from a previous version of Access, some commands may no longer be available. A command may have been renamed, moved to a different menu, or may no longer be available in Access. The **DoMenuItem** actions for such commands can't be converted to **RunMenuCommand** actions. When you open the macro, Access will display a **RunMenuCommand** action with a blank **Command** argument for such commands. You must edit the macro and enter a valid command argument, or delete the **RunMenuCommand** action.</span><span class="sxs-lookup"><span data-stu-id="ef14d-p103">When you convert an Access database from a previous version of Access, some commands may no longer be available. A command may have been renamed, moved to a different menu, or may no longer be available in Access. The **DoMenuItem** actions for such commands can't be converted to **RunMenuCommand** actions. When you open the macro, Access will display a **RunMenuCommand** action with a blank **Command** argument for such commands. You must edit the macro and enter a valid command argument, or delete the **RunMenuCommand** action.</span></span>

<span data-ttu-id="ef14d-p104">To run the **RunMenuCommand** action in a Visual Basic for Applications (VBA) module, use the **RunCommand** method of the **Application** object. (This is equivalent to the **RunCommand** method of the **DoCmd** object.)</span><span class="sxs-lookup"><span data-stu-id="ef14d-p104">To run the **RunMenuCommand** action in a Visual Basic for Applications (VBA) module, use the **RunCommand** method of the **Application** object. (This is equivalent to the **RunCommand** method of the **DoCmd** object.)</span></span>

