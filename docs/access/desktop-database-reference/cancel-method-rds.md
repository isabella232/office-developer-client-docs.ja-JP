---
title: Cancel メソッド (RDS)
TOCTitle: Cancel Method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8455496e8d426d26f56b902d9a089d236bde1a6a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868748"
---
# <a name="cancel-method-rds"></a><span data-ttu-id="2d12f-102">Cancel メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="2d12f-102">Cancel Method (RDS)</span></span>


<span data-ttu-id="2d12f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2d12f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d12f-104">保留中の非同期メソッド呼び出しの実行を取り消します。</span><span class="sxs-lookup"><span data-stu-id="2d12f-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d12f-105">構文</span><span class="sxs-lookup"><span data-stu-id="2d12f-105">Syntax</span></span>

<span data-ttu-id="2d12f-106">*RDS*。</span><span class="sxs-lookup"><span data-stu-id="2d12f-106">*RDS*.</span></span> <span data-ttu-id="2d12f-107">*DataControl*。キャンセル</span><span class="sxs-lookup"><span data-stu-id="2d12f-107">*DataControl*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="2d12f-108">解説</span><span class="sxs-lookup"><span data-stu-id="2d12f-108">Remarks</span></span>

<span data-ttu-id="2d12f-109">**Cancel** を呼び出すと、 [ReadyState](readystate-property-rds.md) が自動的に **adcReadyStateLoaded** に設定され、 [Recordset](recordset-object-ado.md) は空になります。</span><span class="sxs-lookup"><span data-stu-id="2d12f-109">When you call **Cancel**, [ReadyState](readystate-property-rds.md) is automatically set to **adcReadyStateLoaded**, and the [Recordset](recordset-object-ado.md) will be empty.</span></span>

