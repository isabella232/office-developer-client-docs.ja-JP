---
title: iaddrbookcompareentryids
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBookCompareEntryIDs
api_type:
- COM
ms.assetid: 7dabc1d3-5ea4-482f-91a9-9ef3009eddd2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b6abecc298df7a86afff9338752a15615c73b3a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424260"
---
# <a name="iaddrbookcompareentryids"></a><span data-ttu-id="81876-103">IAddrBook::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="81876-103">IAddrBook::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="81876-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81876-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81876-105">特定のアドレス帳プロバイダーに属する2つのエントリ識別子を比較して、同じアドレス帳オブジェクトを参照しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="81876-105">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span> 
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="81876-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="81876-106">Parameters</span></span>

 <span data-ttu-id="81876-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="81876-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="81876-108">順番_lpEntryID1_パラメーターによって指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="81876-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="81876-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="81876-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="81876-110">順番比較する最初のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="81876-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="81876-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="81876-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="81876-112">順番_lpEntryID2_パラメーターによって指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="81876-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="81876-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="81876-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="81876-114">順番比較する2番目のエントリ id へのポインター。</span><span class="sxs-lookup"><span data-stu-id="81876-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="81876-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="81876-115">_ulFlags_</span></span>
  
> <span data-ttu-id="81876-116">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="81876-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="81876-117">_lルー result_</span><span class="sxs-lookup"><span data-stu-id="81876-117">_lpulResult_</span></span>
  
> <span data-ttu-id="81876-118">読み上げ比較結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="81876-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="81876-119">2つのエントリ識別子が同じオブジェクトを参照する場合、 _lアウト result_の内容は TRUE に設定されます。それ以外の場合は、内容が FALSE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="81876-119">The contents of  _lpulResult_ are set to TRUE if the two entry identifiers refer to the same object; otherwise, the contents are set to FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="81876-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="81876-120">Return value</span></span>

<span data-ttu-id="81876-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="81876-121">S_OK</span></span> 
  
> <span data-ttu-id="81876-122">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="81876-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="81876-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="81876-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="81876-124">_lpEntryID1_パラメーターまたは_lpEntryID2_パラメーターと共に渡されたエントリ識別子の一方または両方が、アドレス帳プロバイダーによって認識されません。</span><span class="sxs-lookup"><span data-stu-id="81876-124">One or both of the entry identifiers passed in with the  _lpEntryID1_ or  _lpEntryID2_ parameters are not recognized by any address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="81876-125">注釈</span><span class="sxs-lookup"><span data-stu-id="81876-125">Remarks</span></span>

<span data-ttu-id="81876-126">クライアントアプリケーションおよびサービスプロバイダーは、1つのアドレス帳プロバイダーに属する2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断するために、 **compareentryids**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="81876-126">Client applications and service providers call the **CompareEntryIDs** method to compare two entry identifiers that belongs to a single address book provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="81876-127">**compareentryids**は、1つのオブジェクトが複数の有効なエントリ識別子を持つことができるので便利です。</span><span class="sxs-lookup"><span data-stu-id="81876-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="81876-128">このような状況は、アドレス帳プロバイダーの新しいバージョンがインストールされた後などに発生します。</span><span class="sxs-lookup"><span data-stu-id="81876-128">This situation can occur, for example, after a new version of an address book provider is installed.</span></span> 
  
<span data-ttu-id="81876-129">この呼び出しは、エントリ識別子を処理するアドレス帳プロバイダーに渡され、エントリ識別子の[MAPIUID](mapiuid.md)構造と、 **MAPIUID**構造が一致することによって適切なプロバイダーが決定されます。供給.</span><span class="sxs-lookup"><span data-stu-id="81876-129">MAPI passes this call to the address book provider that is responsible for the entry identifiers, determining the appropriate provider by matching the [MAPIUID](mapiuid.md) structure in the entry identifiers with the **MAPIUID** structure registered by the provider.</span></span> 
  
<span data-ttu-id="81876-130">2つのエントリ識別子が同じオブジェクトを参照している場合、 **compareentryids**は_lpulresult_パラメーターの内容を TRUE に設定します。異なるオブジェクトを参照している場合、 **compareentryids**は内容を FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="81876-130">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the contents of the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets the contents to FALSE.</span></span> <span data-ttu-id="81876-131">どちらの場合も、 **compareentryids**は S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="81876-131">In either case, **CompareEntryIDs** returns S_OK.</span></span> <span data-ttu-id="81876-132">**compareentryids**がエラーを返した場合は、アドレス帳プロバイダーが登録されていない**MAPIUID**構造がエントリ識別子内にある場合、クライアントとプロバイダーは、その結果に基づいて操作を行うことはできません。結果.</span><span class="sxs-lookup"><span data-stu-id="81876-132">If **CompareEntryIDs** returns an error, which can occur if no address book provider has registered a **MAPIUID** structure that matches the one in the entry identifiers, clients and providers should not take any action based on the result of the comparison.</span></span> <span data-ttu-id="81876-133">そのような場合は、実行するアクションに対して最も慎重な方法をとる必要があります。</span><span class="sxs-lookup"><span data-stu-id="81876-133">They should instead take the most conservative approach to the action being performed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="81876-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="81876-134">See also</span></span>



[<span data-ttu-id="81876-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="81876-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

