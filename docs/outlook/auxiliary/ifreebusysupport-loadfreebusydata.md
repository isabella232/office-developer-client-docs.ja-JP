---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: 指定したユーザーごとに、時間範囲内のデータの空き時間情報ブロックを列挙するインターフェイスを返します。
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411233"
---
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="490f3-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="490f3-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="490f3-104">指定したユーザーごとに、時間範囲内のデータの空き時間情報ブロックを列挙するインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="490f3-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="490f3-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="490f3-105">Quick info</span></span>

<span data-ttu-id="490f3-106">[「IFreeBusySupport」を参照してください](ifreebusysupport.md)。</span><span class="sxs-lookup"><span data-stu-id="490f3-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="490f3-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="490f3-107">Parameters</span></span>

<span data-ttu-id="490f3-108">_cMax_</span><span class="sxs-lookup"><span data-stu-id="490f3-108">_cMax_</span></span>
  
> <span data-ttu-id="490f3-109">[in]返す [IFreeBusyData](ifreebusydata.md) インターフェイスの数。</span><span class="sxs-lookup"><span data-stu-id="490f3-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="490f3-110">_rgfbuser_</span><span class="sxs-lookup"><span data-stu-id="490f3-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="490f3-111">[in]データを取得する空き時間情報ユーザーの配列。</span><span class="sxs-lookup"><span data-stu-id="490f3-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="490f3-112">_prgfbdata_</span><span class="sxs-lookup"><span data-stu-id="490f3-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="490f3-113">[in][out][FBUser](fbuser.md)構造体の _rgfbuser_ 配列に対応する **IFreeBusyData** インターフェイスの配列。</span><span class="sxs-lookup"><span data-stu-id="490f3-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="490f3-114">このポインターの配列は、呼び出し元によって割り当て、呼び出し元によって解放されます。</span><span class="sxs-lookup"><span data-stu-id="490f3-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="490f3-115">呼び出し元が呼び出し元と一緒に実行されると、指す実際のインターフェイスが解放されます。</span><span class="sxs-lookup"><span data-stu-id="490f3-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="490f3-116">_phrStatus_</span><span class="sxs-lookup"><span data-stu-id="490f3-116">_phrStatus_</span></span>
  
> <span data-ttu-id="490f3-117">[out] **HRESULT の配列は** 、対応する各 **IFreeBusyData インターフェイスを取得するための結果** です。</span><span class="sxs-lookup"><span data-stu-id="490f3-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="490f3-118">値には NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="490f3-118">The value may be NULL.</span></span> <span data-ttu-id="490f3-119">対応する  _prgfbdata_ が有効S_OK場合、結果は値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="490f3-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="490f3-120">_pcRead_</span><span class="sxs-lookup"><span data-stu-id="490f3-120">_pcRead_</span></span>
  
>  <span data-ttu-id="490f3-121">[out] **IFreeBusyData** インターフェイスが見つかったユーザーの実際の数。</span><span class="sxs-lookup"><span data-stu-id="490f3-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="490f3-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="490f3-122">Return values</span></span>

<span data-ttu-id="490f3-123">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="490f3-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="490f3-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="490f3-124">See also</span></span>

- [<span data-ttu-id="490f3-125">定数 (空き時間情報 API)</span><span class="sxs-lookup"><span data-stu-id="490f3-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

