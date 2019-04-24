---
title: StopAllMacros マクロ アクション
TOCTitle: StopAllMacros macro action
ms:assetid: 6afbf906-03b8-6e68-bbc9-7a4b141cf1c5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195440(v=office.15)
ms:contentKeyID: 48545442
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm104968
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4e44182dd4290b05a2cfc8fabdf9240819f4b7aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314477"
---
# <a name="stopallmacros-macro-action"></a><span data-ttu-id="727bc-102">StopAllMacros マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="727bc-102">StopAllMacros macro action</span></span>


<span data-ttu-id="727bc-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="727bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="727bc-104">"StopAllMacros/全マクロの中止" アクションを使用すると、現在実行中のすべてのマクロを中止できます。</span><span class="sxs-lookup"><span data-stu-id="727bc-104">You can use the **StopAllMacros** action to stop all macros that are currently running.</span></span>

## <a name="setting"></a><span data-ttu-id="727bc-105">Setting</span><span class="sxs-lookup"><span data-stu-id="727bc-105">Setting</span></span>

<span data-ttu-id="727bc-106">"StopAllMacros/全マクロの中止" アクションには、引数はありません。</span><span class="sxs-lookup"><span data-stu-id="727bc-106">The **StopAllMacros** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="727bc-107">注釈</span><span class="sxs-lookup"><span data-stu-id="727bc-107">Remarks</span></span>

<span data-ttu-id="727bc-p101">通常、このアクションは、エラーが発生したためにすべてのマクロを中止する必要が生じた場合に使用します。このアクションが定義されているマクロ内のアクション行に条件式を指定できます。条件式の評価が True (–1) の場合、Microsoft Access はすべてのマクロを中止します。</span><span class="sxs-lookup"><span data-stu-id="727bc-p101">You typically use this action when an error condition makes it necessary to stop all macros. You can use a conditional expression in the macro's action row that contains this action. When the expression evaluates to **True** (–1), Microsoft Access stops all macros.</span></span>

<span data-ttu-id="727bc-p102">For example, you might have a macro that displays a message box as one of a number of complex actions, including running other macros. If the user clicks **Cancel** in this message box, the **StopAllMacros** action can stop all the macros that are running.</span><span class="sxs-lookup"><span data-stu-id="727bc-p102">For example, you might have a macro that displays a message box as one of a number of complex actions, including running other macros. If the user clicks **Cancel** in this message box, the **StopAllMacros** action can stop all the macros that are running.</span></span>

<span data-ttu-id="727bc-113">If a macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopAllMacros** action automatically turns them back on.</span><span class="sxs-lookup"><span data-stu-id="727bc-113">If a macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopAllMacros** action automatically turns them back on.</span></span>

<span data-ttu-id="727bc-114">このアクションは Visual Basic for Applications (VBA) モジュールでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="727bc-114">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

