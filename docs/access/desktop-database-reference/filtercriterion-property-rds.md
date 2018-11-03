---
title: FilterCriterion プロパティ (RDS)
TOCTitle: FilterCriterion property (RDS)
ms:assetid: 51e6cb64-a404-114e-8e1a-0744cceeec3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249267(v=office.15)
ms:contentKeyID: 48544834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5a9724d84bed6c89267aeb811936eeb49b49bc17
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929343"
---
# <a name="filtercriterion-property-rds"></a><span data-ttu-id="8c742-102">FilterCriterion プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="8c742-102">FilterCriterion property (RDS)</span></span>


<span data-ttu-id="8c742-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="8c742-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="8c742-104">フィルター値に使う評価演算子を表します。</span><span class="sxs-lookup"><span data-stu-id="8c742-104">Indicates the evaluation operator to use in the filter value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c742-105">構文</span><span class="sxs-lookup"><span data-stu-id="8c742-105">Syntax</span></span>

<span data-ttu-id="8c742-106">*DataControl*。FilterCriterion =*文字列*</span><span class="sxs-lookup"><span data-stu-id="8c742-106">*DataControl*.FilterCriterion = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="8c742-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8c742-107">Parameters</span></span>

  - <span data-ttu-id="8c742-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="8c742-108">*DataControl*</span></span>

  - <span data-ttu-id="8c742-109">[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8c742-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="8c742-110">*String*</span><span class="sxs-lookup"><span data-stu-id="8c742-110">*String*</span></span>

  - <span data-ttu-id="8c742-111">レコードに **FilterValue** の評価演算子を指定する文字列型 ( [String](filtervalue-property-rds.md) ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="8c742-111">A **String** value that specifies the evaluation operator of the [FilterValue](filtervalue-property-rds.md) to the records.</span></span> <span data-ttu-id="8c742-112">次のいずれかをすることができます: \<、 \<= \>、 \>=、=、または\< \>。</span><span class="sxs-lookup"><span data-stu-id="8c742-112">Can be any one of the following: \<, \<=, \>, \>=, =, or \<\>.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c742-113">解説</span><span class="sxs-lookup"><span data-stu-id="8c742-113">Remarks</span></span>

<span data-ttu-id="8c742-p102">プロパティ [SortColumn](sortcolumn-property-rds.md)、 [SortDirection](sortdirection-property-rds.md) 、 [FilterValue](filtervalue-property-rds.md)、**FilterCriterion**、および [FilterColumn](filtercolumn-property-rds.md) は、クライアント側のキャッシュ上で並べ替え機能とフィルター機能を提供します。並べ替え機能は、列の値でレコードを並べ替えます。フィルター機能は、キャッシュ内の完全な [Recordset](recordset-object-ado.md) は保持したまま、検索条件に基づいてレコードのサブセットを表示します。 [Reset](reset-method-rds.md) メソッドは検索条件を実行し、現在の **Recordset** を更新可能な **Recordset** に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="8c742-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion**, and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="8c742-118">"\!="演算子では無効です**FilterCriterion**。代わりに、"\<\>」です。</span><span class="sxs-lookup"><span data-stu-id="8c742-118">The "\!=" operator is not valid for **FilterCriterion**; instead, use "\<\>".</span></span>

<span data-ttu-id="8c742-p103">フィルター プロパティと並べ替えプロパティの両方を設定して **Reset** メソッドを呼び出した場合、行セットでは最初にフィルターが実行され、次に並べ替えが実行されます。昇順の並べ替えでは Null 値が最初に、降順の並べ替えでは Null 値が最後になります (昇順が既定の動作です)。</span><span class="sxs-lookup"><span data-stu-id="8c742-p103">If both the filter and sort properties are set and you call the **Reset** method, the rowset is first filtered and then it is sorted. For ascending sorts, the null values are at the top; for descending sorts, null values are at the bottom (ascending is default behavior).</span></span>

