---
title: rowposition プロパティ (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84d3ad7cc5b3d43b15ac1113f6fa00932678ebc3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306861"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="d01cd-102">rowposition プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="d01cd-102">RowPosition property (ADO)</span></span>

<span data-ttu-id="d01cd-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="d01cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d01cd-104">**ADORecordsetConstruction** オブジェクトの OLE DB **RowPosition** オブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d01cd-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="d01cd-105">**\_put rowposition**を使用して**rowposition**オブジェクトを設定すると、結果の**Recordset**オブジェクトは**rowposition**オブジェクトを使用して現在の行を特定します。</span><span class="sxs-lookup"><span data-stu-id="d01cd-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="d01cd-106">値の取得と設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="d01cd-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d01cd-107">構文</span><span class="sxs-lookup"><span data-stu-id="d01cd-107">Syntax</span></span>

<span data-ttu-id="d01cd-108">HRESULT get\_rowposition (\[out, retval\] IUnknown\* \* ppRowPos);</span><span class="sxs-lookup"><span data-stu-id="d01cd-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="d01cd-109">HRESULT put\_(\[\] IUnknown\* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="d01cd-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="d01cd-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d01cd-110">Parameters</span></span>

|<span data-ttu-id="d01cd-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d01cd-111">Parameter</span></span>|<span data-ttu-id="d01cd-112">説明</span><span class="sxs-lookup"><span data-stu-id="d01cd-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d01cd-113">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="d01cd-113">*ppRowPos*</span></span> |<span data-ttu-id="d01cd-114">OLE DB **RowPosition** オブジェクトを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="d01cd-114">Pointer to an OLE DB **RowPosition** object.</span></span>|
|<span data-ttu-id="d01cd-115">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="d01cd-115">*PRowPos*</span></span> |<span data-ttu-id="d01cd-116">OLE DB **RowPosition** オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="d01cd-116">An OLE DB **RowPosition** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="d01cd-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="d01cd-117">Return values</span></span>

<span data-ttu-id="d01cd-118">このプロパティメソッドは、S\_OK および E\_FAIL を含む標準の HRESULT 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d01cd-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d01cd-119">注釈</span><span class="sxs-lookup"><span data-stu-id="d01cd-119">Remarks</span></span>

<span data-ttu-id="d01cd-p102">このプロパティを設定したときに、**RowPosition** オブジェクトの **Rowset** オブジェクトと **Recordset** オブジェクトの **Rowset** オブジェクトが異なる場合、前者が後者よりも優先されます。同様の動作が **RowPosition** の現在の **Chapter** にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="d01cd-p102">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="d01cd-122">適用対象</span><span class="sxs-lookup"><span data-stu-id="d01cd-122">Applies to</span></span>

[<span data-ttu-id="d01cd-123">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="d01cd-123">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

