---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: 指定した時間範囲内のユーザーのデータの空き時間ブロックを列挙するインターフェイスを取得します。
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317557"
---
# <a name="ifreebusydataenumblocks"></a><span data-ttu-id="b79a0-103">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="b79a0-103">IFreeBusyData::EnumBlocks</span></span>

<span data-ttu-id="b79a0-104">指定した時間範囲内のユーザーのデータの空き時間ブロックを列挙するインターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="b79a0-104">Gets an interface that enumerates free/busy blocks of data for a user within a specified time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b79a0-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b79a0-105">Quick info</span></span>

<span data-ttu-id="b79a0-106">[IFreeBusyData](ifreebusydata.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b79a0-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="b79a0-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b79a0-107">Parameters</span></span>

<span data-ttu-id="b79a0-108">_ppenumfb_</span><span class="sxs-lookup"><span data-stu-id="b79a0-108">_ppenumfb_</span></span>
  
> <span data-ttu-id="b79a0-109">読み上げ空き時間ブロックを列挙するためのインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="b79a0-109">[out] An interface to enumerate free/busy blocks.</span></span>
    
<span data-ttu-id="b79a0-110">_ftmstart_</span><span class="sxs-lookup"><span data-stu-id="b79a0-110">_ftmStart_</span></span>
  
> <span data-ttu-id="b79a0-111">順番列挙の開始時刻。</span><span class="sxs-lookup"><span data-stu-id="b79a0-111">[in] The start time for the enumeration.</span></span> <span data-ttu-id="b79a0-112">これは、 [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx)で表されます。</span><span class="sxs-lookup"><span data-stu-id="b79a0-112">It is expressed in [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span></span>
    
<span data-ttu-id="b79a0-113">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="b79a0-113">_ftmEnd_</span></span>
  
> <span data-ttu-id="b79a0-114">順番列挙の終了時刻。</span><span class="sxs-lookup"><span data-stu-id="b79a0-114">[in] The end time for the enumeration.</span></span> <span data-ttu-id="b79a0-115">これは、 **FILETIME**で表されます。</span><span class="sxs-lookup"><span data-stu-id="b79a0-115">It is expressed in **FILETIME**.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b79a0-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="b79a0-116">Return values</span></span>

<span data-ttu-id="b79a0-117">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="b79a0-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b79a0-118">解説</span><span class="sxs-lookup"><span data-stu-id="b79a0-118">Remarks</span></span>

<span data-ttu-id="b79a0-119">このメソッドは、詳細を取得する予定表アイテムの時間範囲を示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b79a0-119">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="b79a0-120">*ftmstart*および*ftmEnd*の値はキャッシュされ、その後の[IFreeBusyData:: getfbpublishrange](ifreebusydata-getfbpublishrange.md)の呼び出しで返されます。</span><span class="sxs-lookup"><span data-stu-id="b79a0-120">The values of  *ftmStart* and *ftmEnd* are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
<span data-ttu-id="b79a0-121">空き時間プロバイダーは、返された[IEnumFBBlock](ienumfbblock.md)インターフェイスを使用して列挙にアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="b79a0-121">A free/busy provider can also subsequently use the returned [IEnumFBBlock](ienumfbblock.md) interface to access the enumeration.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b79a0-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="b79a0-122">See also</span></span>

- [<span data-ttu-id="b79a0-123">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="b79a0-123">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="b79a0-124">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="b79a0-124">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="b79a0-125">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="b79a0-125">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)
- [<span data-ttu-id="b79a0-126">空き時間情報データにアクセスするのに相対時間を使用する</span><span class="sxs-lookup"><span data-stu-id="b79a0-126">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

