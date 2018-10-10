---
title: Cancel メソッド (RDS)
TOCTitle: Cancel Method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dcd37f8736b7ab4b953480cd28daeb3080abe07f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477017"
---
# <a name="cancel-method-rds"></a><span data-ttu-id="d52e4-102">Cancel メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="d52e4-102">Cancel Method (RDS)</span></span>


<span data-ttu-id="d52e4-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d52e4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d52e4-104">保留中の非同期メソッド呼び出しの実行を取り消します。</span><span class="sxs-lookup"><span data-stu-id="d52e4-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="d52e4-105">構文</span><span class="sxs-lookup"><span data-stu-id="d52e4-105">Syntax</span></span>

<span data-ttu-id="d52e4-106">*RDS*。</span><span class="sxs-lookup"><span data-stu-id="d52e4-106">*RDS*.</span></span> <span data-ttu-id="d52e4-107">*DataControl*。キャンセル</span><span class="sxs-lookup"><span data-stu-id="d52e4-107">*DataControl*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="d52e4-108">解説</span><span class="sxs-lookup"><span data-stu-id="d52e4-108">Remarks</span></span>

<span data-ttu-id="d52e4-109">**Cancel** を呼び出すと、 [ReadyState](readystate-property-rds.md) が自動的に **adcReadyStateLoaded** に設定され、 [Recordset](recordset-object-ado.md) は空になります。</span><span class="sxs-lookup"><span data-stu-id="d52e4-109">When you call **Cancel**, [ReadyState](readystate-property-rds.md) is automatically set to **adcReadyStateLoaded**, and the [Recordset](recordset-object-ado.md) will be empty.</span></span>

