---
title: SMessageClassArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMessageClassArray
api_type:
- COM
ms.assetid: 05f8c191-db2b-4174-8b3c-a9fdabfe6ac8
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 01563e3655d42abc62ea88a12f2878e5d81129d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803975"
---
# <a name="smessageclassarray"></a><span data-ttu-id="44b6d-103">SMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="44b6d-103">SMessageClassArray</span></span>

  
  
<span data-ttu-id="44b6d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="44b6d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="44b6d-105">メッセージ クラスの文字列へのポインターの配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="44b6d-105">Contains an array of pointers to message class strings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44b6d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="44b6d-106">Header file:</span></span>  <br/> |<span data-ttu-id="44b6d-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="44b6d-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="44b6d-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="44b6d-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="44b6d-109">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="44b6d-109">CbMessageClassArray</span></span>](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a><span data-ttu-id="44b6d-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="44b6d-110">Members</span></span>

 <span data-ttu-id="44b6d-111">**あう**</span><span class="sxs-lookup"><span data-stu-id="44b6d-111">**cValues**</span></span>
  
> <span data-ttu-id="44b6d-112">配列内のメッセージ クラスの文字列ポインターの数。</span><span class="sxs-lookup"><span data-stu-id="44b6d-112">Count of message class string pointers in the array.</span></span>
    
 <span data-ttu-id="44b6d-113">**aMessageClass**</span><span class="sxs-lookup"><span data-stu-id="44b6d-113">**aMessageClass**</span></span>
  
> <span data-ttu-id="44b6d-114">メッセージ クラスの文字列へのポインターの配列です。</span><span class="sxs-lookup"><span data-stu-id="44b6d-114">Array of pointers to message class strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="44b6d-115">備考</span><span class="sxs-lookup"><span data-stu-id="44b6d-115">Remarks</span></span>

<span data-ttu-id="44b6d-116">**SMessageClassArray**構造体は、次のメソッドのパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="44b6d-116">The **SMessageClassArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="44b6d-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="44b6d-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="44b6d-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="44b6d-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="44b6d-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="44b6d-119">See also</span></span>



[<span data-ttu-id="44b6d-120">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="44b6d-120">MAPI Structures</span></span>](mapi-structures.md)

