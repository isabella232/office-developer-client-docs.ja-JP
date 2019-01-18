---
title: Recordset.Cancel メソッド (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 102511575770ceb38cf682d5e627fb7e64faa1ff
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716713"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="ad5ac-102">Recordset.Cancel メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="ad5ac-102">Recordset.Cancel method (DAO)</span></span>


<span data-ttu-id="ad5ac-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ad5ac-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="ad5ac-104">構文</span><span class="sxs-lookup"><span data-stu-id="ad5ac-104">Syntax</span></span>

<span data-ttu-id="ad5ac-105">*式*です。キャンセル</span><span class="sxs-lookup"><span data-stu-id="ad5ac-105">*expression* .Cancel</span></span>

<span data-ttu-id="ad5ac-106">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="ad5ac-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad5ac-107">注釈</span><span class="sxs-lookup"><span data-stu-id="ad5ac-107">Remarks</span></span>

<span data-ttu-id="ad5ac-108">**Cancel**メソッドを使用して、**実行**または**されます**メソッドの非同期呼び出しの実行を中止する (つまり、メソッドが dbRunAsync オプションを指定して呼び出されました)。</span><span class="sxs-lookup"><span data-stu-id="ad5ac-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="ad5ac-109">終了するメソッドで dbRunAsync が使用できない場合、**キャンセル**実行時エラー戻ります。</span><span class="sxs-lookup"><span data-stu-id="ad5ac-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

