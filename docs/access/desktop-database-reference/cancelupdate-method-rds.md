---
title: CancelUpdate メソッド (RDS)
TOCTitle: CancelUpdate Method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ea646f2412ec078f3a45334ec2b1cdbe449285b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477477"
---
# <a name="cancelupdate-method-rds"></a><span data-ttu-id="71a5f-102">CancelUpdate メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="71a5f-102">CancelUpdate Method (RDS)</span></span>


<span data-ttu-id="71a5f-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="71a5f-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="71a5f-104">[Recordset](recordset-object-ado.md) オブジェクトの現在の行または新しい行に加えられたすべての変更をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="71a5f-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="71a5f-105">構文</span><span class="sxs-lookup"><span data-stu-id="71a5f-105">Syntax</span></span>

<span data-ttu-id="71a5f-106">*DataControl*。CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="71a5f-106">*DataControl*.CancelUpdate</span></span>

## <a name="parameters"></a><span data-ttu-id="71a5f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="71a5f-107">Parameters</span></span>

  - <span data-ttu-id="71a5f-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="71a5f-108">*DataControl*</span></span>

  - <span data-ttu-id="71a5f-109">[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="71a5f-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="71a5f-110">解説</span><span class="sxs-lookup"><span data-stu-id="71a5f-110">Remarks</span></span>

<span data-ttu-id="71a5f-p101">Cursor Service for OLE DB は、元の値のコピーと変更のキャッシュを両方維持します。 **CancelUpdate** を呼び出すと、変更のキャッシュがリセットされて空になり、すべての連結コントロールが元のデータで更新されます。</span><span class="sxs-lookup"><span data-stu-id="71a5f-p101">The Cursor Service for OLE DB keeps both a copy of the original values and a cache of changes. When you call **CancelUpdate**, the cache of changes is reset to empty, and any bound controls are refreshed with the original data.</span></span>

