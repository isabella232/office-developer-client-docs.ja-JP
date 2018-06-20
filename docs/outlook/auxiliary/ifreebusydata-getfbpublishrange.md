---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: ユーザーのデータのブロックの空き時間情報の列挙型の事前に設定された時間の範囲を取得します。
ms.openlocfilehash: 2a322a43da38a0b902789f4c83baaabd769154c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799337"
---
# <a name="ifreebusydatagetfbpublishrange"></a><span data-ttu-id="e273c-103">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="e273c-103">IFreeBusyData::GetFBPublishRange</span></span>

<span data-ttu-id="e273c-104">ユーザーのデータのブロックの空き時間情報の列挙型の事前に設定された時間の範囲を取得します。</span><span class="sxs-lookup"><span data-stu-id="e273c-104">Gets a preset time range for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e273c-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e273c-105">Quick info</span></span>

<span data-ttu-id="e273c-106">[IFreeBusyData](ifreebusydata.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e273c-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="e273c-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="e273c-107">Parameters</span></span>

<span data-ttu-id="e273c-108">_prtmStart_</span><span class="sxs-lookup"><span data-stu-id="e273c-108">_prtmStart_</span></span>
  
> <span data-ttu-id="e273c-109">[out]空き時間情報の開始時刻の相対的な値です。</span><span class="sxs-lookup"><span data-stu-id="e273c-109">[out] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="e273c-110">この値は、1601 年 1 月 1 日以降の分の数です。</span><span class="sxs-lookup"><span data-stu-id="e273c-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="e273c-111">_prtmEnd_</span><span class="sxs-lookup"><span data-stu-id="e273c-111">_prtmEnd_</span></span>
  
> <span data-ttu-id="e273c-112">[out]空き時間情報の最後の時間の相対値です。</span><span class="sxs-lookup"><span data-stu-id="e273c-112">[out] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="e273c-113">この値は、1601 年 1 月 1 日以降の分の数です。</span><span class="sxs-lookup"><span data-stu-id="e273c-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="e273c-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="e273c-114">Return values</span></span>

<span data-ttu-id="e273c-115">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="e273c-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e273c-116">解釈</span><span class="sxs-lookup"><span data-stu-id="e273c-116">Remarks</span></span>

<span data-ttu-id="e273c-117">空き/予約済みのプロバイダーには、列挙体の時間範囲を設定するには、 [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)または[IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e273c-117">A free/busy provider calls [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) to set the time range for an enumeration.</span></span> <span data-ttu-id="e273c-118">1601 年 4 月 1 日、00:00:00Z と 11:59:59Z が 4500 年 8 月 31 日間、 **prtmStart**および**prtmEnd**の既定値を設定する必要があります[IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)または[IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)のいずれかが呼び出されなかった場合、それぞれ。</span><span class="sxs-lookup"><span data-stu-id="e273c-118">If either [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) has not been called, the default values for **prtmStart** and **prtmEnd** must be set between April 1st, 1601 00:00:00Z and August 31, 4500 11:59:59Z respectively.</span></span> <span data-ttu-id="e273c-119">さらに、開始時刻を終了時刻より大きい値を設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="e273c-119">Additionally, you should not set the start time to be greater than the end time.</span></span> 
  
<span data-ttu-id="e273c-120">**IFreeBusyData::GetFBPublishRange**は、 **IFreeBusyData::EnumBlocks**または**IFreeBusyData::SetFBRange**の最新の呼び出しによってキャッシュされた時間の範囲の値の設定を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e273c-120">**IFreeBusyData::GetFBPublishRange** must return the cached values for the time range set by the most recent call for **IFreeBusyData::EnumBlocks** or **IFreeBusyData::SetFBRange**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e273c-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="e273c-121">See also</span></span>

- [<span data-ttu-id="e273c-122">空き時間情報データにアクセスする相対時間を使用します。</span><span class="sxs-lookup"><span data-stu-id="e273c-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)
- [<span data-ttu-id="e273c-123">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="e273c-123">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="e273c-124">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="e273c-124">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)

