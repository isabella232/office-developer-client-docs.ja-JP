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
ms.openlocfilehash: ab28f1b976144c40eb8be639bb7c7a1adc3e4450
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920229"
---
# <a name="querydefcancel-method-dao"></a><span data-ttu-id="dbcbf-102">QueryDef.Cancel メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="dbcbf-102">QueryDef.Cancel method (DAO)</span></span>


<span data-ttu-id="dbcbf-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="dbcbf-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="dbcbf-104">構文</span><span class="sxs-lookup"><span data-stu-id="dbcbf-104">Syntax</span></span>

<span data-ttu-id="dbcbf-105">*式*です。キャンセル</span><span class="sxs-lookup"><span data-stu-id="dbcbf-105">*expression* .Cancel</span></span>

<span data-ttu-id="dbcbf-106">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="dbcbf-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbcbf-107">備考</span><span class="sxs-lookup"><span data-stu-id="dbcbf-107">Remarks</span></span>

<span data-ttu-id="dbcbf-108">**Cancel**メソッドを使用して、**実行**または**されます**メソッドの非同期呼び出しの実行を中止する (つまり、メソッドが dbRunAsync オプションを指定して呼び出されました)。</span><span class="sxs-lookup"><span data-stu-id="dbcbf-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="dbcbf-109">終了するメソッドで dbRunAsync が使用できない場合、**キャンセル**実行時エラー戻ります。</span><span class="sxs-lookup"><span data-stu-id="dbcbf-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

