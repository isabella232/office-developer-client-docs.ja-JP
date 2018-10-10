---
title: FilterValue プロパティ (RDS)
TOCTitle: FilterValue Property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39152be2c53dc0de9bc1bcb21fee505fcb9106dc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477381"
---
# <a name="filtervalue-property-rds"></a><span data-ttu-id="9f0ad-102">FilterValue プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="9f0ad-102">FilterValue Property (RDS)</span></span>


<span data-ttu-id="9f0ad-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f0ad-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="9f0ad-104">レコードをフィルター処理するための値を示します。</span><span class="sxs-lookup"><span data-stu-id="9f0ad-104">Indicates the value with which to filter records.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f0ad-105">構文</span><span class="sxs-lookup"><span data-stu-id="9f0ad-105">Syntax</span></span>

<span data-ttu-id="9f0ad-106">*DataControl*。FilterValue =*文字列*</span><span class="sxs-lookup"><span data-stu-id="9f0ad-106">*DataControl*.FilterValue = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="9f0ad-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9f0ad-107">Parameters</span></span>

  - <span data-ttu-id="9f0ad-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="9f0ad-108">*DataControl*</span></span>

  - <span data-ttu-id="9f0ad-109">[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9f0ad-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="9f0ad-110">*String*</span><span class="sxs-lookup"><span data-stu-id="9f0ad-110">*String*</span></span>

  - <span data-ttu-id="9f0ad-111">**文字列**を表す値 (たとえば、'プログラマ' または 125) のフィルター処理に使用するデータ値を記録します。</span><span class="sxs-lookup"><span data-stu-id="9f0ad-111">A **String** value that represents a data value with which to filter records (for example, 'Programmer' or 125 ).</span></span>

## <a name="remarks"></a><span data-ttu-id="9f0ad-112">解説</span><span class="sxs-lookup"><span data-stu-id="9f0ad-112">Remarks</span></span>

<span data-ttu-id="9f0ad-p101">プロパティ [SortColumn](sortcolumn-property-rds.md)、[SortDirection](sortdirection-property-rds.md)、 **FilterValue** 、 [FilterCriterion](filtercriterion-property-rds.md)、および [FilterColumn](filtercolumn-property-rds.md) は、クライアント側のキャッシュ上で並べ替え機能とフィルター機能を提供します。並べ替え機能は、列の値でレコードを並べ替えます。フィルター機能は、キャッシュ内の完全な [Recordset](recordset-object-ado.md) は保持したまま、検索条件に基づいてレコードのサブセットを表示します。 [Reset](reset-method-rds.md) メソッドは検索条件を実行し、現在の **Recordset** を更新可能な **Recordset** に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="9f0ad-p101">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="9f0ad-117">Null 値は型の不一致エラーになります。</span><span class="sxs-lookup"><span data-stu-id="9f0ad-117">Null values result in a type mismatch error.</span></span>
