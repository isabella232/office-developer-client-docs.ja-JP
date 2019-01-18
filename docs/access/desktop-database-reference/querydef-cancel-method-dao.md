---
title: QueryDef.Cancel メソッド (DAO)
TOCTitle: Cancel Method
ms:assetid: 91e61012-c01c-4c24-185c-bdadb7f33a58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197642(v=office.15)
ms:contentKeyID: 48546364
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055470
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 56a4ba804dba25eb0b4722bcf5396229ee003f43
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720556"
---
# <a name="querydefcancel-method-dao"></a><span data-ttu-id="36731-102">QueryDef.Cancel メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="36731-102">QueryDef.Cancel method (DAO)</span></span>


<span data-ttu-id="36731-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="36731-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="36731-104">構文</span><span class="sxs-lookup"><span data-stu-id="36731-104">Syntax</span></span>

<span data-ttu-id="36731-105">*式*です。キャンセル</span><span class="sxs-lookup"><span data-stu-id="36731-105">*expression* .Cancel</span></span>

<span data-ttu-id="36731-106">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="36731-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="36731-107">注釈</span><span class="sxs-lookup"><span data-stu-id="36731-107">Remarks</span></span>

<span data-ttu-id="36731-108">**Cancel**メソッドを使用して、**実行**または**されます**メソッドの非同期呼び出しの実行を中止する (つまり、メソッドが dbRunAsync オプションを指定して呼び出されました)。</span><span class="sxs-lookup"><span data-stu-id="36731-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="36731-109">終了するメソッドで dbRunAsync が使用できない場合、**キャンセル**実行時エラー戻ります。</span><span class="sxs-lookup"><span data-stu-id="36731-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

