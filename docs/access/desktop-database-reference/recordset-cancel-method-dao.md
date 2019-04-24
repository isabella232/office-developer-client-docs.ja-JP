---
title: Recordset の Cancel メソッド (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 102511575770ceb38cf682d5e627fb7e64faa1ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300813"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="c68ff-102">Recordset の Cancel メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="c68ff-102">Recordset.Cancel method (DAO)</span></span>


<span data-ttu-id="c68ff-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c68ff-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="c68ff-104">構文</span><span class="sxs-lookup"><span data-stu-id="c68ff-104">Syntax</span></span>

<span data-ttu-id="c68ff-105">*式*。キャンセル</span><span class="sxs-lookup"><span data-stu-id="c68ff-105">*expression* .Cancel</span></span>

<span data-ttu-id="c68ff-106">\*式\***Recordset**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="c68ff-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c68ff-107">注釈</span><span class="sxs-lookup"><span data-stu-id="c68ff-107">Remarks</span></span>

<span data-ttu-id="c68ff-108">**Cancel**メソッドを使用して、非同期の**Execute**メソッドまたは**openconnection**メソッドの呼び出し (つまり、dbrunasync オプションを指定してメソッドが呼び出された場合) の実行を終了します。</span><span class="sxs-lookup"><span data-stu-id="c68ff-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="c68ff-109">終了しようとしているメソッドで dbrunasync が使用されていない場合、 **Cancel**は実行時エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="c68ff-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

