---
title: MTSID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MTSID
api_type:
- COM
ms.assetid: 3d9bc643-332f-4c8e-83e6-ce9b15711945
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 59e9cf23aed2a389384318468c3853cd41c9ec1e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585683"
---
# <a name="mtsid"></a><span data-ttu-id="bf49f-103">MTSID</span><span class="sxs-lookup"><span data-stu-id="bf49f-103">MTSID</span></span>

  
  
<span data-ttu-id="bf49f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf49f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf49f-105">X.400 メッセージ転送システム (MTS) エントリ識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bf49f-105">Contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf49f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="bf49f-106">Header file:</span></span>  <br/> |<span data-ttu-id="bf49f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf49f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="bf49f-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="bf49f-108">Related macros:</span></span>  <br/> |<span data-ttu-id="bf49f-109">[CbMTSID](cbmtsid.md)、 [CbNewMTSID](cbnewmtsid.md)</span><span class="sxs-lookup"><span data-stu-id="bf49f-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a><span data-ttu-id="bf49f-110">Members</span><span class="sxs-lookup"><span data-stu-id="bf49f-110">Members</span></span>

 <span data-ttu-id="bf49f-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="bf49f-111">**cb**</span></span>
  
> <span data-ttu-id="bf49f-112">**AbEntry**メンバーが記載されている配列内のバイト数。</span><span class="sxs-lookup"><span data-stu-id="bf49f-112">Count of bytes in the array described by the **abEntry** member.</span></span> 
    
 <span data-ttu-id="bf49f-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="bf49f-113">**abEntry**</span></span>
  
> <span data-ttu-id="bf49f-114">MTS のエントリの識別子のデータを格納するバイトの配列です。</span><span class="sxs-lookup"><span data-stu-id="bf49f-114">Byte array that contains the MTS entry identifier data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bf49f-115">注釈</span><span class="sxs-lookup"><span data-stu-id="bf49f-115">Remarks</span></span>

<span data-ttu-id="bf49f-116">**MTSID**構造体は、MAPI エントリの識別子の X.400 マッピングに対してのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="bf49f-116">The **MTSID** structure is used only for X.400 mappings of MAPI entry identifiers.</span></span> <span data-ttu-id="bf49f-117">MAPI [FLATENTRY](flatentry.md)構造体に対応します。</span><span class="sxs-lookup"><span data-stu-id="bf49f-117">It corresponds to the MAPI [FLATENTRY](flatentry.md) structure.</span></span> 
  
<span data-ttu-id="bf49f-118">MTS 識別子には、MAPI エントリの識別子またはバイナリのプロパティ値と同じ形式があります。</span><span class="sxs-lookup"><span data-stu-id="bf49f-118">An MTS identifier has the same format as a MAPI entry identifier or a binary property value.</span></span> <span data-ttu-id="bf49f-119">MTS 識別子は遅延メッセージをキャンセルするときに便利にすることはできます。</span><span class="sxs-lookup"><span data-stu-id="bf49f-119">MTS identifiers can be particularly useful for canceling deferred messages.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bf49f-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf49f-120">See also</span></span>



[<span data-ttu-id="bf49f-121">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="bf49f-121">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="bf49f-122">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="bf49f-122">FLATMTSIDLIST</span></span>](flatmtsidlist.md)


[<span data-ttu-id="bf49f-123">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="bf49f-123">MAPI Structures</span></span>](mapi-structures.md)

