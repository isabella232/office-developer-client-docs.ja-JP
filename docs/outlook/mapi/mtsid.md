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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e42bbf23ea8cf4e6196017a962329366e168420d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801665"
---
# <a name="mtsid"></a><span data-ttu-id="ecd16-103">MTSID</span><span class="sxs-lookup"><span data-stu-id="ecd16-103">MTSID</span></span>

  
  
<span data-ttu-id="ecd16-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ecd16-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ecd16-105">X.400 メッセージ転送システム (MTS) エントリ識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ecd16-105">Contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ecd16-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ecd16-106">Header file:</span></span>  <br/> |<span data-ttu-id="ecd16-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ecd16-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ecd16-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="ecd16-108">Related macros:</span></span>  <br/> |<span data-ttu-id="ecd16-109">[CbMTSID](cbmtsid.md)、 [CbNewMTSID](cbnewmtsid.md)</span><span class="sxs-lookup"><span data-stu-id="ecd16-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a><span data-ttu-id="ecd16-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="ecd16-110">Members</span></span>

 <span data-ttu-id="ecd16-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="ecd16-111">**cb**</span></span>
  
> <span data-ttu-id="ecd16-112">**AbEntry**メンバーが記載されている配列内のバイト数。</span><span class="sxs-lookup"><span data-stu-id="ecd16-112">Count of bytes in the array described by the **abEntry** member.</span></span> 
    
 <span data-ttu-id="ecd16-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="ecd16-113">**abEntry**</span></span>
  
> <span data-ttu-id="ecd16-114">MTS のエントリの識別子のデータを格納するバイトの配列です。</span><span class="sxs-lookup"><span data-stu-id="ecd16-114">Byte array that contains the MTS entry identifier data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ecd16-115">備考</span><span class="sxs-lookup"><span data-stu-id="ecd16-115">Remarks</span></span>

<span data-ttu-id="ecd16-116">**MTSID**構造体は、MAPI エントリの識別子の X.400 マッピングに対してのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="ecd16-116">The **MTSID** structure is used only for X.400 mappings of MAPI entry identifiers.</span></span> <span data-ttu-id="ecd16-117">MAPI [FLATENTRY](flatentry.md)構造体に対応します。</span><span class="sxs-lookup"><span data-stu-id="ecd16-117">It corresponds to the MAPI [FLATENTRY](flatentry.md) structure.</span></span> 
  
<span data-ttu-id="ecd16-118">MTS 識別子には、MAPI エントリの識別子またはバイナリのプロパティ値と同じ形式があります。</span><span class="sxs-lookup"><span data-stu-id="ecd16-118">An MTS identifier has the same format as a MAPI entry identifier or a binary property value.</span></span> <span data-ttu-id="ecd16-119">MTS 識別子は遅延メッセージをキャンセルするときに便利にすることはできます。</span><span class="sxs-lookup"><span data-stu-id="ecd16-119">MTS identifiers can be particularly useful for canceling deferred messages.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ecd16-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="ecd16-120">See also</span></span>



[<span data-ttu-id="ecd16-121">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="ecd16-121">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="ecd16-122">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="ecd16-122">FLATMTSIDLIST</span></span>](flatmtsidlist.md)


[<span data-ttu-id="ecd16-123">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="ecd16-123">MAPI Structures</span></span>](mapi-structures.md)

