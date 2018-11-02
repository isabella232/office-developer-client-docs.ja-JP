---
title: Recordset.Cancel メソッド (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 81b08472b46ab3a3d35d184e2f8b7be8673f7d1f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927264"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="13080-102">Recordset.Cancel メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="13080-102">Recordset.Cancel method (DAO)</span></span>


<span data-ttu-id="13080-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="13080-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="13080-104">構文</span><span class="sxs-lookup"><span data-stu-id="13080-104">Syntax</span></span>

<span data-ttu-id="13080-105">*式*です。キャンセル</span><span class="sxs-lookup"><span data-stu-id="13080-105">*expression* .Cancel</span></span>

<span data-ttu-id="13080-106">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="13080-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="13080-107">備考</span><span class="sxs-lookup"><span data-stu-id="13080-107">Remarks</span></span>

<span data-ttu-id="13080-108">**Cancel**メソッドを使用して、**実行**または**されます**メソッドの非同期呼び出しの実行を中止する (つまり、メソッドが dbRunAsync オプションを指定して呼び出されました)。</span><span class="sxs-lookup"><span data-stu-id="13080-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="13080-109">終了するメソッドで dbRunAsync が使用できない場合、**キャンセル**実行時エラー戻ります。</span><span class="sxs-lookup"><span data-stu-id="13080-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

