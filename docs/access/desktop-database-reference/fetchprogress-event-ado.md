---
title: FetchProgress イベント (ADO)
TOCTitle: FetchProgress Event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25d062f4ae7008df787394eeb9253b65d6f5d1c8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886194"
---
# <a name="fetchprogress-event-ado"></a><span data-ttu-id="39027-102">FetchProgress イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="39027-102">FetchProgress Event (ADO)</span></span>


<span data-ttu-id="39027-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="39027-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="39027-104">非同期操作が長く続く場合、現在までに **Recordset** に取得された行数を報告するために [FetchProgress](recordset-object-ado.md) イベントが定期的に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="39027-104">The **FetchProgress** event is called periodically during a lengthy asynchronous operation to report how many more rows have currently been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="39027-105">構文</span><span class="sxs-lookup"><span data-stu-id="39027-105">Syntax</span></span>

<span data-ttu-id="39027-106">FetchProgress*の進行状況*、 *MaxProgress*、 *adStatus*、 *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="39027-106">FetchProgress*Progress*, *MaxProgress*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="39027-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="39027-107">Parameters</span></span>

  - <span data-ttu-id="39027-108">*Progress*</span><span class="sxs-lookup"><span data-stu-id="39027-108">*Progress*</span></span>

  - <span data-ttu-id="39027-109">フェッチ操作によって、現在までに取得したレコード数を表す長整数型 ( **Long** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="39027-109">A **Long** value indicating the number of records that have currently been retrieved by the fetch operation.</span></span>

  - <span data-ttu-id="39027-110">*MaxProgress*</span><span class="sxs-lookup"><span data-stu-id="39027-110">*MaxProgress*</span></span>

  - <span data-ttu-id="39027-111">取得する予定の最大レコード数を表す長整数型 ( **Long** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="39027-111">A **Long** value indicating the maximum number of records expected to be retrieved.</span></span>

  - <span data-ttu-id="39027-112">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="39027-112">*adStatus*</span></span>

  - <span data-ttu-id="39027-113">[EventStatusEnum](eventstatusenum.md) 状態値です。</span><span class="sxs-lookup"><span data-stu-id="39027-113">An [EventStatusEnum](eventstatusenum.md) status value.</span></span>

  - <span data-ttu-id="39027-114">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="39027-114">*pRecordset*</span></span>

  - <span data-ttu-id="39027-115">レコードの取得先のオブジェクトである **Recordset** オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="39027-115">A **Recordset** object that is the object for which the records are being retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="39027-116">解説</span><span class="sxs-lookup"><span data-stu-id="39027-116">Remarks</span></span>

<span data-ttu-id="39027-117">**FetchProgress**を使用して、子**レコード セット**に、場合は、*進捗状況*と*MaxProgress*パラメーターの値が基になる[カーソル サービス](microsoft-cursor-service-for-ole-db-ado-service-component.md)の行セットから派生したことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="39027-117">When using **FetchProgress** with a child **Recordset**, be aware that the *Progress* and *MaxProgress* parameter values are derived from the underlying [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) rowset.</span></span> <span data-ttu-id="39027-118">戻り値は、基になる行セットの全レコード数であり、現在のチャプターのレコード数だけではありません。</span><span class="sxs-lookup"><span data-stu-id="39027-118">The values returned represent the total number of records in the underlying rowset, not just the number of records in the current chapter.</span></span>


> [!NOTE]
> <span data-ttu-id="39027-119">[!メモ] Microsoft Visual Basic で **FetchProgress** を使用するには、Visual Basic 6.0 以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="39027-119">To use **FetchProgress** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>


