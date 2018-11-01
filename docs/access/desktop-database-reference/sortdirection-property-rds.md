---
title: SortDirection プロパティ (RDS)
TOCTitle: SortDirection Property (RDS)
ms:assetid: 33de0dce-f371-6a54-d179-0627939f5b14
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249106(v=office.15)
ms:contentKeyID: 48544119
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3603696992ab7ac759a62a70f50b4fa35636d2c0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879152"
---
# <a name="sortdirection-property-rds"></a><span data-ttu-id="81fc4-102">SortDirection プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="81fc4-102">SortDirection Property (RDS)</span></span>


<span data-ttu-id="81fc4-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="81fc4-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="81fc4-104">並べ替え順序が昇順であるか、降順であるかを示します。</span><span class="sxs-lookup"><span data-stu-id="81fc4-104">Indicates whether a sort order is ascending or descending.</span></span>

## <a name="syntax"></a><span data-ttu-id="81fc4-105">構文</span><span class="sxs-lookup"><span data-stu-id="81fc4-105">Syntax</span></span>

<span data-ttu-id="81fc4-106">*DataControl*。これら*の値*を =</span><span class="sxs-lookup"><span data-stu-id="81fc4-106">*DataControl*.SortDirection = *value*</span></span>

## <a name="parameters"></a><span data-ttu-id="81fc4-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="81fc4-107">Parameters</span></span>

  - <span data-ttu-id="81fc4-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="81fc4-108">*DataControl*</span></span>

  - <span data-ttu-id="81fc4-109">[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="81fc4-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="81fc4-110">*Value*</span><span class="sxs-lookup"><span data-stu-id="81fc4-110">*Value*</span></span>

  - <span data-ttu-id="81fc4-p101">ブール型 ( **Boolean** ) の値。 **True** に設定されている場合は、並べ替え順序が昇順であることを示します。 **False** は降順であることを示します。</span><span class="sxs-lookup"><span data-stu-id="81fc4-p101">A **Boolean** value that, when set to **True**, indicates the sort direction is ascending. **False** indicates descending order.</span></span>

## <a name="remarks"></a><span data-ttu-id="81fc4-113">解説</span><span class="sxs-lookup"><span data-stu-id="81fc4-113">Remarks</span></span>

<span data-ttu-id="81fc4-p102">プロパティ [SortColumn](sortcolumn-property-rds.md)、 **SortDirection** 、 [FilterValue](filtervalue-property-rds.md)、[FilterCriterion](filtercriterion-property-rds.md)、および [FilterColumn](filtercolumn-property-rds.md) は、クライアント側のキャッシュ上で並べ替え機能とフィルター機能を提供します。並べ替え機能は、列の値でレコードを並べ替えます。フィルター機能は、キャッシュ内の完全な [Recordset](recordset-object-ado.md) は保持したまま、検索条件に基づいてレコードのサブセットを表示します。 **Reset** メソッドは検索条件を実行し、現在の **Recordset** を更新可能な **Recordset** に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="81fc4-p102">The [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

