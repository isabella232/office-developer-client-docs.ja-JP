---
title: IABLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: cb4a38ff-2fdd-40ac-a613-12c3f11a1df9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 48ddb5a7c4e013c03138b08d9dadcdc0991faeec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438373"
---
# <a name="iablogoncompareentryids"></a><span data-ttu-id="39643-103">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="39643-103">IABLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="39643-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39643-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39643-105">2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="39643-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span>
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulRet
);
```

## <a name="parameters"></a><span data-ttu-id="39643-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="39643-106">Parameters</span></span>

 <span data-ttu-id="39643-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="39643-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="39643-108">[in]  _lpEntryID1_ パラメーターが指すエントリ識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="39643-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="39643-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="39643-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="39643-110">[in]比較する最初のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="39643-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="39643-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="39643-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="39643-112">[in]  _lpEntryID2_ パラメーターが指すエントリ識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="39643-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="39643-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="39643-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="39643-114">[in]比較する 2 番目のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="39643-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="39643-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="39643-115">_ulFlags_</span></span>
  
> <span data-ttu-id="39643-116">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="39643-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="39643-117">_lpulRet_</span><span class="sxs-lookup"><span data-stu-id="39643-117">_lpulRet_</span></span>
  
> <span data-ttu-id="39643-118">[out]比較の結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="39643-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="39643-119">TRUE を指定すると、2 つのエントリ識別子が同じオブジェクトを参照します。それ以外の場合は FALSE。</span><span class="sxs-lookup"><span data-stu-id="39643-119">TRUE to indicate that the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="39643-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="39643-120">Return value</span></span>

<span data-ttu-id="39643-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="39643-121">S_OK</span></span> 
  
> <span data-ttu-id="39643-122">エントリ識別子が正常に比較されました。</span><span class="sxs-lookup"><span data-stu-id="39643-122">The entry identifiers were successfully compared.</span></span>
    
<span data-ttu-id="39643-123">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="39643-123">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="39643-124">エントリ識別子の一方または両方がアドレス帳プロバイダーに属していない。</span><span class="sxs-lookup"><span data-stu-id="39643-124">One or both of the entry identifiers do not belong to the address book provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="39643-125">注釈</span><span class="sxs-lookup"><span data-stu-id="39643-125">Remarks</span></span>

<span data-ttu-id="39643-126">アドレス帳プロバイダーは **CompareEntryIDs** メソッドを実装して、2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="39643-126">Address book providers implement the **CompareEntryIDs** method to compare two entry identifiers to determine whether they refer to the same object.</span></span> 
  
 <span data-ttu-id="39643-127">**CompareEntryIDs は** 、オブジェクトが複数の有効なエントリ識別子を持つ可能性がある場合に便利です。このような状況は、たとえば、短期エントリ識別子と長期エントリ識別子を比較するときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="39643-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier; such a situation can occur, for example, when you compare a short-term entry identifier with a long-term entry identifier.</span></span> 
  
<span data-ttu-id="39643-128">エントリ識別子を作成する方法の詳細については、「MAPI エントリ識別子 [」を参照してください](mapi-entry-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="39643-128">For more information about how to create entry identifiers, see [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="39643-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="39643-129">See also</span></span>



[<span data-ttu-id="39643-130">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="39643-130">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

