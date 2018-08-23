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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 03256f2dec62d0228c4d5456dcd1b60f66b13ad2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800351"
---
# <a name="iablogoncompareentryids"></a><span data-ttu-id="d5f05-103">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="d5f05-103">IABLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="d5f05-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d5f05-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d5f05-105">同じオブジェクトを参照しているかどうかを決定する 2 つのエントリ id を比較します。</span><span class="sxs-lookup"><span data-stu-id="d5f05-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="d5f05-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5f05-106">Parameters</span></span>

 <span data-ttu-id="d5f05-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="d5f05-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="d5f05-108">[in]_LpEntryID1_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="d5f05-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="d5f05-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="d5f05-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="d5f05-110">[in]比較する最初のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d5f05-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="d5f05-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="d5f05-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="d5f05-112">[in]_LpEntryID2_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="d5f05-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="d5f05-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="d5f05-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="d5f05-114">[in]比較する 2 番目のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d5f05-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="d5f05-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d5f05-115">_ulFlags_</span></span>
  
> <span data-ttu-id="d5f05-116">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="d5f05-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d5f05-117">_lpulRet_</span><span class="sxs-lookup"><span data-stu-id="d5f05-117">_lpulRet_</span></span>
  
> <span data-ttu-id="d5f05-118">[out]比較の結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d5f05-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="d5f05-119">2 つのエントリの識別子が同じオブジェクトを参照している場合は TRUE。それ以外の場合、FALSE です。</span><span class="sxs-lookup"><span data-stu-id="d5f05-119">TRUE to indicate that the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d5f05-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d5f05-120">Return value</span></span>

<span data-ttu-id="d5f05-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="d5f05-121">S_OK</span></span> 
  
> <span data-ttu-id="d5f05-122">エントリ id が正常に比較されました。</span><span class="sxs-lookup"><span data-stu-id="d5f05-122">The entry identifiers were successfully compared.</span></span>
    
<span data-ttu-id="d5f05-123">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d5f05-123">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="d5f05-124">いずれかまたは両方のエントリの識別子は、アドレス帳プロバイダーに属していません。</span><span class="sxs-lookup"><span data-stu-id="d5f05-124">One or both of the entry identifiers do not belong to the address book provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d5f05-125">注釈</span><span class="sxs-lookup"><span data-stu-id="d5f05-125">Remarks</span></span>

<span data-ttu-id="d5f05-126">アドレス帳プロバイダーは、同じオブジェクトを参照しているかどうかを決定する 2 つのエントリ id を比較する**CompareEntryIDs**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="d5f05-126">Address book providers implement the **CompareEntryIDs** method to compare two entry identifiers to determine whether they refer to the same object.</span></span> 
  
 <span data-ttu-id="d5f05-127">**CompareEntryIDs**は、オブジェクトが複数のエントリの有効な識別子を持つことができますので便利です。このような状況には、たとえば、長期的なエントリの識別子を使用して、短期的なエントリ id を比較するときが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5f05-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier; such a situation can occur, for example, when you compare a short-term entry identifier with a long-term entry identifier.</span></span> 
  
<span data-ttu-id="d5f05-128">エントリの識別子を作成する方法の詳細については、 [MAPI エントリの識別子](mapi-entry-identifiers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5f05-128">For more information about how to create entry identifiers, see [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d5f05-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="d5f05-129">See also</span></span>



[<span data-ttu-id="d5f05-130">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d5f05-130">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

