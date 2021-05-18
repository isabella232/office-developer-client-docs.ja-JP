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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 01b42c04244d35d72dd856222b4bab543b84db45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412696"
---
# <a name="smessageclassarray"></a><span data-ttu-id="d85ea-103">SMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="d85ea-103">SMessageClassArray</span></span>

  
  
<span data-ttu-id="d85ea-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d85ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d85ea-105">メッセージ クラス文字列へのポインターの配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="d85ea-105">Contains an array of pointers to message class strings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d85ea-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d85ea-106">Header file:</span></span>  <br/> |<span data-ttu-id="d85ea-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="d85ea-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="d85ea-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="d85ea-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="d85ea-109">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="d85ea-109">CbMessageClassArray</span></span>](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a><span data-ttu-id="d85ea-110">Members</span><span class="sxs-lookup"><span data-stu-id="d85ea-110">Members</span></span>

 <span data-ttu-id="d85ea-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="d85ea-111">**cValues**</span></span>
  
> <span data-ttu-id="d85ea-112">配列内のメッセージ クラス文字列ポインターの数。</span><span class="sxs-lookup"><span data-stu-id="d85ea-112">Count of message class string pointers in the array.</span></span>
    
 <span data-ttu-id="d85ea-113">**aMessageClass**</span><span class="sxs-lookup"><span data-stu-id="d85ea-113">**aMessageClass**</span></span>
  
> <span data-ttu-id="d85ea-114">メッセージ クラス文字列へのポインターの配列。</span><span class="sxs-lookup"><span data-stu-id="d85ea-114">Array of pointers to message class strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d85ea-115">注釈</span><span class="sxs-lookup"><span data-stu-id="d85ea-115">Remarks</span></span>

<span data-ttu-id="d85ea-116">**SMessageClassArray** 構造体は、次のメソッドでパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="d85ea-116">The **SMessageClassArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="d85ea-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="d85ea-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="d85ea-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="d85ea-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="d85ea-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="d85ea-119">See also</span></span>



[<span data-ttu-id="d85ea-120">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="d85ea-120">MAPI Structures</span></span>](mapi-structures.md)

