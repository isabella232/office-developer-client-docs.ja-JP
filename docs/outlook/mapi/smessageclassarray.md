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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 01b42c04244d35d72dd856222b4bab543b84db45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339663"
---
# <a name="smessageclassarray"></a><span data-ttu-id="37eee-103">SMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="37eee-103">SMessageClassArray</span></span>

  
  
<span data-ttu-id="37eee-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37eee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37eee-105">メッセージクラスの文字列へのポインターの配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="37eee-105">Contains an array of pointers to message class strings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="37eee-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="37eee-106">Header file:</span></span>  <br/> |<span data-ttu-id="37eee-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="37eee-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="37eee-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="37eee-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="37eee-109">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="37eee-109">CbMessageClassArray</span></span>](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a><span data-ttu-id="37eee-110">Members</span><span class="sxs-lookup"><span data-stu-id="37eee-110">Members</span></span>

 <span data-ttu-id="37eee-111">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="37eee-111">**cValues**</span></span>
  
> <span data-ttu-id="37eee-112">配列内のメッセージクラス文字列ポインターの数。</span><span class="sxs-lookup"><span data-stu-id="37eee-112">Count of message class string pointers in the array.</span></span>
    
 <span data-ttu-id="37eee-113">**amessageclass**</span><span class="sxs-lookup"><span data-stu-id="37eee-113">**aMessageClass**</span></span>
  
> <span data-ttu-id="37eee-114">メッセージクラスの文字列へのポインターの配列です。</span><span class="sxs-lookup"><span data-stu-id="37eee-114">Array of pointers to message class strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="37eee-115">解説</span><span class="sxs-lookup"><span data-stu-id="37eee-115">Remarks</span></span>

<span data-ttu-id="37eee-116">**SMessageClassArray**構造体は、次のメソッドのパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="37eee-116">The **SMessageClassArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="37eee-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="37eee-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="37eee-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="37eee-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="37eee-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="37eee-119">See also</span></span>



[<span data-ttu-id="37eee-120">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="37eee-120">MAPI Structures</span></span>](mapi-structures.md)

