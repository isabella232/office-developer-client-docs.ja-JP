---
title: SortColumn プロパティ (RDS)
TOCTitle: SortColumn Property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 85f2b031ac105bf900548e90eda6c0feb4b78f96
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478464"
---
# <a name="sortcolumn-property-rds"></a><span data-ttu-id="693c7-102">SortColumn プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="693c7-102">SortColumn Property (RDS)</span></span>


<span data-ttu-id="693c7-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="693c7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="693c7-104">レコードの並べ替えに使用する列を示します。</span><span class="sxs-lookup"><span data-stu-id="693c7-104">Indicates by which column to sort the records.</span></span>

## <a name="syntax"></a><span data-ttu-id="693c7-105">構文</span><span class="sxs-lookup"><span data-stu-id="693c7-105">Syntax</span></span>

<span data-ttu-id="693c7-106">*DataControl*。SortColumn =*文字列*</span><span class="sxs-lookup"><span data-stu-id="693c7-106">*DataControl*.SortColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="693c7-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="693c7-107">Parameters</span></span>

  - <span data-ttu-id="693c7-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="693c7-108">*DataControl*</span></span>

  - <span data-ttu-id="693c7-109">[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="693c7-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="693c7-110">*String*</span><span class="sxs-lookup"><span data-stu-id="693c7-110">*String*</span></span>

  - <span data-ttu-id="693c7-111">レコードの並べ替えに使用する列の名前または別名を表す文字列型 ( **String** ) の値。</span><span class="sxs-lookup"><span data-stu-id="693c7-111">A **String** value that represents the name or alias of the column by which to sort the records.</span></span>

## <a name="remarks"></a><span data-ttu-id="693c7-112">解説</span><span class="sxs-lookup"><span data-stu-id="693c7-112">Remarks</span></span>

<span data-ttu-id="693c7-p101">プロパティ **SortColumn**、 [SortDirection](sortdirection-property-rds.md) 、 [FilterValue](filtervalue-property-rds.md)、[FilterCriterion](filtercriterion-property-rds.md)、および [FilterColumn](filtercolumn-property-rds.md) は、クライアント側のキャッシュ上で並べ替え機能とフィルター機能を提供します。並べ替え機能は、列の値でレコードを並べ替えます。フィルター機能は、キャッシュ内の完全な [Recordset](recordset-object-ado.md) は保持したまま、検索条件に基づいてレコードのサブセットを表示します。 [Reset](reset-method-rds.md) メソッドは検索条件を実行し、現在の **Recordset** を更新可能な **Recordset** に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="693c7-p101">The **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="693c7-117">**Recordset** の並べ替えを実行するには、まず保留になっている変更をすべて保存します。</span><span class="sxs-lookup"><span data-stu-id="693c7-117">To sort on a **Recordset**, you must first save any pending changes.</span></span> <span data-ttu-id="693c7-118">**RDS.DataControl** を使用している場合は、 [SubmitChanges](submitchanges-method-rds.md) メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="693c7-118">If you are using the **RDS.DataControl**, you can use the [SubmitChanges](submitchanges-method-rds.md) method.</span></span> <span data-ttu-id="693c7-119">などの場合、**の rds.DataControl** 、ADC1 という名前で、コードになります ADC1。SubmitChanges。</span><span class="sxs-lookup"><span data-stu-id="693c7-119">For example, if your **RDS.DataControl** is named ADC1, your code would be ADC1.SubmitChanges .</span></span> <span data-ttu-id="693c7-120">ADO **Recordset** を使用している場合は、 [UpdateBatch](updatebatch-method-ado.md) メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="693c7-120">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="693c7-121">**CreateRecordset** メソッドで作成した **Recordset** オブジェクトには、 [UpdateBatch](createrecordset-method-rds.md) を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="693c7-121">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="693c7-122">たとえば、コードは myRS.UpdateBatch 可能性がありますか。</span><span class="sxs-lookup"><span data-stu-id="693c7-122">For example, your code could be myRS.UpdateBatch or .</span></span> <span data-ttu-id="693c7-123">ADO **Recordset** を使用している場合は、 [UpdateBatch](updatebatch-method-ado.md) メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="693c7-123">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="693c7-124">**CreateRecordset** メソッドで作成した **Recordset** オブジェクトには、 [UpdateBatch](createrecordset-method-rds.md) を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="693c7-124">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="693c7-125">などのコードは myRS.UpdateBatch または ADC1 する。Recordset.UpdateBatch。</span><span class="sxs-lookup"><span data-stu-id="693c7-125">For example, your code could be myRS.UpdateBatch or ADC1.Recordset.UpdateBatch .</span></span>
