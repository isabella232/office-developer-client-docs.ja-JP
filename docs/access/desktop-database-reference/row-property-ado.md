---
title: 行プロパティ-ActiveX データオブジェクト (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4beaa742bfc46ecd32fc04733c3e6ddaf12aa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306483"
---
# <a name="row-property-ado"></a><span data-ttu-id="86373-102">Row プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="86373-102">Row property (ADO)</span></span>

<span data-ttu-id="86373-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="86373-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86373-104">**ADORecordConstruction** オブジェクトの OLE DB **Row** オブジェクトを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="86373-104">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="86373-105">**put\_row**を使用して**row**オブジェクトを設定すると、行は ADO **Record**オブジェクトになります。</span><span class="sxs-lookup"><span data-stu-id="86373-105">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="86373-106">値の取得と設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="86373-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="86373-107">構文</span><span class="sxs-lookup"><span data-stu-id="86373-107">Syntax</span></span>

<span data-ttu-id="86373-108">HRESULT get\_行 (\[out, retval\] IUnknown\* \* pprow);</span><span class="sxs-lookup"><span data-stu-id="86373-108">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="86373-109">HRESULT put\_行 (\[\] IUnknown\* prow);</span><span class="sxs-lookup"><span data-stu-id="86373-109">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="86373-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="86373-110">Parameters</span></span>

|<span data-ttu-id="86373-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="86373-111">Parameter</span></span>|<span data-ttu-id="86373-112">説明</span><span class="sxs-lookup"><span data-stu-id="86373-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="86373-113">*pprow*</span><span class="sxs-lookup"><span data-stu-id="86373-113">*ppRow*</span></span> |<span data-ttu-id="86373-114">OLE DB **Row** オブジェクトを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="86373-114">Pointer to an OLE DB **Row** object.</span></span>|
|<span data-ttu-id="86373-115">*PRow*</span><span class="sxs-lookup"><span data-stu-id="86373-115">*PRow*</span></span> |<span data-ttu-id="86373-116">OLE DB **Row** オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="86373-116">An OLE DB **Row** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="86373-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="86373-117">Return values</span></span>

<span data-ttu-id="86373-118">このプロパティメソッドは、S\_OK および E\_FAIL を含む標準の HRESULT 値を返します。</span><span class="sxs-lookup"><span data-stu-id="86373-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="86373-119">適用対象</span><span class="sxs-lookup"><span data-stu-id="86373-119">Applies to</span></span>

[<span data-ttu-id="86373-120">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="86373-120">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

