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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ef284a2c036abb9eac10ecf33de4adbf61f3c54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309486"
---
# <a name="smapiverb"></a><span data-ttu-id="97a83-103">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="97a83-103">SMAPIVerb</span></span>

  
  
<span data-ttu-id="97a83-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97a83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97a83-105">MAPI の動詞を記述します。</span><span class="sxs-lookup"><span data-stu-id="97a83-105">Describes a MAPI verb.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="97a83-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="97a83-106">Header file:</span></span>  <br/> |<span data-ttu-id="97a83-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="97a83-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="97a83-108">Members</span><span class="sxs-lookup"><span data-stu-id="97a83-108">Members</span></span>

 <span data-ttu-id="97a83-109">**lverb**</span><span class="sxs-lookup"><span data-stu-id="97a83-109">**lVerb**</span></span>
  
> <span data-ttu-id="97a83-110">imapiform に渡される動詞を表すコード[::D overb](imapiform-doverb.md)</span><span class="sxs-lookup"><span data-stu-id="97a83-110">Code representing the verb that is passed to [IMAPIForm::DoVerb](imapiform-doverb.md).</span></span> <span data-ttu-id="97a83-111">標準動詞は、ヘッダーファイルの exchform .h で定義されています。</span><span class="sxs-lookup"><span data-stu-id="97a83-111">Standard verbs are defined in the header file Exchform.h.</span></span>
    
 <span data-ttu-id="97a83-112">**szVerbname**</span><span class="sxs-lookup"><span data-stu-id="97a83-112">**szVerbname**</span></span>
  
> <span data-ttu-id="97a83-113">フォームメニューに表示される動詞の表示名。</span><span class="sxs-lookup"><span data-stu-id="97a83-113">Display name of the verb as it appears on the form menu.</span></span>
    
 <span data-ttu-id="97a83-114">**futex フラグ**</span><span class="sxs-lookup"><span data-stu-id="97a83-114">**fuFlags**</span></span>
  
> <span data-ttu-id="97a83-115">動詞のフラグです。</span><span class="sxs-lookup"><span data-stu-id="97a83-115">Flags for the verb.</span></span>
    
 <span data-ttu-id="97a83-116">**grfAttribs**</span><span class="sxs-lookup"><span data-stu-id="97a83-116">**grfAttribs**</span></span>
  
> <span data-ttu-id="97a83-117">動詞の属性。</span><span class="sxs-lookup"><span data-stu-id="97a83-117">Attributes of the verb.</span></span> 
    
 <span data-ttu-id="97a83-118">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="97a83-118">**ulFlags**</span></span>
  
> <span data-ttu-id="97a83-119">動詞の表示名の形式を示すフラグです。</span><span class="sxs-lookup"><span data-stu-id="97a83-119">Flag indicating the format of the verb's display name.</span></span> <span data-ttu-id="97a83-120">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="97a83-120">The following flag can be set:</span></span>
    
<span data-ttu-id="97a83-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="97a83-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="97a83-122">表示名は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="97a83-122">The display name is in Unicode format.</span></span> <span data-ttu-id="97a83-123">MAPI_UNICODE フラグが設定されていない場合、表示名は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="97a83-123">If the MAPI_UNICODE flag is not set, the display name is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="97a83-124">解説</span><span class="sxs-lookup"><span data-stu-id="97a83-124">Remarks</span></span>

<span data-ttu-id="97a83-125">**smapiverb**構造体は、次のメソッドのパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="97a83-125">The **SMAPIVerb** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="97a83-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="97a83-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="97a83-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="97a83-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="97a83-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="97a83-128">See also</span></span>



[<span data-ttu-id="97a83-129">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="97a83-129">CbMessageClassArray</span></span>](cbmessageclassarray.md)


[<span data-ttu-id="97a83-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="97a83-130">MAPI Structures</span></span>](mapi-structures.md)

