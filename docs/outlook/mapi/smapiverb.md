---
title: SMAPIVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerb
api_type:
- COM
ms.assetid: 45066528-2447-4178-aaa3-7513ed0b3ba4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ef284a2c036abb9eac10ecf33de4adbf61f3c54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410960"
---
# <a name="smapiverb"></a><span data-ttu-id="20c0e-103">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="20c0e-103">SMAPIVerb</span></span>

  
  
<span data-ttu-id="20c0e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20c0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20c0e-105">MAPI 動詞について説明します。</span><span class="sxs-lookup"><span data-stu-id="20c0e-105">Describes a MAPI verb.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="20c0e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="20c0e-106">Header file:</span></span>  <br/> |<span data-ttu-id="20c0e-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="20c0e-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG lVerb;
  LPSTR szVerbname;
  DWORD fuFlags;
  DWORD grfAttribs;
  ULONG ulFlags; /* Either 0 or MAPI_UNICODE */
} SMAPIVerb, FAR * LPMAPIVERB;

```

## <a name="members"></a><span data-ttu-id="20c0e-108">Members</span><span class="sxs-lookup"><span data-stu-id="20c0e-108">Members</span></span>

 <span data-ttu-id="20c0e-109">**lVerb**</span><span class="sxs-lookup"><span data-stu-id="20c0e-109">**lVerb**</span></span>
  
> <span data-ttu-id="20c0e-110">[IMAPIForm::D oVerb](imapiform-doverb.md)に渡される動詞を表すコードです。</span><span class="sxs-lookup"><span data-stu-id="20c0e-110">Code representing the verb that is passed to [IMAPIForm::DoVerb](imapiform-doverb.md).</span></span> <span data-ttu-id="20c0e-111">標準動詞は、ヘッダー ファイル Exchform.h で定義されます。</span><span class="sxs-lookup"><span data-stu-id="20c0e-111">Standard verbs are defined in the header file Exchform.h.</span></span>
    
 <span data-ttu-id="20c0e-112">**szVerbname**</span><span class="sxs-lookup"><span data-stu-id="20c0e-112">**szVerbname**</span></span>
  
> <span data-ttu-id="20c0e-113">フォーム メニューに表示される動詞の名前を表示します。</span><span class="sxs-lookup"><span data-stu-id="20c0e-113">Display name of the verb as it appears on the form menu.</span></span>
    
 <span data-ttu-id="20c0e-114">**fuFlags**</span><span class="sxs-lookup"><span data-stu-id="20c0e-114">**fuFlags**</span></span>
  
> <span data-ttu-id="20c0e-115">動詞のフラグ。</span><span class="sxs-lookup"><span data-stu-id="20c0e-115">Flags for the verb.</span></span>
    
 <span data-ttu-id="20c0e-116">**grfAttribs**</span><span class="sxs-lookup"><span data-stu-id="20c0e-116">**grfAttribs**</span></span>
  
> <span data-ttu-id="20c0e-117">動詞の属性。</span><span class="sxs-lookup"><span data-stu-id="20c0e-117">Attributes of the verb.</span></span> 
    
 <span data-ttu-id="20c0e-118">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="20c0e-118">**ulFlags**</span></span>
  
> <span data-ttu-id="20c0e-119">動詞の表示名の形式を示すフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="20c0e-119">Flag indicating the format of the verb's display name.</span></span> <span data-ttu-id="20c0e-120">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="20c0e-120">The following flag can be set:</span></span>
    
<span data-ttu-id="20c0e-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="20c0e-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="20c0e-122">表示名は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="20c0e-122">The display name is in Unicode format.</span></span> <span data-ttu-id="20c0e-123">このフラグMAPI_UNICODE設定されていない場合、表示名は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="20c0e-123">If the MAPI_UNICODE flag is not set, the display name is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="20c0e-124">注釈</span><span class="sxs-lookup"><span data-stu-id="20c0e-124">Remarks</span></span>

<span data-ttu-id="20c0e-125">**SMAPIVerb 構造体** は、次のメソッドでパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="20c0e-125">The **SMAPIVerb** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="20c0e-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="20c0e-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="20c0e-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="20c0e-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="20c0e-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="20c0e-128">See also</span></span>



[<span data-ttu-id="20c0e-129">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="20c0e-129">CbMessageClassArray</span></span>](cbmessageclassarray.md)


[<span data-ttu-id="20c0e-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="20c0e-130">MAPI Structures</span></span>](mapi-structures.md)

