---
title: SMAPIFormPropEnumVal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropEnumVal
api_type:
- COM
ms.assetid: 694d40e9-cff2-435e-ad90-446044c306d2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 353bc574ca5987d71faf4841744de30a3d6c3f19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309493"
---
# <a name="smapiformpropenumval"></a><span data-ttu-id="5efc2-103">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="5efc2-103">SMAPIFormPropEnumVal</span></span>

  
  
<span data-ttu-id="5efc2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5efc2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5efc2-105">列挙された整数値をその値の表示名にマップします。</span><span class="sxs-lookup"><span data-stu-id="5efc2-105">Maps an enumerated integer value to a display name for that value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5efc2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5efc2-106">Header file:</span></span>  <br/> |<span data-ttu-id="5efc2-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="5efc2-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a><span data-ttu-id="5efc2-108">Members</span><span class="sxs-lookup"><span data-stu-id="5efc2-108">Members</span></span>

 <span data-ttu-id="5efc2-109">**pszdisplayname**</span><span class="sxs-lookup"><span data-stu-id="5efc2-109">**pszDisplayName**</span></span>
  
> <span data-ttu-id="5efc2-110">**nval**メンバーで指定された値の表示名を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="5efc2-110">String that contains the display name for the value specified in the **nVal** member.</span></span> 
    
 <span data-ttu-id="5efc2-111">**nval**</span><span class="sxs-lookup"><span data-stu-id="5efc2-111">**nVal**</span></span>
  
> <span data-ttu-id="5efc2-112">**pszdisplayname**メンバーによって示される表示名の列挙値。</span><span class="sxs-lookup"><span data-stu-id="5efc2-112">An enumeration value for the display name pointed to by the **pszDisplayName** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5efc2-113">解説</span><span class="sxs-lookup"><span data-stu-id="5efc2-113">Remarks</span></span>

<span data-ttu-id="5efc2-114">ユーザーがフォームから表示名を選択すると、その名前の対応する列挙値は、フォームに関連付けられている[imapiprop](imapipropiunknown.md)インターフェイスの実装を使用して格納されます。</span><span class="sxs-lookup"><span data-stu-id="5efc2-114">When a user selects a display name from a form, the name's corresponding enumeration value is stored by using the [IMAPIProp](imapipropiunknown.md) interface implementation that is associated with the form.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5efc2-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="5efc2-115">See also</span></span>



[<span data-ttu-id="5efc2-116">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="5efc2-116">SMAPIFormProp</span></span>](smapiformprop.md)
  
[<span data-ttu-id="5efc2-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="5efc2-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="5efc2-118">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="5efc2-118">MAPI Structures</span></span>](mapi-structures.md)

