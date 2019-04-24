---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: ユーザーのデータの空き時間ブロックの列挙時間の範囲を設定します。
ms.openlocfilehash: 4647453acb0e530521aa808f7f017e3e311644bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317480"
---
# <a name="ifreebusydatasetfbrange"></a><span data-ttu-id="a9ddb-103">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="a9ddb-103">IFreeBusyData::SetFBRange</span></span>

<span data-ttu-id="a9ddb-104">ユーザーのデータの空き時間ブロックの列挙時間の範囲を設定します。</span><span class="sxs-lookup"><span data-stu-id="a9ddb-104">Sets the range of time for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a9ddb-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a9ddb-105">Quick info</span></span>

<span data-ttu-id="a9ddb-106">[IFreeBusyData](ifreebusydata.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9ddb-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a><span data-ttu-id="a9ddb-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a9ddb-107">Parameters</span></span>

<span data-ttu-id="a9ddb-108">_rtmstart_</span><span class="sxs-lookup"><span data-stu-id="a9ddb-108">_rtmStart_</span></span>
  
> <span data-ttu-id="a9ddb-109">順番空き時間情報の開始の相対時間値。</span><span class="sxs-lookup"><span data-stu-id="a9ddb-109">[in] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="a9ddb-110">この値は、1601年1月1日からの経過時間 (分単位) です。</span><span class="sxs-lookup"><span data-stu-id="a9ddb-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="a9ddb-111">_rtmEnd_</span><span class="sxs-lookup"><span data-stu-id="a9ddb-111">_rtmEnd_</span></span>
  
> <span data-ttu-id="a9ddb-112">順番空き時間情報の終了の相対時間値。</span><span class="sxs-lookup"><span data-stu-id="a9ddb-112">[in] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="a9ddb-113">この値は、1601年1月1日からの経過時間 (分単位) です。</span><span class="sxs-lookup"><span data-stu-id="a9ddb-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="a9ddb-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="a9ddb-114">Return values</span></span>

<span data-ttu-id="a9ddb-115">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="a9ddb-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a9ddb-116">解説</span><span class="sxs-lookup"><span data-stu-id="a9ddb-116">Remarks</span></span>

<span data-ttu-id="a9ddb-117">このメソッドは、詳細を取得する予定表アイテムの時間範囲を示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a9ddb-117">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="a9ddb-118">*ftmstart*および*ftmEnd*の値はキャッシュされ、その後の[IFreeBusyData:: getfbpublishrange](ifreebusydata-getfbpublishrange.md)の呼び出しで返されます。</span><span class="sxs-lookup"><span data-stu-id="a9ddb-118">The values of  *ftmStart*  and  *ftmEnd*  are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a9ddb-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9ddb-119">See also</span></span>

- [<span data-ttu-id="a9ddb-120">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="a9ddb-120">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="a9ddb-121">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="a9ddb-121">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="a9ddb-122">空き時間情報データにアクセスするのに相対時間を使用する</span><span class="sxs-lookup"><span data-stu-id="a9ddb-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

