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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 96da91acec741322e6c07c64555171d35f0f7e00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435174"
---
# <a name="mtsid"></a><span data-ttu-id="db0fb-103">MTSID</span><span class="sxs-lookup"><span data-stu-id="db0fb-103">MTSID</span></span>

  
  
<span data-ttu-id="db0fb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db0fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db0fb-105">X.400 メッセージ トランスポート システム (MTS) エントリ識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="db0fb-105">Contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db0fb-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="db0fb-106">Header file:</span></span>  <br/> |<span data-ttu-id="db0fb-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="db0fb-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="db0fb-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="db0fb-108">Related macros:</span></span>  <br/> |<span data-ttu-id="db0fb-109">[CbMTSID](cbmtsid.md)、 [CbNewMTSID](cbnewmtsid.md)</span><span class="sxs-lookup"><span data-stu-id="db0fb-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a><span data-ttu-id="db0fb-110">Members</span><span class="sxs-lookup"><span data-stu-id="db0fb-110">Members</span></span>

 <span data-ttu-id="db0fb-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="db0fb-111">**cb**</span></span>
  
> <span data-ttu-id="db0fb-112">abEntry メンバーによって記述された配列 **内のバイト数** 。</span><span class="sxs-lookup"><span data-stu-id="db0fb-112">Count of bytes in the array described by the **abEntry** member.</span></span> 
    
 <span data-ttu-id="db0fb-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="db0fb-113">**abEntry**</span></span>
  
> <span data-ttu-id="db0fb-114">MTS エントリ識別子データを含むバイト配列。</span><span class="sxs-lookup"><span data-stu-id="db0fb-114">Byte array that contains the MTS entry identifier data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="db0fb-115">注釈</span><span class="sxs-lookup"><span data-stu-id="db0fb-115">Remarks</span></span>

<span data-ttu-id="db0fb-116">**MTSID 構造** は、MAPI エントリ識別子の X.400 マッピングにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="db0fb-116">The **MTSID** structure is used only for X.400 mappings of MAPI entry identifiers.</span></span> <span data-ttu-id="db0fb-117">MAPI [FLATENTRY 構造に対応](flatentry.md) します。</span><span class="sxs-lookup"><span data-stu-id="db0fb-117">It corresponds to the MAPI [FLATENTRY](flatentry.md) structure.</span></span> 
  
<span data-ttu-id="db0fb-118">MTS 識別子は、MAPI エントリ識別子またはバイナリ プロパティ値と同じ形式です。</span><span class="sxs-lookup"><span data-stu-id="db0fb-118">An MTS identifier has the same format as a MAPI entry identifier or a binary property value.</span></span> <span data-ttu-id="db0fb-119">MTS 識別子は、遅延メッセージをキャンセルする場合に特に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="db0fb-119">MTS identifiers can be particularly useful for canceling deferred messages.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="db0fb-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="db0fb-120">See also</span></span>



[<span data-ttu-id="db0fb-121">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="db0fb-121">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="db0fb-122">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="db0fb-122">FLATMTSIDLIST</span></span>](flatmtsidlist.md)


[<span data-ttu-id="db0fb-123">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="db0fb-123">MAPI Structures</span></span>](mapi-structures.md)

