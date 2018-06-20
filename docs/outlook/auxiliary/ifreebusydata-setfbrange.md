---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: ユーザーの空き時間情報データ ブロックの列挙体の時間の範囲を設定します。
ms.openlocfilehash: 84a25a2dd43f594caa075d90e4f183086452184a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799355"
---
# <a name="ifreebusydatasetfbrange"></a><span data-ttu-id="ff882-103">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="ff882-103">IFreeBusyData::SetFBRange</span></span>

<span data-ttu-id="ff882-104">ユーザーの空き時間情報データ ブロックの列挙体の時間の範囲を設定します。</span><span class="sxs-lookup"><span data-stu-id="ff882-104">Sets the range of time for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ff882-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="ff882-105">Quick info</span></span>

<span data-ttu-id="ff882-106">[IFreeBusyData](ifreebusydata.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ff882-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a><span data-ttu-id="ff882-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="ff882-107">Parameters</span></span>

<span data-ttu-id="ff882-108">_rtmStart_</span><span class="sxs-lookup"><span data-stu-id="ff882-108">_rtmStart_</span></span>
  
> <span data-ttu-id="ff882-109">[in]空き時間情報の開始時刻の相対的な値です。</span><span class="sxs-lookup"><span data-stu-id="ff882-109">[in] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="ff882-110">この値は、1601 年 1 月 1 日以降の分の数です。</span><span class="sxs-lookup"><span data-stu-id="ff882-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="ff882-111">_rtmEnd_</span><span class="sxs-lookup"><span data-stu-id="ff882-111">_rtmEnd_</span></span>
  
> <span data-ttu-id="ff882-112">[in]空き時間情報の最後の時間の相対値です。</span><span class="sxs-lookup"><span data-stu-id="ff882-112">[in] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="ff882-113">この値は、1601 年 1 月 1 日以降の分の数です。</span><span class="sxs-lookup"><span data-stu-id="ff882-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="ff882-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="ff882-114">Return values</span></span>

<span data-ttu-id="ff882-115">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="ff882-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ff882-116">解釈</span><span class="sxs-lookup"><span data-stu-id="ff882-116">Remarks</span></span>

<span data-ttu-id="ff882-117">予定表のアイテムの詳細を取得するための時間の範囲を示すためにこのメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ff882-117">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="ff882-118">*FtmStart*と*ftmEnd*の値がキャッシュされ、 [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)の後続の呼び出しで返されます。</span><span class="sxs-lookup"><span data-stu-id="ff882-118">The values of  *ftmStart*  and  *ftmEnd*  are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ff882-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="ff882-119">See also</span></span>

- [<span data-ttu-id="ff882-120">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="ff882-120">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="ff882-121">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="ff882-121">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="ff882-122">空き時間情報データにアクセスする相対時間を使用します。</span><span class="sxs-lookup"><span data-stu-id="ff882-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

