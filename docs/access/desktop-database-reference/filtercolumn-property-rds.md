---
title: FilterColumn プロパティ (RDS)
TOCTitle: FilterColumn Property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9cf03a2cbff06919981ac940f5b2962062a850c2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877801"
---
# <a name="filtercolumn-property-rds"></a><span data-ttu-id="567ca-102">FilterColumn プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="567ca-102">FilterColumn Property (RDS)</span></span>


<span data-ttu-id="567ca-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="567ca-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="567ca-104">フィルター条件を評価する列を示します。</span><span class="sxs-lookup"><span data-stu-id="567ca-104">Indicates the column on which to evaluate the filter criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="567ca-105">構文</span><span class="sxs-lookup"><span data-stu-id="567ca-105">Syntax</span></span>

<span data-ttu-id="567ca-106">*DataControl*。FilterColumn =*文字列*</span><span class="sxs-lookup"><span data-stu-id="567ca-106">*DataControl*.FilterColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="567ca-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="567ca-107">Parameters</span></span>

  - <span data-ttu-id="567ca-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="567ca-108">*DataControl*</span></span>

  - <span data-ttu-id="567ca-109">[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="567ca-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="567ca-110">*String*</span><span class="sxs-lookup"><span data-stu-id="567ca-110">*String*</span></span>

  - <span data-ttu-id="567ca-p101">フィルター条件を評価する列を指定する文字列型 ( **String** ) の値を指定します。フィルター条件は [FilterCriterion](filtercriterion-property-rds.md) プロパティに指定します。</span><span class="sxs-lookup"><span data-stu-id="567ca-p101">A **String** value that specifies the column on which to evaluate the filter criteria. The filter criteria are specified in the [FilterCriterion](filtercriterion-property-rds.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="567ca-113">解説</span><span class="sxs-lookup"><span data-stu-id="567ca-113">Remarks</span></span>

<span data-ttu-id="567ca-p102">プロパティ [SortColumn](sortcolumn-property-rds.md)、 [SortDirection](sortdirection-property-rds.md) 、 [FilterValue](filtervalue-property-rds.md)、[FilterCriterion](filtercriterion-property-rds.md)、および **FilterColumn** は、クライアント側のキャッシュ上で並べ替え機能とフィルター機能を提供します。並べ替え機能は、列の値でレコードを並べ替えます。フィルター機能は、キャッシュ内の完全な [Recordset](recordset-object-ado.md) は保持したまま、検索条件に基づいてレコードのサブセットを表示します。 [Reset](reset-method-rds.md) メソッドは検索条件を実行し、現在の **Recordset** を更新可能な **Recordset** に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="567ca-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and **FilterColumn** properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

