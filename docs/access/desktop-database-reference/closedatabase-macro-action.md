---
title: CloseDatabase マクロ アクション
TOCTitle: CloseDatabase macro action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ac29cbdae8c162a992f2763530514150ca0240ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296298"
---
# <a name="closedatabase-macro-action"></a><span data-ttu-id="2179f-102">CloseDatabase マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="2179f-102">CloseDatabase macro action</span></span>


<span data-ttu-id="2179f-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="2179f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2179f-104">"CloseDatabase/データベースを閉じる" アクションを使用すると、カレント データベースを閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="2179f-104">You can use the **CloseDatabase** action to close the current database.</span></span>

## <a name="setting"></a><span data-ttu-id="2179f-105">Setting</span><span class="sxs-lookup"><span data-stu-id="2179f-105">Setting</span></span>

<span data-ttu-id="2179f-106">"CloseDatabase/データベースを閉じる" アクションには、引数はありません。</span><span class="sxs-lookup"><span data-stu-id="2179f-106">The **CloseDatabase** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="2179f-107">注釈</span><span class="sxs-lookup"><span data-stu-id="2179f-107">Remarks</span></span>

  - <span data-ttu-id="2179f-108">マクロの中で "CloseDatabase/データベースを閉じる" アクションより後に設定されたアクションは実行されません。</span><span class="sxs-lookup"><span data-stu-id="2179f-108">Access will not run any actions that follow the **CloseDatabase** action in a macro.</span></span>

  - <span data-ttu-id="2179f-109">このアクションの動作は、[**ファイル**] タブをクリックし、[**データベースを閉じる**] をクリックした場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="2179f-109">This action has the same effect as clicking the **File** tab and then clicking **Close Database**.</span></span> <span data-ttu-id="2179f-110">If there are any unsaved objects open when you run the **CloseDatabase** action, the dialog boxes that appear are the same as those displayed when you click **Close Database**.</span><span class="sxs-lookup"><span data-stu-id="2179f-110">If there are any unsaved objects open when you run the **CloseDatabase** action, the dialog boxes that appear are the same as those displayed when you click **Close Database**.</span></span>

  - <span data-ttu-id="2179f-111">To run the **CloseDatabase** action in a Visual Basic for Applications (VBA) module, use the **CloseDatabase** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="2179f-111">To run the **CloseDatabase** action in a Visual Basic for Applications (VBA) module, use the **CloseDatabase** method of the **DoCmd** object.</span></span>

