---
title: FBadRglpNameID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpNameID
api_type:
- COM
ms.assetid: fec5d5ac-bca6-4fff-b264-45cdb6b37f55
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3f04c5be240f63d35ea8dba0f7abbf1085f2a41d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800034"
---
# <a name="fbadrglpnameid"></a><span data-ttu-id="69fe8-103">FBadRglpNameID</span><span class="sxs-lookup"><span data-stu-id="69fe8-103">FBadRglpNameID</span></span>

  
  
<span data-ttu-id="69fe8-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="69fe8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="69fe8-105">名前付きプロパティを記述する構造体の配列を検証し、その割り当てを確認します。</span><span class="sxs-lookup"><span data-stu-id="69fe8-105">Validates an array of structures that describe named properties and verifies their allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69fe8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="69fe8-106">Header file:</span></span>  <br/> |<span data-ttu-id="69fe8-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="69fe8-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="69fe8-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="69fe8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="69fe8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="69fe8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="69fe8-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="69fe8-110">Called by:</span></span>  <br/> |<span data-ttu-id="69fe8-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="69fe8-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a><span data-ttu-id="69fe8-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="69fe8-112">Parameters</span></span>

 <span data-ttu-id="69fe8-113">_lppNameId_</span><span class="sxs-lookup"><span data-stu-id="69fe8-113">_lppNameId_</span></span>
  
> <span data-ttu-id="69fe8-114">[in]名前付きプロパティを記述する[MAPINAMEID](mapinameid.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="69fe8-114">[in] Pointer to an array of [MAPINAMEID](mapinameid.md) structures describing the named properties.</span></span> 
    
 <span data-ttu-id="69fe8-115">_Cname_</span><span class="sxs-lookup"><span data-stu-id="69fe8-115">_cNames_</span></span>
  
> <span data-ttu-id="69fe8-116">[in]_LppNameId_パラメーターが指す配列内の名前付きプロパティの構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="69fe8-116">[in] Count of named property structures in the array pointed to by the  _lppNameId_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="69fe8-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="69fe8-117">Return value</span></span>

<span data-ttu-id="69fe8-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="69fe8-118">TRUE</span></span> 
  
> <span data-ttu-id="69fe8-119">1 つ以上の指定したプロパティの名前の構造体が有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="69fe8-119">One or more of the specified property name structures is invalid.</span></span> 
    
<span data-ttu-id="69fe8-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="69fe8-120">FALSE</span></span> 
  
> <span data-ttu-id="69fe8-121">指定したプロパティの名前の構造体は、すべて有効です。</span><span class="sxs-lookup"><span data-stu-id="69fe8-121">The specified property name structures are all valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="69fe8-122">注釈</span><span class="sxs-lookup"><span data-stu-id="69fe8-122">Remarks</span></span>

<span data-ttu-id="69fe8-123">[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)または[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)への呼び出しをセットアップするとき、 **FBadRglpNameID**関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="69fe8-123">The **FBadRglpNameID** function can be used when setting up for a call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> 
  

