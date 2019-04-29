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
# <a name="iablogoncompareentryids"></a><span data-ttu-id="50302-103">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="50302-103">IABLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="50302-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50302-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50302-105">2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="50302-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="50302-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50302-106">Parameters</span></span>

 <span data-ttu-id="50302-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="50302-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="50302-108">順番_lpEntryID1_パラメーターによって指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="50302-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="50302-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="50302-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="50302-110">順番比較する最初のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="50302-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="50302-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="50302-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="50302-112">順番_lpEntryID2_パラメーターによって指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="50302-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="50302-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="50302-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="50302-114">順番比較する2番目のエントリ id へのポインター。</span><span class="sxs-lookup"><span data-stu-id="50302-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="50302-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="50302-115">_ulFlags_</span></span>
  
> <span data-ttu-id="50302-116">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="50302-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="50302-117">_lアウト ret_</span><span class="sxs-lookup"><span data-stu-id="50302-117">_lpulRet_</span></span>
  
> <span data-ttu-id="50302-118">読み上げ比較結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="50302-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="50302-119">2つのエントリ識別子が同じオブジェクトを参照していることを示す場合は TRUE。それ以外の場合は FALSE。</span><span class="sxs-lookup"><span data-stu-id="50302-119">TRUE to indicate that the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="50302-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="50302-120">Return value</span></span>

<span data-ttu-id="50302-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="50302-121">S_OK</span></span> 
  
> <span data-ttu-id="50302-122">エントリ識別子が正常に比較されました。</span><span class="sxs-lookup"><span data-stu-id="50302-122">The entry identifiers were successfully compared.</span></span>
    
<span data-ttu-id="50302-123">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="50302-123">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="50302-124">一方または両方のエントリ識別子は、アドレス帳プロバイダーに属していません。</span><span class="sxs-lookup"><span data-stu-id="50302-124">One or both of the entry identifiers do not belong to the address book provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="50302-125">注釈</span><span class="sxs-lookup"><span data-stu-id="50302-125">Remarks</span></span>

<span data-ttu-id="50302-126">アドレス帳プロバイダーは、2つのエントリ識別子を比較して同じオブジェクトを参照するかどうかを判断するために、 **compareentryids**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="50302-126">Address book providers implement the **CompareEntryIDs** method to compare two entry identifiers to determine whether they refer to the same object.</span></span> 
  
 <span data-ttu-id="50302-127">**compareentryids**は、1つのオブジェクトが複数の有効なエントリ識別子を持つことができるので便利です。このような状況は、短い用語のエントリ id を長期のエントリ識別子と比較する場合などに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="50302-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier; such a situation can occur, for example, when you compare a short-term entry identifier with a long-term entry identifier.</span></span> 
  
<span data-ttu-id="50302-128">エントリ識別子を作成する方法の詳細については、「 [MAPI エントリ識別子](mapi-entry-identifiers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50302-128">For more information about how to create entry identifiers, see [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="50302-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="50302-129">See also</span></span>



[<span data-ttu-id="50302-130">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="50302-130">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

