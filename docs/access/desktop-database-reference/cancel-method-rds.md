---
title: Cancel メソッド (RDS)
TOCTitle: Cancel method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 35322ec058d31f92288fd06a4e8434a4256c2d74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296648"
---
# <a name="cancel-method-rds"></a><span data-ttu-id="0f8a6-102">Cancel メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="0f8a6-102">Cancel method (RDS)</span></span>


<span data-ttu-id="0f8a6-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f8a6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0f8a6-104">保留中の非同期メソッド呼び出しの実行を取り消します。</span><span class="sxs-lookup"><span data-stu-id="0f8a6-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f8a6-105">構文</span><span class="sxs-lookup"><span data-stu-id="0f8a6-105">Syntax</span></span>

<span data-ttu-id="0f8a6-106">*RDS*。</span><span class="sxs-lookup"><span data-stu-id="0f8a6-106">*RDS*.</span></span> <span data-ttu-id="0f8a6-107">*DataControl*。キャンセル</span><span class="sxs-lookup"><span data-stu-id="0f8a6-107">*DataControl*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="0f8a6-108">注釈</span><span class="sxs-lookup"><span data-stu-id="0f8a6-108">Remarks</span></span>

<span data-ttu-id="0f8a6-109">**Cancel** を呼び出すと、[ReadyState](readystate-property-rds.md) が自動的に **adcReadyStateLoaded** に設定され、[Recordset](recordset-object-ado.md) は空になります。</span><span class="sxs-lookup"><span data-stu-id="0f8a6-109">When you call **Cancel**, [ReadyState](readystate-property-rds.md) is automatically set to **adcReadyStateLoaded**, and the [Recordset](recordset-object-ado.md) will be empty.</span></span>

