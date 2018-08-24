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
ms.openlocfilehash: 2c49a17389a9bfc998f892e0becf96dca4cd773f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578718"
---
# <a name="smapiformpropenumval"></a><span data-ttu-id="449e5-103">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="449e5-103">SMAPIFormPropEnumVal</span></span>

  
  
<span data-ttu-id="449e5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="449e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="449e5-105">列挙された整数値をその値の表示名にマップします。</span><span class="sxs-lookup"><span data-stu-id="449e5-105">Maps an enumerated integer value to a display name for that value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="449e5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="449e5-106">Header file:</span></span>  <br/> |<span data-ttu-id="449e5-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="449e5-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a><span data-ttu-id="449e5-108">Members</span><span class="sxs-lookup"><span data-stu-id="449e5-108">Members</span></span>

 <span data-ttu-id="449e5-109">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="449e5-109">**pszDisplayName**</span></span>
  
> <span data-ttu-id="449e5-110">**NVal**のメンバーで指定された値の表示名を含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="449e5-110">String that contains the display name for the value specified in the **nVal** member.</span></span> 
    
 <span data-ttu-id="449e5-111">**nVal**</span><span class="sxs-lookup"><span data-stu-id="449e5-111">**nVal**</span></span>
  
> <span data-ttu-id="449e5-112">**PszDisplayName**メンバーで指定された表示名の列挙値。</span><span class="sxs-lookup"><span data-stu-id="449e5-112">An enumeration value for the display name pointed to by the **pszDisplayName** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="449e5-113">注釈</span><span class="sxs-lookup"><span data-stu-id="449e5-113">Remarks</span></span>

<span data-ttu-id="449e5-114">ユーザーは、フォームの表示名を選択すると、フォームに関連付けられている[IMAPIProp](imapipropiunknown.md)インターフェイスの実装を使用して名前の対応する列挙値が格納されます。</span><span class="sxs-lookup"><span data-stu-id="449e5-114">When a user selects a display name from a form, the name's corresponding enumeration value is stored by using the [IMAPIProp](imapipropiunknown.md) interface implementation that is associated with the form.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="449e5-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="449e5-115">See also</span></span>



[<span data-ttu-id="449e5-116">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="449e5-116">SMAPIFormProp</span></span>](smapiformprop.md)
  
[<span data-ttu-id="449e5-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="449e5-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="449e5-118">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="449e5-118">MAPI Structures</span></span>](mapi-structures.md)

