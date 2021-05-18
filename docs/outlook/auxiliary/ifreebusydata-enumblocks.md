---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: 指定した時間範囲内のユーザーのデータの空き時間情報ブロックを列挙するインターフェイスを取得します。
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317557"
---
# <a name="ifreebusydataenumblocks"></a><span data-ttu-id="9d45a-103">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="9d45a-103">IFreeBusyData::EnumBlocks</span></span>

<span data-ttu-id="9d45a-104">指定した時間範囲内のユーザーのデータの空き時間情報ブロックを列挙するインターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="9d45a-104">Gets an interface that enumerates free/busy blocks of data for a user within a specified time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9d45a-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="9d45a-105">Quick info</span></span>

<span data-ttu-id="9d45a-106">[「IFreeBusyData」を参照してください](ifreebusydata.md)。</span><span class="sxs-lookup"><span data-stu-id="9d45a-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="9d45a-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9d45a-107">Parameters</span></span>

<span data-ttu-id="9d45a-108">_ppenumfb_</span><span class="sxs-lookup"><span data-stu-id="9d45a-108">_ppenumfb_</span></span>
  
> <span data-ttu-id="9d45a-109">[out]空き時間情報ブロックを列挙するインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="9d45a-109">[out] An interface to enumerate free/busy blocks.</span></span>
    
<span data-ttu-id="9d45a-110">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="9d45a-110">_ftmStart_</span></span>
  
> <span data-ttu-id="9d45a-111">[in]列挙の開始時刻。</span><span class="sxs-lookup"><span data-stu-id="9d45a-111">[in] The start time for the enumeration.</span></span> <span data-ttu-id="9d45a-112">これは [FILETIME で表されます](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx)。</span><span class="sxs-lookup"><span data-stu-id="9d45a-112">It is expressed in [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span></span>
    
<span data-ttu-id="9d45a-113">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="9d45a-113">_ftmEnd_</span></span>
  
> <span data-ttu-id="9d45a-114">[in]列挙の終了時刻。</span><span class="sxs-lookup"><span data-stu-id="9d45a-114">[in] The end time for the enumeration.</span></span> <span data-ttu-id="9d45a-115">これは **FILETIME で表されます**。</span><span class="sxs-lookup"><span data-stu-id="9d45a-115">It is expressed in **FILETIME**.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="9d45a-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="9d45a-116">Return values</span></span>

<span data-ttu-id="9d45a-117">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="9d45a-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9d45a-118">注釈</span><span class="sxs-lookup"><span data-stu-id="9d45a-118">Remarks</span></span>

<span data-ttu-id="9d45a-119">このメソッドは、詳細を取得する予定表アイテムの時間範囲を示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9d45a-119">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="9d45a-120">*ftmStart と* *ftmEnd* の値はキャッシュされ [、IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)の後続の呼び出しで返されます。</span><span class="sxs-lookup"><span data-stu-id="9d45a-120">The values of  *ftmStart* and *ftmEnd* are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
<span data-ttu-id="9d45a-121">空き時間情報プロバイダーは、その後、返された [IEnumFBBlock](ienumfbblock.md) インターフェイスを使用して列挙にアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="9d45a-121">A free/busy provider can also subsequently use the returned [IEnumFBBlock](ienumfbblock.md) interface to access the enumeration.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9d45a-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="9d45a-122">See also</span></span>

- [<span data-ttu-id="9d45a-123">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="9d45a-123">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="9d45a-124">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="9d45a-124">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="9d45a-125">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="9d45a-125">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)
- [<span data-ttu-id="9d45a-126">空き時間情報データにアクセスするのに相対時間を使用する</span><span class="sxs-lookup"><span data-stu-id="9d45a-126">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

