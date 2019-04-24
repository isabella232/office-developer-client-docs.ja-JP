---
title: filtervalue プロパティ (RDS)
TOCTitle: FilterValue property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70dca16f4a949cc6088779c1406e0c77cb477ba1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292406"
---
# <a name="filtervalue-property-rds"></a><span data-ttu-id="cd9d4-102">filtervalue プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="cd9d4-102">FilterValue property (RDS)</span></span>

<span data-ttu-id="cd9d4-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd9d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cd9d4-104">レコードをフィルター処理するための値を示します。</span><span class="sxs-lookup"><span data-stu-id="cd9d4-104">Indicates the value with which to filter records.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd9d4-105">構文</span><span class="sxs-lookup"><span data-stu-id="cd9d4-105">Syntax</span></span>

<span data-ttu-id="cd9d4-106">*DataControl*。filtervalue = *String*</span><span class="sxs-lookup"><span data-stu-id="cd9d4-106">*DataControl*.FilterValue = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="cd9d4-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cd9d4-107">Parameters</span></span>

|<span data-ttu-id="cd9d4-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cd9d4-108">Parameter</span></span>|<span data-ttu-id="cd9d4-109">説明</span><span class="sxs-lookup"><span data-stu-id="cd9d4-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="cd9d4-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="cd9d4-110">*DataControl*</span></span> |<span data-ttu-id="cd9d4-111">[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="cd9d4-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="cd9d4-112">*String*</span><span class="sxs-lookup"><span data-stu-id="cd9d4-112">*String*</span></span> |<span data-ttu-id="cd9d4-113">レコードをフィルター処理するためのデータ値を表す**文字列型 (String** ) の値を指定します (例: ' プログラマーズ ' または 125)。</span><span class="sxs-lookup"><span data-stu-id="cd9d4-113">A **String** value that represents a data value with which to filter records (for example, 'Programmer' or 125 ).</span></span>|

## <a name="remarks"></a><span data-ttu-id="cd9d4-114">注釈</span><span class="sxs-lookup"><span data-stu-id="cd9d4-114">Remarks</span></span>

<span data-ttu-id="cd9d4-115">プロパティ [SortColumn](sortcolumn-property-rds.md)、 [SortDirection](sortdirection-property-rds.md) 、 **FilterValue**、[FilterCriterion](filtercriterion-property-rds.md)、および [FilterColumn](filtercolumn-property-rds.md) は、クライアント側のキャッシュ上で並べ替え機能とフィルター機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="cd9d4-115">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> 

<span data-ttu-id="cd9d4-116">並べ替え機能は、列の値でレコードを並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="cd9d4-116">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="cd9d4-117">フィルター機能は、キャッシュ内の完全な [Recordset](recordset-object-ado.md) は保持したまま、検索条件に基づいてレコードのサブセットを表示します。</span><span class="sxs-lookup"><span data-stu-id="cd9d4-117">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="cd9d4-118">[Reset](reset-method-rds.md) メソッドは検索条件を実行し、現在の **Recordset** を更新可能な **Recordset** に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="cd9d4-118">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="cd9d4-119">Null 値は型の不一致エラーになります。</span><span class="sxs-lookup"><span data-stu-id="cd9d4-119">Null values result in a type mismatch error.</span></span>

