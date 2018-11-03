---
title: Recordset2.Cancel メソッド (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 159f476b592a8c944df2dc4570d84377c89b5043
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929232"
---
# <a name="recordset2cancel-method-dao"></a><span data-ttu-id="88759-102">Recordset2.Cancel メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="88759-102">Recordset2.Cancel method (DAO)</span></span>


<span data-ttu-id="88759-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="88759-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="88759-104">構文</span><span class="sxs-lookup"><span data-stu-id="88759-104">Syntax</span></span>

<span data-ttu-id="88759-105">*式*です。キャンセル</span><span class="sxs-lookup"><span data-stu-id="88759-105">*expression* .Cancel</span></span>

<span data-ttu-id="88759-106">\*式\***Recordset2**オブジェクトを返すオブジェクト式を指定します。</span><span class="sxs-lookup"><span data-stu-id="88759-106">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="88759-107">備考</span><span class="sxs-lookup"><span data-stu-id="88759-107">Remarks</span></span>

<span data-ttu-id="88759-108">**Cancel**メソッドを使用して、**実行**または**されます**メソッドの非同期呼び出しの実行を中止する (つまり、メソッドが dbRunAsync オプションを指定して呼び出されました)。</span><span class="sxs-lookup"><span data-stu-id="88759-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="88759-109">終了するメソッドで dbRunAsync が使用できない場合、**キャンセル**実行時エラー戻ります。</span><span class="sxs-lookup"><span data-stu-id="88759-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

