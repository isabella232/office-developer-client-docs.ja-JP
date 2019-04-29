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
# <a name="smessageclassarray"></a><span data-ttu-id="e4208-103">SMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="e4208-103">SMessageClassArray</span></span>

  
  
<span data-ttu-id="e4208-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4208-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4208-105">メッセージクラスの文字列へのポインターの配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="e4208-105">Contains an array of pointers to message class strings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e4208-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e4208-106">Header file:</span></span>  <br/> |<span data-ttu-id="e4208-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="e4208-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="e4208-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="e4208-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="e4208-109">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="e4208-109">CbMessageClassArray</span></span>](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a><span data-ttu-id="e4208-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="e4208-110">Members</span></span>

 <span data-ttu-id="e4208-111">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="e4208-111">**cValues**</span></span>
  
> <span data-ttu-id="e4208-112">配列内のメッセージクラス文字列ポインターの数。</span><span class="sxs-lookup"><span data-stu-id="e4208-112">Count of message class string pointers in the array.</span></span>
    
 <span data-ttu-id="e4208-113">**amessageclass**</span><span class="sxs-lookup"><span data-stu-id="e4208-113">**aMessageClass**</span></span>
  
> <span data-ttu-id="e4208-114">メッセージクラスの文字列へのポインターの配列です。</span><span class="sxs-lookup"><span data-stu-id="e4208-114">Array of pointers to message class strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e4208-115">注釈</span><span class="sxs-lookup"><span data-stu-id="e4208-115">Remarks</span></span>

<span data-ttu-id="e4208-116">**SMessageClassArray**構造体は、次のメソッドのパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="e4208-116">The **SMessageClassArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="e4208-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="e4208-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="e4208-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="e4208-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="e4208-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="e4208-119">See also</span></span>



[<span data-ttu-id="e4208-120">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="e4208-120">MAPI Structures</span></span>](mapi-structures.md)

