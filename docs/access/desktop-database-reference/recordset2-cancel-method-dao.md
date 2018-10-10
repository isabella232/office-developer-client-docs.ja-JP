---
title: Recordset2.Cancel メソッド (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d3b943bed5abdd057b21e8a1380a68231d20e00
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478052"
---
# <a name="recordset2cancel-method-dao"></a><span data-ttu-id="7aef2-102">Recordset2.Cancel メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="7aef2-102">Recordset2.Cancel Method (DAO)</span></span>


<span data-ttu-id="7aef2-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="7aef2-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="7aef2-104">構文</span><span class="sxs-lookup"><span data-stu-id="7aef2-104">Syntax</span></span>

<span data-ttu-id="7aef2-105">*式*です。キャンセル</span><span class="sxs-lookup"><span data-stu-id="7aef2-105">*expression* .Cancel</span></span>

<span data-ttu-id="7aef2-106">\*式\***Recordset2**オブジェクトを返すオブジェクト式を指定します。</span><span class="sxs-lookup"><span data-stu-id="7aef2-106">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7aef2-107">備考</span><span class="sxs-lookup"><span data-stu-id="7aef2-107">Remarks</span></span>

<span data-ttu-id="7aef2-108">**Cancel**メソッドを使用して、**実行**または**されます**メソッドの非同期呼び出しの実行を中止する (つまり、メソッドが dbRunAsync オプションを指定して呼び出されました)。</span><span class="sxs-lookup"><span data-stu-id="7aef2-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="7aef2-109">終了するメソッドで dbRunAsync が使用できない場合、**キャンセル**実行時エラー戻ります。</span><span class="sxs-lookup"><span data-stu-id="7aef2-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

