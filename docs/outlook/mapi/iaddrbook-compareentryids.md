---
title: IAddrBookCompareEntryIDs
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
# <a name="iaddrbookcompareentryids"></a><span data-ttu-id="2721b-103">IAddrBook::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="2721b-103">IAddrBook::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="2721b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2721b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2721b-105">特定のアドレス帳プロバイダーに属する 2 つのエントリ識別子を比較して、同じアドレス帳オブジェクトを参照するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="2721b-105">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="2721b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2721b-106">Parameters</span></span>

 <span data-ttu-id="2721b-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="2721b-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="2721b-108">[in]  _lpEntryID1_ パラメーターが指すエントリ識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="2721b-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="2721b-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="2721b-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="2721b-110">[in]比較する最初のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2721b-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="2721b-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="2721b-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="2721b-112">[in]  _lpEntryID2_ パラメーターが指すエントリ識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="2721b-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="2721b-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="2721b-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="2721b-114">[in]比較する 2 番目のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2721b-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="2721b-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2721b-115">_ulFlags_</span></span>
  
> <span data-ttu-id="2721b-116">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="2721b-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="2721b-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="2721b-117">_lpulResult_</span></span>
  
> <span data-ttu-id="2721b-118">[out]比較の結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2721b-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="2721b-119">2 つのエントリ識別子が同じオブジェクトを参照する場合  _、lpulResult_ の内容は TRUE に設定されます。それ以外の場合、コンテンツは FALSE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="2721b-119">The contents of  _lpulResult_ are set to TRUE if the two entry identifiers refer to the same object; otherwise, the contents are set to FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2721b-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="2721b-120">Return value</span></span>

<span data-ttu-id="2721b-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="2721b-121">S_OK</span></span> 
  
> <span data-ttu-id="2721b-122">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="2721b-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="2721b-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2721b-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="2721b-124">_lpEntryID1_ または _lpEntryID2_ パラメーターで渡されたエントリ識別子の一方または両方は、アドレス帳プロバイダーによって認識されません。</span><span class="sxs-lookup"><span data-stu-id="2721b-124">One or both of the entry identifiers passed in with the  _lpEntryID1_ or  _lpEntryID2_ parameters are not recognized by any address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2721b-125">注釈</span><span class="sxs-lookup"><span data-stu-id="2721b-125">Remarks</span></span>

<span data-ttu-id="2721b-126">クライアント アプリケーションとサービス プロバイダーは **CompareEntryIDs** メソッドを呼び出して、1 つのアドレス帳プロバイダーに属する 2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="2721b-126">Client applications and service providers call the **CompareEntryIDs** method to compare two entry identifiers that belongs to a single address book provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="2721b-127">**CompareEntryIDs は** 、オブジェクトが複数の有効なエントリ識別子を持つ可能性がある場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="2721b-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="2721b-128">この状況は、たとえば、アドレス帳プロバイダーの新しいバージョンがインストールされた後に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2721b-128">This situation can occur, for example, after a new version of an address book provider is installed.</span></span> 
  
<span data-ttu-id="2721b-129">MAPI は、エントリ識別子を担当するアドレス帳プロバイダーにこの呼び出しを渡し、エントリ識別子の [MAPIUID](mapiuid.md) 構造をプロバイダーによって登録された **MAPIUID** 構造と照合して、適切なプロバイダーを決定します。</span><span class="sxs-lookup"><span data-stu-id="2721b-129">MAPI passes this call to the address book provider that is responsible for the entry identifiers, determining the appropriate provider by matching the [MAPIUID](mapiuid.md) structure in the entry identifiers with the **MAPIUID** structure registered by the provider.</span></span> 
  
<span data-ttu-id="2721b-130">2 つのエントリ識別子が同じオブジェクトを参照する場合 **、CompareEntryIDs は**  _lpulResult_ パラメーターの内容を TRUE に設定します。異なるオブジェクトを参照する場合 **、CompareEntryIDs はコンテンツ** を FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="2721b-130">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the contents of the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets the contents to FALSE.</span></span> <span data-ttu-id="2721b-131">どちらの場合も **、CompareEntryIDs は** データをS_OK。</span><span class="sxs-lookup"><span data-stu-id="2721b-131">In either case, **CompareEntryIDs** returns S_OK.</span></span> <span data-ttu-id="2721b-132">**CompareEntryIDs** がエラーを返す場合は、アドレス帳プロバイダーがエントリ識別子の **MAPIUID** 構造と一致する MAPIUID 構造を登録していない場合に発生する可能性があります。クライアントとプロバイダーは、比較の結果に基づいてアクションを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2721b-132">If **CompareEntryIDs** returns an error, which can occur if no address book provider has registered a **MAPIUID** structure that matches the one in the entry identifiers, clients and providers should not take any action based on the result of the comparison.</span></span> <span data-ttu-id="2721b-133">代わりに、実行するアクションに対して最も保守的なアプローチを取る必要があります。</span><span class="sxs-lookup"><span data-stu-id="2721b-133">They should instead take the most conservative approach to the action being performed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2721b-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="2721b-134">See also</span></span>



[<span data-ttu-id="2721b-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2721b-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

