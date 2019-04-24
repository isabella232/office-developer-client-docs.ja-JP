---
title: Chapter プロパティ (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b4f4efc2ffab9f7996b2d805658b985badbaf87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296396"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="fb0f9-102">Chapter プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="fb0f9-102">Chapter property (ADO)</span></span>

<span data-ttu-id="fb0f9-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb0f9-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="fb0f9-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span><span class="sxs-lookup"><span data-stu-id="fb0f9-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="fb0f9-105">**put\_チャプター**を使用して**チャプター**オブジェクトを設定すると、行のサブセットが ADO **Recordset**オブジェクトになります。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="fb0f9-106">This sets the current chapter of the **Rowset** object.</span><span class="sxs-lookup"><span data-stu-id="fb0f9-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="fb0f9-107">値の取得と設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb0f9-108">構文</span><span class="sxs-lookup"><span data-stu-id="fb0f9-108">Syntax</span></span>

<span data-ttu-id="fb0f9-109">HRESULT get\_チャプター (\[out, retval\] long\* plchapter);</span><span class="sxs-lookup"><span data-stu-id="fb0f9-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="fb0f9-110">HRESULT put\_チャプター (\[\]長い lchapter)。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="fb0f9-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fb0f9-111">Parameters</span></span>

|<span data-ttu-id="fb0f9-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fb0f9-112">Parameter</span></span>|<span data-ttu-id="fb0f9-113">説明</span><span class="sxs-lookup"><span data-stu-id="fb0f9-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="fb0f9-114">*plchapter*</span><span class="sxs-lookup"><span data-stu-id="fb0f9-114">*plChapter*</span></span> |<span data-ttu-id="fb0f9-115">チャプターのハンドルへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-115">Pointer to the handle of a chapter.</span></span>|
|<span data-ttu-id="fb0f9-116">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="fb0f9-116">*LChapter*</span></span> |<span data-ttu-id="fb0f9-117">チャプターのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-117">Handle of a chapter.</span></span>|

## <a name="return-values"></a><span data-ttu-id="fb0f9-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="fb0f9-118">Return values</span></span>

<span data-ttu-id="fb0f9-119">このプロパティメソッドは、S\_OK および E\_FAIL を含む標準の HRESULT 値を返します。</span><span class="sxs-lookup"><span data-stu-id="fb0f9-119">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="fb0f9-120">対象</span><span class="sxs-lookup"><span data-stu-id="fb0f9-120">Applies To</span></span>

[<span data-ttu-id="fb0f9-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="fb0f9-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

