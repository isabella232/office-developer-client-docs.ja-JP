---
title: QueryDef メソッド (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301121"
---
# <a name="querydefcancel-method-dao"></a><span data-ttu-id="be270-102">QueryDef メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="be270-102">QueryDef.Cancel method (DAO)</span></span>


<span data-ttu-id="be270-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="be270-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="be270-104">構文</span><span class="sxs-lookup"><span data-stu-id="be270-104">Syntax</span></span>

<span data-ttu-id="be270-105">*式*。キャンセル</span><span class="sxs-lookup"><span data-stu-id="be270-105">*expression* .Cancel</span></span>

<span data-ttu-id="be270-106">\*式\***QueryDef**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="be270-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="be270-107">注釈</span><span class="sxs-lookup"><span data-stu-id="be270-107">Remarks</span></span>

<span data-ttu-id="be270-108">**Cancel**メソッドを使用して、非同期の**Execute**メソッドまたは**openconnection**メソッドの呼び出し (つまり、dbrunasync オプションを指定してメソッドが呼び出された場合) の実行を終了します。</span><span class="sxs-lookup"><span data-stu-id="be270-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="be270-109">終了しようとしているメソッドで dbrunasync が使用されていない場合、 **Cancel**は実行時エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="be270-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

