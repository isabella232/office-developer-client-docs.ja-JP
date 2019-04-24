---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: 指定した各ユーザーについて、時間範囲内のデータの空き時間ブロックを列挙するためのインターフェイスを返します。
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319405"
---
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="07837-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="07837-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="07837-104">指定した各ユーザーについて、時間範囲内のデータの空き時間ブロックを列挙するためのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="07837-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="07837-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="07837-105">Quick info</span></span>

<span data-ttu-id="07837-106">[IFreeBusySupport](ifreebusysupport.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07837-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="07837-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07837-107">Parameters</span></span>

<span data-ttu-id="07837-108">_cmax_</span><span class="sxs-lookup"><span data-stu-id="07837-108">_cMax_</span></span>
  
> <span data-ttu-id="07837-109">順番取得する[IFreeBusyData](ifreebusydata.md)インターフェイスの数を指定します。</span><span class="sxs-lookup"><span data-stu-id="07837-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="07837-110">_rgfbuser_</span><span class="sxs-lookup"><span data-stu-id="07837-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="07837-111">順番データを取得する空き時間情報ユーザーの配列。</span><span class="sxs-lookup"><span data-stu-id="07837-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="07837-112">_prgfbdata_</span><span class="sxs-lookup"><span data-stu-id="07837-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="07837-113">順番読み上げ[fbuser](fbuser.md)構造の_rgfbuser_配列に対応する**IFreeBusyData**インターフェイスの配列。</span><span class="sxs-lookup"><span data-stu-id="07837-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="07837-114">このポインターの配列は、呼び出し元によって割り当てられ、呼び出し元によって解放されます。</span><span class="sxs-lookup"><span data-stu-id="07837-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="07837-115">呼び出し元が実行されたときに、参照されている実際のインターフェイスは解放されます。</span><span class="sxs-lookup"><span data-stu-id="07837-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="07837-116">_phrStatus_</span><span class="sxs-lookup"><span data-stu-id="07837-116">_phrStatus_</span></span>
  
> <span data-ttu-id="07837-117">読み上げそれぞれの対応する**IFreeBusyData**インターフェイスを取得するための**HRESULT**結果の配列。</span><span class="sxs-lookup"><span data-stu-id="07837-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="07837-118">値は NULL である場合があります。</span><span class="sxs-lookup"><span data-stu-id="07837-118">The value may be NULL.</span></span> <span data-ttu-id="07837-119">対応する_prgfbdata_が有効な場合、結果は S_OK に設定されます。</span><span class="sxs-lookup"><span data-stu-id="07837-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="07837-120">_pcread_</span><span class="sxs-lookup"><span data-stu-id="07837-120">_pcRead_</span></span>
  
>  <span data-ttu-id="07837-121">読み上げ**IFreeBusyData**インターフェイスが検出された実際のユーザー数。</span><span class="sxs-lookup"><span data-stu-id="07837-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="07837-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="07837-122">Return values</span></span>

<span data-ttu-id="07837-123">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="07837-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="07837-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="07837-124">See also</span></span>

- [<span data-ttu-id="07837-125">定数 (空き時間情報 API)</span><span class="sxs-lookup"><span data-stu-id="07837-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

