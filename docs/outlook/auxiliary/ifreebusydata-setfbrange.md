---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: ユーザーのデータの空き時間情報ブロックの列挙の時間範囲を設定します。
ms.openlocfilehash: 4647453acb0e530521aa808f7f017e3e311644bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421663"
---
# <a name="ifreebusydatasetfbrange"></a><span data-ttu-id="b0c88-103">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="b0c88-103">IFreeBusyData::SetFBRange</span></span>

<span data-ttu-id="b0c88-104">ユーザーのデータの空き時間情報ブロックの列挙の時間範囲を設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c88-104">Sets the range of time for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b0c88-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b0c88-105">Quick info</span></span>

<span data-ttu-id="b0c88-106">[「IFreeBusyData」を参照してください](ifreebusydata.md)。</span><span class="sxs-lookup"><span data-stu-id="b0c88-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a><span data-ttu-id="b0c88-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b0c88-107">Parameters</span></span>

<span data-ttu-id="b0c88-108">_rtmStart_</span><span class="sxs-lookup"><span data-stu-id="b0c88-108">_rtmStart_</span></span>
  
> <span data-ttu-id="b0c88-109">[in]空き時間情報の開始の相対時間値。</span><span class="sxs-lookup"><span data-stu-id="b0c88-109">[in] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="b0c88-110">この値は、1601 年 1 月 1 日以降の分数です。</span><span class="sxs-lookup"><span data-stu-id="b0c88-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="b0c88-111">_rtmEnd_</span><span class="sxs-lookup"><span data-stu-id="b0c88-111">_rtmEnd_</span></span>
  
> <span data-ttu-id="b0c88-112">[in]空き時間情報の末尾の相対時間値。</span><span class="sxs-lookup"><span data-stu-id="b0c88-112">[in] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="b0c88-113">この値は、1601 年 1 月 1 日以降の分数です。</span><span class="sxs-lookup"><span data-stu-id="b0c88-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="b0c88-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="b0c88-114">Return values</span></span>

<span data-ttu-id="b0c88-115">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="b0c88-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b0c88-116">注釈</span><span class="sxs-lookup"><span data-stu-id="b0c88-116">Remarks</span></span>

<span data-ttu-id="b0c88-117">このメソッドは、詳細を取得する予定表アイテムの時間範囲を示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0c88-117">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="b0c88-118">*ftmStart と* *ftmEnd* の値はキャッシュされ [、IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)の後続の呼び出しで返されます。</span><span class="sxs-lookup"><span data-stu-id="b0c88-118">The values of  *ftmStart*  and  *ftmEnd*  are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b0c88-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="b0c88-119">See also</span></span>

- [<span data-ttu-id="b0c88-120">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="b0c88-120">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="b0c88-121">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="b0c88-121">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="b0c88-122">空き時間情報データにアクセスするのに相対時間を使用する</span><span class="sxs-lookup"><span data-stu-id="b0c88-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

