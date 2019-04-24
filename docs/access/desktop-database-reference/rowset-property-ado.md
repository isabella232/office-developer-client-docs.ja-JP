---
title: Rowset プロパティ (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be2a4855b3411a11ddd5a76225acaa52344877a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306742"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="bb051-102">Rowset プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="bb051-102">Rowset property (ADO)</span></span>

<span data-ttu-id="bb051-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="bb051-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bb051-104">**ADORecordsetConstruction** オブジェクトの OLE DB **Rowset** オブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="bb051-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="bb051-105">put\_行セットを使用すると、行セットは ADO **Recordset**オブジェクトになります。</span><span class="sxs-lookup"><span data-stu-id="bb051-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="bb051-106">値の取得と設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="bb051-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb051-107">構文</span><span class="sxs-lookup"><span data-stu-id="bb051-107">Syntax</span></span>

<span data-ttu-id="bb051-108">HRESULT get\_行セット\[(out,\] retval\* \* IUnknown ppRowset);</span><span class="sxs-lookup"><span data-stu-id="bb051-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="bb051-109">HRESULT put\_行セット\[(\] IUnknown\* pRowset)。</span><span class="sxs-lookup"><span data-stu-id="bb051-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="bb051-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bb051-110">Parameters</span></span>

|<span data-ttu-id="bb051-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bb051-111">Parameter</span></span>|<span data-ttu-id="bb051-112">説明</span><span class="sxs-lookup"><span data-stu-id="bb051-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="bb051-113">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="bb051-113">*ppRowset*</span></span> |<span data-ttu-id="bb051-114">OLE DB **Rowset** オブジェクトを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="bb051-114">Pointer to an OLE DB **Rowset** object.</span></span>|
|<span data-ttu-id="bb051-115">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="bb051-115">*PRowset*</span></span> |<span data-ttu-id="bb051-116">OLE DB **Rowset** オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="bb051-116">An OLE DB **Rowset** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="bb051-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="bb051-117">Return values</span></span>

<span data-ttu-id="bb051-118">このプロパティメソッドは、S\_OK および E\_FAIL を含む標準の HRESULT 値を返します。</span><span class="sxs-lookup"><span data-stu-id="bb051-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="bb051-119">適用対象</span><span class="sxs-lookup"><span data-stu-id="bb051-119">Applies to</span></span>

[<span data-ttu-id="bb051-120">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="bb051-120">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

