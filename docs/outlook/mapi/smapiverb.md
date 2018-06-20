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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4d060d62deb685b4691846c2b8e48a82ae3195ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803976"
---
# <a name="smapiverb"></a><span data-ttu-id="c644a-103">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="c644a-103">SMAPIVerb</span></span>

  
  
<span data-ttu-id="c644a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c644a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c644a-105">MAPI 動詞をについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c644a-105">Describes a MAPI verb.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c644a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c644a-106">Header file:</span></span>  <br/> |<span data-ttu-id="c644a-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="c644a-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="c644a-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="c644a-108">Members</span></span>

 <span data-ttu-id="c644a-109">**lVerb**</span><span class="sxs-lookup"><span data-stu-id="c644a-109">**lVerb**</span></span>
  
> <span data-ttu-id="c644a-110">[IMAPIForm::DoVerb](imapiform-doverb.md)に渡される動詞を表すコードです。</span><span class="sxs-lookup"><span data-stu-id="c644a-110">Code representing the verb that is passed to [IMAPIForm::DoVerb](imapiform-doverb.md).</span></span> <span data-ttu-id="c644a-111">標準動詞は、Exchform.h ヘッダー ファイルで定義されます。</span><span class="sxs-lookup"><span data-stu-id="c644a-111">Standard verbs are defined in the header file Exchform.h.</span></span>
    
 <span data-ttu-id="c644a-112">**szVerbname**</span><span class="sxs-lookup"><span data-stu-id="c644a-112">**szVerbname**</span></span>
  
> <span data-ttu-id="c644a-113">フォーム] メニューに表示される動詞の名前を表示します。</span><span class="sxs-lookup"><span data-stu-id="c644a-113">Display name of the verb as it appears on the form menu.</span></span>
    
 <span data-ttu-id="c644a-114">**fuFlags**</span><span class="sxs-lookup"><span data-stu-id="c644a-114">**fuFlags**</span></span>
  
> <span data-ttu-id="c644a-115">動詞のフラグです。</span><span class="sxs-lookup"><span data-stu-id="c644a-115">Flags for the verb.</span></span>
    
 <span data-ttu-id="c644a-116">**grfAttribs**</span><span class="sxs-lookup"><span data-stu-id="c644a-116">**grfAttribs**</span></span>
  
> <span data-ttu-id="c644a-117">動詞の属性。</span><span class="sxs-lookup"><span data-stu-id="c644a-117">Attributes of the verb.</span></span> 
    
 <span data-ttu-id="c644a-118">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="c644a-118">**ulFlags**</span></span>
  
> <span data-ttu-id="c644a-119">動詞の表示名の形式を示すフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="c644a-119">Flag indicating the format of the verb's display name.</span></span> <span data-ttu-id="c644a-120">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="c644a-120">The following flag can be set:</span></span>
    
<span data-ttu-id="c644a-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c644a-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c644a-122">表示名は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="c644a-122">The display name is in Unicode format.</span></span> <span data-ttu-id="c644a-123">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の表示名です。</span><span class="sxs-lookup"><span data-stu-id="c644a-123">If the MAPI_UNICODE flag is not set, the display name is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c644a-124">備考</span><span class="sxs-lookup"><span data-stu-id="c644a-124">Remarks</span></span>

<span data-ttu-id="c644a-125">**SMAPIVerb**構造体は、次のメソッドのパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="c644a-125">The **SMAPIVerb** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="c644a-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="c644a-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="c644a-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="c644a-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="c644a-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="c644a-128">See also</span></span>



[<span data-ttu-id="c644a-129">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="c644a-129">CbMessageClassArray</span></span>](cbmessageclassarray.md)


[<span data-ttu-id="c644a-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="c644a-130">MAPI Structures</span></span>](mapi-structures.md)

