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
ms.openlocfilehash: 34dbfc3504744dd446a018e797ebacfb79066d96
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923351"
---
# <a name="stopallmacros-macro-action"></a><span data-ttu-id="715db-102">StopAllMacros マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="715db-102">StopAllMacros macro action</span></span>


<span data-ttu-id="715db-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="715db-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="715db-104">**中止**を使用すると、現在実行されているすべてのマクロを停止します。</span><span class="sxs-lookup"><span data-stu-id="715db-104">You can use the **StopAllMacros** action to stop all macros that are currently running.</span></span>

## <a name="setting"></a><span data-ttu-id="715db-105">設定値</span><span class="sxs-lookup"><span data-stu-id="715db-105">Setting</span></span>

<span data-ttu-id="715db-106">**中止**引数はありません。</span><span class="sxs-lookup"><span data-stu-id="715db-106">The **StopAllMacros** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="715db-107">解説</span><span class="sxs-lookup"><span data-stu-id="715db-107">Remarks</span></span>

<span data-ttu-id="715db-108">この操作は、エラー状態では、すべてのマクロを停止するために必要なときに使用します。</span><span class="sxs-lookup"><span data-stu-id="715db-108">You typically use this action when an error condition makes it necessary to stop all macros.</span></span> <span data-ttu-id="715db-109">このアクションが定義されているマクロ内のアクション行に条件式を指定できます。</span><span class="sxs-lookup"><span data-stu-id="715db-109">You can use a conditional expression in the macro's action row that contains this action.</span></span> <span data-ttu-id="715db-110">式は、 **True** (-1) に評価されると、Microsoft Access は、すべてのマクロを停止します。</span><span class="sxs-lookup"><span data-stu-id="715db-110">When the expression evaluates to **True** (–1), Microsoft Access stops all macros.</span></span>

<span data-ttu-id="715db-111">などの他のマクロの実行を含む、複雑なアクションの数の 1 つとしてメッセージ ボックスを表示するマクロがあります。</span><span class="sxs-lookup"><span data-stu-id="715db-111">For example, you might have a macro that displays a message box as one of a number of complex actions, including running other macros.</span></span> <span data-ttu-id="715db-112">ユーザーは、このメッセージ ボックスで**キャンセル**をクリックすると、**中止**は、実行されているすべてのマクロを停止できます。</span><span class="sxs-lookup"><span data-stu-id="715db-112">If the user clicks **Cancel** in this message box, the **StopAllMacros** action can stop all the macros that are running.</span></span>

<span data-ttu-id="715db-113">マクロは、エコーやシステム メッセージの表示を有効にするのには**エコー** "や" **SetWarnings**アクションを使用するには場合、**中止**に自動的にオンに戻ります。</span><span class="sxs-lookup"><span data-stu-id="715db-113">If a macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopAllMacros** action automatically turns them back on.</span></span>

<span data-ttu-id="715db-114">このアクションは Visual Basic for Applications (VBA) モジュールでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="715db-114">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

