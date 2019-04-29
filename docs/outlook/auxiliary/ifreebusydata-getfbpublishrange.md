---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: ユーザーのデータの空き時間ブロックの列挙の事前設定の時間範囲を取得します。
ms.openlocfilehash: 26951ea6a885f8d0e5e6a2fb5bcf9a63069c7f44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430078"
---
# <a name="ifreebusydatagetfbpublishrange"></a><span data-ttu-id="25276-103">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="25276-103">IFreeBusyData::GetFBPublishRange</span></span>

<span data-ttu-id="25276-104">ユーザーのデータの空き時間ブロックの列挙の事前設定の時間範囲を取得します。</span><span class="sxs-lookup"><span data-stu-id="25276-104">Gets a preset time range for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="25276-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="25276-105">Quick info</span></span>

<span data-ttu-id="25276-106">[IFreeBusyData](ifreebusydata.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25276-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="25276-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="25276-107">Parameters</span></span>

<span data-ttu-id="25276-108">_prtmstart_</span><span class="sxs-lookup"><span data-stu-id="25276-108">_prtmStart_</span></span>
  
> <span data-ttu-id="25276-109">読み上げ空き時間情報の開始の相対時間値。</span><span class="sxs-lookup"><span data-stu-id="25276-109">[out] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="25276-110">この値は、1601年1月1日からの経過時間 (分単位) です。</span><span class="sxs-lookup"><span data-stu-id="25276-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="25276-111">_prtmEnd_</span><span class="sxs-lookup"><span data-stu-id="25276-111">_prtmEnd_</span></span>
  
> <span data-ttu-id="25276-112">読み上げ空き時間情報の終了の相対時間値。</span><span class="sxs-lookup"><span data-stu-id="25276-112">[out] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="25276-113">この値は、1601年1月1日からの経過時間 (分単位) です。</span><span class="sxs-lookup"><span data-stu-id="25276-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="25276-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="25276-114">Return values</span></span>

<span data-ttu-id="25276-115">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="25276-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="25276-116">注釈</span><span class="sxs-lookup"><span data-stu-id="25276-116">Remarks</span></span>

<span data-ttu-id="25276-117">空き時間情報プロバイダーは、 [IFreeBusyData:: enumblocks](ifreebusydata-enumblocks.md)または[IFreeBusyData:: setfbrange](ifreebusydata-setfbrange.md)を呼び出して、列挙の時間範囲を設定します。</span><span class="sxs-lookup"><span data-stu-id="25276-117">A free/busy provider calls [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) to set the time range for an enumeration.</span></span> <span data-ttu-id="25276-118">[IFreeBusyData:: enumblocks](ifreebusydata-enumblocks.md)または[IFreeBusyData:: setfbrange](ifreebusydata-setfbrange.md)がまだ呼び出されていない場合は、 **prtmstart**および**prtmEnd**の既定値は4月1日、1601 00:00: 00z、4500 11 年8月31日の間に設定する必要があります。59z4.3.</span><span class="sxs-lookup"><span data-stu-id="25276-118">If either [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) has not been called, the default values for **prtmStart** and **prtmEnd** must be set between April 1st, 1601 00:00:00Z and August 31, 4500 11:59:59Z respectively.</span></span> <span data-ttu-id="25276-119">さらに、開始時刻を終了時刻よりも大きい値に設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="25276-119">Additionally, you should not set the start time to be greater than the end time.</span></span> 
  
<span data-ttu-id="25276-120">**IFreeBusyData:: getfbpublishrange**は、 **IFreeBusyData:: enumblocks**または**IFreeBusyData:: setfbrange**最新の呼び出しによって設定された時間範囲のキャッシュされた値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="25276-120">**IFreeBusyData::GetFBPublishRange** must return the cached values for the time range set by the most recent call for **IFreeBusyData::EnumBlocks** or **IFreeBusyData::SetFBRange**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="25276-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="25276-121">See also</span></span>

- [<span data-ttu-id="25276-122">空き時間情報データにアクセスするのに相対時間を使用する</span><span class="sxs-lookup"><span data-stu-id="25276-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)
- [<span data-ttu-id="25276-123">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="25276-123">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="25276-124">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="25276-124">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)

