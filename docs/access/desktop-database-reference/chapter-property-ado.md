---
title: Chapter プロパティ (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d7523a930feed7431bf8be0bbb7222a4b305483
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949398"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="13a75-102">Chapter プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="13a75-102">Chapter property (ADO)</span></span>

<span data-ttu-id="13a75-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="13a75-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="13a75-104">OLE DB Chapter オブジェクトを ADORecordsetConstruction オブジェクトから取得するか、または、OLE DB Chapter オブジェクトを ADORecordsetConstruction オブジェクトに設定します。</span><span class="sxs-lookup"><span data-stu-id="13a75-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="13a75-105">使用すると**に\_章\*\*\*\*章**オブジェクトを設定する行のサブセットになって、ADO**レコード セット**オブジェクトにします。</span><span class="sxs-lookup"><span data-stu-id="13a75-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="13a75-106">これにより、 **Rowset**オブジェクトのカレント チャプターが設定されます。</span><span class="sxs-lookup"><span data-stu-id="13a75-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="13a75-107">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="13a75-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="13a75-108">構文</span><span class="sxs-lookup"><span data-stu-id="13a75-108">Syntax</span></span>

<span data-ttu-id="13a75-109">HRESULT get\_章 (\[、戻り値を\]長\*plChapter)。</span><span class="sxs-lookup"><span data-stu-id="13a75-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="13a75-110">HRESULT に\_の章 (\[に\]長 lChapter)。</span><span class="sxs-lookup"><span data-stu-id="13a75-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="13a75-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="13a75-111">Parameters</span></span>

|<span data-ttu-id="13a75-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="13a75-112">Parameter</span></span>|<span data-ttu-id="13a75-113">説明</span><span class="sxs-lookup"><span data-stu-id="13a75-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="13a75-114">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="13a75-114">*plChapter*</span></span> |<span data-ttu-id="13a75-115">チャプターのハンドルへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="13a75-115">Pointer to the handle of a chapter.</span></span>|
|<span data-ttu-id="13a75-116">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="13a75-116">*LChapter*</span></span> |<span data-ttu-id="13a75-117">チャプターのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="13a75-117">Handle of a chapter.</span></span>|

## <a name="return-values"></a><span data-ttu-id="13a75-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="13a75-118">Return values</span></span>

<span data-ttu-id="13a75-119">このプロパティのメソッドなどの標準の HRESULT 値を返します。\_[ok] および E\_は失敗します。</span><span class="sxs-lookup"><span data-stu-id="13a75-119">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="13a75-120">対象</span><span class="sxs-lookup"><span data-stu-id="13a75-120">Applies To</span></span>

[<span data-ttu-id="13a75-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="13a75-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

