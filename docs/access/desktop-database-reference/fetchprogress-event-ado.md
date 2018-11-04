---
title: FetchProgress イベント (ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 16292522aae34aa660a258247eeca881199e3fc8
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949524"
---
# <a name="fetchprogress-event-ado"></a><span data-ttu-id="23e17-102">FetchProgress イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="23e17-102">FetchProgress event (ADO)</span></span>

<span data-ttu-id="23e17-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="23e17-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23e17-104">非同期操作が長く続く場合、現在までに **Recordset** に取得された行数を報告するために [FetchProgress](recordset-object-ado.md) イベントが定期的に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="23e17-104">The **FetchProgress** event is called periodically during a lengthy asynchronous operation to report how many more rows have currently been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="23e17-105">構文</span><span class="sxs-lookup"><span data-stu-id="23e17-105">Syntax</span></span>

<span data-ttu-id="23e17-106">FetchProgress*の進行状況*、 *MaxProgress*、 *adStatus*、 *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="23e17-106">FetchProgress*Progress*, *MaxProgress*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="23e17-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e17-107">Parameters</span></span>

|<span data-ttu-id="23e17-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e17-108">Parameter</span></span>|<span data-ttu-id="23e17-109">説明</span><span class="sxs-lookup"><span data-stu-id="23e17-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="23e17-110">*Progress*</span><span class="sxs-lookup"><span data-stu-id="23e17-110">*Progress*</span></span> |<span data-ttu-id="23e17-111">フェッチ操作によって、現在までに取得したレコード数を表す長整数型 ( **Long** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="23e17-111">A **Long** value indicating the number of records that have currently been retrieved by the fetch operation.</span></span>|
|<span data-ttu-id="23e17-112">*MaxProgress*</span><span class="sxs-lookup"><span data-stu-id="23e17-112">*MaxProgress*</span></span> |<span data-ttu-id="23e17-113">取得する予定の最大レコード数を表す長整数型 ( **Long** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="23e17-113">A **Long** value indicating the maximum number of records expected to be retrieved.</span></span>|
|<span data-ttu-id="23e17-114">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="23e17-114">*adStatus*</span></span> |<span data-ttu-id="23e17-115">[EventStatusEnum](eventstatusenum.md) 状態値です。</span><span class="sxs-lookup"><span data-stu-id="23e17-115">An [EventStatusEnum](eventstatusenum.md) status value.</span></span>|
|<span data-ttu-id="23e17-116">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="23e17-116">*pRecordset*</span></span> |<span data-ttu-id="23e17-117">レコードの取得先のオブジェクトである **Recordset** オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="23e17-117">A **Recordset** object that is the object for which the records are being retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="23e17-118">解説</span><span class="sxs-lookup"><span data-stu-id="23e17-118">Remarks</span></span>

<span data-ttu-id="23e17-119">**FetchProgress**を使用して、子**レコード セット**に、場合は、*進捗状況*と*MaxProgress*パラメーターの値が基になる[カーソル サービス](microsoft-cursor-service-for-ole-db-ado-service-component.md)の行セットから派生したことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="23e17-119">When using **FetchProgress** with a child **Recordset**, be aware that the *Progress* and *MaxProgress* parameter values are derived from the underlying [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) rowset.</span></span> <span data-ttu-id="23e17-120">戻り値は、基になる行セットの全レコード数であり、現在のチャプターのレコード数だけではありません。</span><span class="sxs-lookup"><span data-stu-id="23e17-120">The values returned represent the total number of records in the underlying rowset, not just the number of records in the current chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="23e17-121">[!メモ] Microsoft Visual Basic で **FetchProgress** を使用するには、Visual Basic 6.0 以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="23e17-121">To use **FetchProgress** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>


