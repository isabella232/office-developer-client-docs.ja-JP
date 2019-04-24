---
title: CancelUpdate メソッド (RDS)
TOCTitle: CancelUpdate method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b0c02a9ca72add763e1d3ccf62d5ede8adaecc6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296669"
---
# <a name="cancelupdate-method-rds"></a><span data-ttu-id="28a37-102">CancelUpdate メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="28a37-102">CancelUpdate method (RDS)</span></span>

<span data-ttu-id="28a37-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="28a37-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28a37-104">[Recordset](recordset-object-ado.md) オブジェクトの現在の行または新しい行に加えられたすべての変更をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="28a37-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="28a37-105">構文</span><span class="sxs-lookup"><span data-stu-id="28a37-105">Syntax</span></span>

<span data-ttu-id="28a37-106">*DataControl*。CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="28a37-106">*DataControl*.CancelUpdate</span></span>

## <a name="parameters"></a><span data-ttu-id="28a37-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="28a37-107">Parameters</span></span>

|<span data-ttu-id="28a37-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="28a37-108">Parameter</span></span>|<span data-ttu-id="28a37-109">説明</span><span class="sxs-lookup"><span data-stu-id="28a37-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="28a37-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="28a37-110">*DataControl*</span></span> |<span data-ttu-id="28a37-111">[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数。</span><span class="sxs-lookup"><span data-stu-id="28a37-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="28a37-112">注釈</span><span class="sxs-lookup"><span data-stu-id="28a37-112">Remarks</span></span>

<span data-ttu-id="28a37-p101">Cursor Service for OLE DB は、元の値のコピーと変更のキャッシュを両方維持します。**CancelUpdate** を呼び出すと、変更のキャッシュがリセットされて空になり、すべての連結コントロールが元のデータで更新されます。</span><span class="sxs-lookup"><span data-stu-id="28a37-p101">The Cursor Service for OLE DB keeps both a copy of the original values and a cache of changes. When you call **CancelUpdate**, the cache of changes is reset to empty, and any bound controls are refreshed with the original data.</span></span>

