---
title: fetchprogress イベント (ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d863f51e7836acdc577ecd720df77114ed66f067
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293183"
---
# <a name="fetchprogress-event-ado"></a><span data-ttu-id="24b74-102">fetchprogress イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="24b74-102">FetchProgress event (ADO)</span></span>

<span data-ttu-id="24b74-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="24b74-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="24b74-104">非同期操作が長く続く場合、現在までに [Recordset](recordset-object-ado.md) に取得された行数を報告するために **FetchProgress** イベントが定期的に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="24b74-104">The **FetchProgress** event is called periodically during a lengthy asynchronous operation to report how many more rows have currently been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="24b74-105">構文</span><span class="sxs-lookup"><span data-stu-id="24b74-105">Syntax</span></span>

<span data-ttu-id="24b74-106">fetchprogress\*\* の進行状況、 *maxprogress*、 *adstatus*、 *precordset*</span><span class="sxs-lookup"><span data-stu-id="24b74-106">FetchProgress*Progress*, *MaxProgress*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="24b74-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="24b74-107">Parameters</span></span>

|<span data-ttu-id="24b74-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="24b74-108">Parameter</span></span>|<span data-ttu-id="24b74-109">説明</span><span class="sxs-lookup"><span data-stu-id="24b74-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="24b74-110">*Progress*</span><span class="sxs-lookup"><span data-stu-id="24b74-110">*Progress*</span></span> |<span data-ttu-id="24b74-111">フェッチ操作によって、現在までに取得したレコード数を表す長整数型 ( **Long** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="24b74-111">A **Long** value indicating the number of records that have currently been retrieved by the fetch operation.</span></span>|
|<span data-ttu-id="24b74-112">*maxprogress*</span><span class="sxs-lookup"><span data-stu-id="24b74-112">*MaxProgress*</span></span> |<span data-ttu-id="24b74-113">取得する予定の最大レコード数を表す長整数型 ( **Long** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="24b74-113">A **Long** value indicating the maximum number of records expected to be retrieved.</span></span>|
|<span data-ttu-id="24b74-114">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="24b74-114">*adStatus*</span></span> |<span data-ttu-id="24b74-115">[EventStatusEnum](eventstatusenum.md) 状態値です。</span><span class="sxs-lookup"><span data-stu-id="24b74-115">An [EventStatusEnum](eventstatusenum.md) status value.</span></span>|
|<span data-ttu-id="24b74-116">*precordset*</span><span class="sxs-lookup"><span data-stu-id="24b74-116">*pRecordset*</span></span> |<span data-ttu-id="24b74-117">レコードの取得先のオブジェクトである **Recordset** オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="24b74-117">A **Recordset** object that is the object for which the records are being retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="24b74-118">注釈</span><span class="sxs-lookup"><span data-stu-id="24b74-118">Remarks</span></span>

<span data-ttu-id="24b74-p101">子 **Recordset** を指定して **FetchProgress** を使用する場合、*Progress* パラメーターと *MaxProgress* パラメーターの値は、基になる [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) 行セットから派生します。戻り値は、基になる行セットの全レコード数であり、現在のチャプターのレコード数だけではありません。</span><span class="sxs-lookup"><span data-stu-id="24b74-p101">When using **FetchProgress** with a child **Recordset**, be aware that the *Progress* and *MaxProgress* parameter values are derived from the underlying [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) rowset. The values returned represent the total number of records in the underlying rowset, not just the number of records in the current chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="24b74-121">[!メモ] Microsoft Visual Basic で **FetchProgress** を使用するには、Visual Basic 6.0 以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="24b74-121">To use **FetchProgress** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>


