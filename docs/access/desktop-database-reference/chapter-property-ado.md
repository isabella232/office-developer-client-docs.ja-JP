---
title: Chapter プロパティ (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95ed1b9b7c048353950b2481c7fefe2211b2799b
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944278"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="3ab1f-102">Chapter プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="3ab1f-102">Chapter property (ADO)</span></span>


<span data-ttu-id="3ab1f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3ab1f-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="3ab1f-104">OLE DB Chapter オブジェクトを ADORecordsetConstruction オブジェクトから取得するか、または、OLE DB Chapter オブジェクトを ADORecordsetConstruction オブジェクトに設定します。</span><span class="sxs-lookup"><span data-stu-id="3ab1f-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="3ab1f-105">使用すると**に\_章\*\*\*\*章**オブジェクトを設定する行のサブセットになって、ADO**レコード セット**オブジェクトにします。</span><span class="sxs-lookup"><span data-stu-id="3ab1f-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="3ab1f-106">これにより、 **Rowset**オブジェクトのカレント チャプターが設定されます。</span><span class="sxs-lookup"><span data-stu-id="3ab1f-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="3ab1f-107">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="3ab1f-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ab1f-108">構文</span><span class="sxs-lookup"><span data-stu-id="3ab1f-108">Syntax</span></span>

<span data-ttu-id="3ab1f-109">HRESULT get\_章 (\[、戻り値を\]長\*plChapter)。</span><span class="sxs-lookup"><span data-stu-id="3ab1f-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="3ab1f-110">HRESULT に\_の章 (\[に\]長 lChapter)。</span><span class="sxs-lookup"><span data-stu-id="3ab1f-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="3ab1f-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3ab1f-111">Parameters</span></span>

- <span data-ttu-id="3ab1f-112">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="3ab1f-112">*plChapter*</span></span>

  - <span data-ttu-id="3ab1f-113">チャプターのハンドルへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="3ab1f-113">Pointer to the handle of a chapter.</span></span>

- <span data-ttu-id="3ab1f-114">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="3ab1f-114">*LChapter*</span></span>

  - <span data-ttu-id="3ab1f-115">チャプターのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="3ab1f-115">Handle of a chapter.</span></span>

## <a name="return-values"></a><span data-ttu-id="3ab1f-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="3ab1f-116">Return values</span></span>

<span data-ttu-id="3ab1f-117">このプロパティのメソッドなどの標準の HRESULT 値を返します。\_[ok] および E\_は失敗します。</span><span class="sxs-lookup"><span data-stu-id="3ab1f-117">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="3ab1f-118">対象</span><span class="sxs-lookup"><span data-stu-id="3ab1f-118">Applies To</span></span>

[<span data-ttu-id="3ab1f-119">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="3ab1f-119">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

