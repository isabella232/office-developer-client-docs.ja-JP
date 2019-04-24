---
title: Reset メソッド (RDS-Access デスクトップデータベースリファレンス)
TOCTitle: Reset method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 898045bcfdd3fb2483954155319e6aab3d0ebc7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306644"
---
# <a name="reset-method-rds"></a><span data-ttu-id="1b89d-102">Reset メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="1b89d-102">Reset method (RDS)</span></span>

<span data-ttu-id="1b89d-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b89d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1b89d-104">指定されたソートとフィルターのプロパティに基づいて、クライアント側の **Recordset** でソートまたはフィルターを実行します。</span><span class="sxs-lookup"><span data-stu-id="1b89d-104">Executes the sort or filter on a client-side **Recordset** based on the specified sort and filter properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b89d-105">構文</span><span class="sxs-lookup"><span data-stu-id="1b89d-105">Syntax</span></span>

<span data-ttu-id="1b89d-106">*DataControl*。Reset (*値*)</span><span class="sxs-lookup"><span data-stu-id="1b89d-106">*DataControl*.Reset(*value*)</span></span>

## <a name="parameters"></a><span data-ttu-id="1b89d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1b89d-107">Parameters</span></span>

|<span data-ttu-id="1b89d-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1b89d-108">Parameter</span></span>|<span data-ttu-id="1b89d-109">説明</span><span class="sxs-lookup"><span data-stu-id="1b89d-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1b89d-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="1b89d-110">*DataControl*</span></span> |<span data-ttu-id="1b89d-111">[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="1b89d-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="1b89d-112">*value*</span><span class="sxs-lookup"><span data-stu-id="1b89d-112">*value*</span></span> |<span data-ttu-id="1b89d-p101">省略可能です。ブール型 ( **Boolean** ) の値を指定します。現在 "フィルター選択されている" 行セットでフィルターを実行する場合は、 **True** (既定値) を指定します。 **False** は、以前のフィルター オプションをすべて破棄して元の行セットでフィルターを実行する場合に指定します。</span><span class="sxs-lookup"><span data-stu-id="1b89d-p101">Optional. A **Boolean** value that is **True** (default) if you want to filter on the current "filtered" rowset. **False** indicates that you filter on the original rowset, removing any previous filter options.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1b89d-116">注釈</span><span class="sxs-lookup"><span data-stu-id="1b89d-116">Remarks</span></span>

<span data-ttu-id="1b89d-p102">[SortColumn](sortcolumn-property-rds.md)、[SortDirection](sortdirection-property-rds.md)、[FilterValue](filtervalue-property-rds.md)、[FilterCriterion](filtercriterion-property-rds.md)、および [FilterColumn](filtercolumn-property-rds.md) の各プロパティは、クライアント側のキャッシュ上でソート機能とフィルター機能を提供します。ソート機能では、1 つの列の値でレコードを並べます。フィルター機能では、抽出条件に基づいてレコードのサブセットを表示します。このとき、キャッシュには [Recordset](recordset-object-ado.md) 全体が保持されています。**Reset** メソッドは、抽出条件を実行し、現在の **Recordset** を更新可能な **Recordset** に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="1b89d-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on a find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="1b89d-p103">元のデータの変更がまだ適用されていない場合、 **Reset** メソッドは失敗します。まず [SubmitChanges](submitchanges-method-rds.md) メソッドを使用して、読み取り/書き込み可能な **Recordset** に加えられた変更を保存し、その後 **Reset** メソッドを使用してレコードに対するソートまたはフィルターを実行します。</span><span class="sxs-lookup"><span data-stu-id="1b89d-p103">If there are changes to the original data that haven't yet been submitted, the **Reset** method will fail. First, use the [SubmitChanges](submitchanges-method-rds.md) method to save any changes in a read/write **Recordset**, and then use the **Reset** method to sort or filter the records.</span></span>

<span data-ttu-id="1b89d-p104">行セットに複数のフィルターを実行する場合、**Reset** メソッドで *Boolean* 引数を使用できます。次の例は、その方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="1b89d-p104">If you want to perform more than one filter on your rowset, you can use the optional *Boolean* argument with the **Reset** method. The following example shows how to do this:</span></span>

