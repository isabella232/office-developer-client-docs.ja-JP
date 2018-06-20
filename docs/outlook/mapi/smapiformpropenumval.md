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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: bae750e7e940bc1417b3d225c9c81129e9da77b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803954"
---
# <a name="smapiformpropenumval"></a><span data-ttu-id="7fd17-103">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="7fd17-103">SMAPIFormPropEnumVal</span></span>

  
  
<span data-ttu-id="7fd17-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7fd17-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7fd17-105">列挙された整数値をその値の表示名にマップします。</span><span class="sxs-lookup"><span data-stu-id="7fd17-105">Maps an enumerated integer value to a display name for that value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7fd17-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7fd17-106">Header file:</span></span>  <br/> |<span data-ttu-id="7fd17-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="7fd17-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a><span data-ttu-id="7fd17-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="7fd17-108">Members</span></span>

 <span data-ttu-id="7fd17-109">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="7fd17-109">**pszDisplayName**</span></span>
  
> <span data-ttu-id="7fd17-110">**NVal**のメンバーで指定された値の表示名を含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="7fd17-110">String that contains the display name for the value specified in the **nVal** member.</span></span> 
    
 <span data-ttu-id="7fd17-111">**nVal**</span><span class="sxs-lookup"><span data-stu-id="7fd17-111">**nVal**</span></span>
  
> <span data-ttu-id="7fd17-112">**PszDisplayName**メンバーで指定された表示名の列挙値。</span><span class="sxs-lookup"><span data-stu-id="7fd17-112">An enumeration value for the display name pointed to by the **pszDisplayName** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7fd17-113">備考</span><span class="sxs-lookup"><span data-stu-id="7fd17-113">Remarks</span></span>

<span data-ttu-id="7fd17-114">ユーザーは、フォームの表示名を選択すると、フォームに関連付けられている[IMAPIProp](imapipropiunknown.md)インターフェイスの実装を使用して名前の対応する列挙値が格納されます。</span><span class="sxs-lookup"><span data-stu-id="7fd17-114">When a user selects a display name from a form, the name's corresponding enumeration value is stored by using the [IMAPIProp](imapipropiunknown.md) interface implementation that is associated with the form.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7fd17-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="7fd17-115">See also</span></span>



[<span data-ttu-id="7fd17-116">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="7fd17-116">SMAPIFormProp</span></span>](smapiformprop.md)
  
[<span data-ttu-id="7fd17-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7fd17-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="7fd17-118">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="7fd17-118">MAPI Structures</span></span>](mapi-structures.md)

