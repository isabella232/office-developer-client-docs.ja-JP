---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: ユーザーごとに指定された、時間の範囲内のデータのブロックの空き時間情報を列挙するためのインターフェイスを返します。
ms.openlocfilehash: 9af5a40da9f0a831de7346b44cee9ca004c02300
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799340"
---
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="08ad2-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="08ad2-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="08ad2-104">ユーザーごとに指定された、時間の範囲内のデータのブロックの空き時間情報を列挙するためのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="08ad2-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="08ad2-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="08ad2-105">Quick info</span></span>

<span data-ttu-id="08ad2-106">[IFreeBusySupport](ifreebusysupport.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08ad2-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="08ad2-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="08ad2-107">Parameters</span></span>

<span data-ttu-id="08ad2-108">_cMax_</span><span class="sxs-lookup"><span data-stu-id="08ad2-108">_cMax_</span></span>
  
> <span data-ttu-id="08ad2-109">[in]返す[IFreeBusyData](ifreebusydata.md)のインタ フェースの数です。</span><span class="sxs-lookup"><span data-stu-id="08ad2-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="08ad2-110">_rgfbuser_</span><span class="sxs-lookup"><span data-stu-id="08ad2-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="08ad2-111">[in]データを取得するユーザーの空き時間情報の配列。</span><span class="sxs-lookup"><span data-stu-id="08ad2-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="08ad2-112">_prgfbdata_</span><span class="sxs-lookup"><span data-stu-id="08ad2-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="08ad2-113">[in][out]_Rgfbuser_ [FBUser](fbuser.md)構造体の配列に対応する**IFreeBusyData**インターフェイスの配列。</span><span class="sxs-lookup"><span data-stu-id="08ad2-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="08ad2-114">このポインターの配列は、呼び出し元によって割り当てられているし、呼び出し元によって解放されます。</span><span class="sxs-lookup"><span data-stu-id="08ad2-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="08ad2-115">示される実際のインターフェイスは、後に、呼び出し元に解放されます。</span><span class="sxs-lookup"><span data-stu-id="08ad2-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="08ad2-116">_phrStatus_</span><span class="sxs-lookup"><span data-stu-id="08ad2-116">_phrStatus_</span></span>
  
> <span data-ttu-id="08ad2-117">[out]**HRESULT**の配列は、それぞれ対応する**IFreeBusyData**インターフェイスを取得するため発生します。</span><span class="sxs-lookup"><span data-stu-id="08ad2-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="08ad2-118">値は NULL である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="08ad2-118">The value may be NULL.</span></span> <span data-ttu-id="08ad2-119">結果は、対応する_prgfbdata_が有効な場合は S_OK に設定されています。</span><span class="sxs-lookup"><span data-stu-id="08ad2-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="08ad2-120">_pcRead_</span><span class="sxs-lookup"><span data-stu-id="08ad2-120">_pcRead_</span></span>
  
>  <span data-ttu-id="08ad2-121">[out]**IFreeBusyData**インタ フェースが検出されましたユーザーの実際の数です。</span><span class="sxs-lookup"><span data-stu-id="08ad2-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="08ad2-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="08ad2-122">Return values</span></span>

<span data-ttu-id="08ad2-123">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="08ad2-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="08ad2-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="08ad2-124">See also</span></span>

- [<span data-ttu-id="08ad2-125">定数 (空き時間情報の API)</span><span class="sxs-lookup"><span data-stu-id="08ad2-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

