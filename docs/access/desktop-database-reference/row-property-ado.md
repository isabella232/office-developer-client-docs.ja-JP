---
title: 行のプロパティを ActiveX データ オブジェクト (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4beaa742bfc46ecd32fc04733c3e6ddaf12aa2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715005"
---
# <a name="row-property-ado"></a><span data-ttu-id="34a06-102">Row プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="34a06-102">Row property (ADO)</span></span>

<span data-ttu-id="34a06-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="34a06-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="34a06-104">**ADORecordConstruction** オブジェクトの OLE DB **Row** オブジェクトを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="34a06-104">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="34a06-105">使用すると**に\_行\*\*\*\*行**オブジェクトを設定するのには、行になって ADO**レコード**オブジェクトにします。</span><span class="sxs-lookup"><span data-stu-id="34a06-105">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="34a06-106">値の取得と設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="34a06-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="34a06-107">構文</span><span class="sxs-lookup"><span data-stu-id="34a06-107">Syntax</span></span>

<span data-ttu-id="34a06-108">HRESULT get\_行 (\[、戻り値を\]IUnknown\* \* ppRow)。</span><span class="sxs-lookup"><span data-stu-id="34a06-108">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="34a06-109">HRESULT に\_の行 (\[の\]IUnknown\* pRow)。</span><span class="sxs-lookup"><span data-stu-id="34a06-109">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="34a06-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="34a06-110">Parameters</span></span>

|<span data-ttu-id="34a06-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="34a06-111">Parameter</span></span>|<span data-ttu-id="34a06-112">説明</span><span class="sxs-lookup"><span data-stu-id="34a06-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="34a06-113">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="34a06-113">*ppRow*</span></span> |<span data-ttu-id="34a06-114">OLE DB **Row** オブジェクトを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="34a06-114">Pointer to an OLE DB **Row** object.</span></span>|
|<span data-ttu-id="34a06-115">*PRow*</span><span class="sxs-lookup"><span data-stu-id="34a06-115">*PRow*</span></span> |<span data-ttu-id="34a06-116">OLE DB **Row** オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="34a06-116">An OLE DB **Row** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="34a06-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="34a06-117">Return values</span></span>

<span data-ttu-id="34a06-118">このプロパティのメソッドなどの標準の HRESULT 値を返します。\_[ok] および E\_は失敗します。</span><span class="sxs-lookup"><span data-stu-id="34a06-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="34a06-119">適用対象</span><span class="sxs-lookup"><span data-stu-id="34a06-119">Applies to</span></span>

[<span data-ttu-id="34a06-120">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="34a06-120">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

