---
title: RowPosition プロパティ (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84d3ad7cc5b3d43b15ac1113f6fa00932678ebc3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720962"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="ff171-102">RowPosition プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="ff171-102">RowPosition property (ADO)</span></span>

<span data-ttu-id="ff171-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ff171-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ff171-104">**ADORecordsetConstruction** オブジェクトの OLE DB **RowPosition** オブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ff171-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="ff171-105">使用すると**に\_RowPosition** **RowPosition**オブジェクトを設定するには、結果の**Recordset**オブジェクトでは、現在の行を特定するのには**RowPosition**オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="ff171-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="ff171-106">値の取得と設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="ff171-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff171-107">構文</span><span class="sxs-lookup"><span data-stu-id="ff171-107">Syntax</span></span>

<span data-ttu-id="ff171-108">HRESULT get\_RowPosition (\[、戻り値を\]IUnknown\* \* ppRowPos)。</span><span class="sxs-lookup"><span data-stu-id="ff171-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="ff171-109">HRESULT に\_RowPosition (\[の\]IUnknown\* pRowPos)。</span><span class="sxs-lookup"><span data-stu-id="ff171-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="ff171-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ff171-110">Parameters</span></span>

|<span data-ttu-id="ff171-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ff171-111">Parameter</span></span>|<span data-ttu-id="ff171-112">説明</span><span class="sxs-lookup"><span data-stu-id="ff171-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ff171-113">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="ff171-113">*ppRowPos*</span></span> |<span data-ttu-id="ff171-114">OLE DB **RowPosition** オブジェクトを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="ff171-114">Pointer to an OLE DB **RowPosition** object.</span></span>|
|<span data-ttu-id="ff171-115">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="ff171-115">*PRowPos*</span></span> |<span data-ttu-id="ff171-116">OLE DB **RowPosition** オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="ff171-116">An OLE DB **RowPosition** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="ff171-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="ff171-117">Return values</span></span>

<span data-ttu-id="ff171-118">このプロパティのメソッドなどの標準の HRESULT 値を返します。\_[ok] および E\_は失敗します。</span><span class="sxs-lookup"><span data-stu-id="ff171-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff171-119">解説</span><span class="sxs-lookup"><span data-stu-id="ff171-119">Remarks</span></span>

<span data-ttu-id="ff171-p102">このプロパティを設定したときに、 **RowPosition** オブジェクトの **Rowset** オブジェクトと **Recordset** オブジェクトの **Rowset** オブジェクトが異なる場合、前者が後者よりも優先されます。同様の動作が **RowPosition** の現在の **Chapter** にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="ff171-p102">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="ff171-122">適用対象</span><span class="sxs-lookup"><span data-stu-id="ff171-122">Applies to</span></span>

[<span data-ttu-id="ff171-123">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="ff171-123">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

