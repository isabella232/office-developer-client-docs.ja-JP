---
title: IMAPISupportCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompareEntryIDs
api_type:
- COM
ms.assetid: be6991d9-6353-4838-bc6b-39de51a94d8d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c939189c2c8f7d3147c3146f55deac0e032ce9df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800736"
---
# <a name="imapisupportcompareentryids"></a><span data-ttu-id="982e3-103">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="982e3-103">IMAPISupport::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="982e3-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="982e3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="982e3-105">同じオブジェクトを参照しているかどうかを決定する 2 つのエントリ id を比較します。</span><span class="sxs-lookup"><span data-stu-id="982e3-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="982e3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="982e3-106">Parameters</span></span>

 <span data-ttu-id="982e3-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="982e3-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="982e3-108">[in]_LpEntryID1_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="982e3-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="982e3-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="982e3-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="982e3-110">[in]比較する最初のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="982e3-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="982e3-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="982e3-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="982e3-112">[in]_LpEntryID2_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="982e3-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="982e3-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="982e3-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="982e3-114">[in]比較する 2 番目のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="982e3-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="982e3-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="982e3-115">_ulFlags_</span></span>
  
> <span data-ttu-id="982e3-116">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="982e3-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="982e3-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="982e3-117">_lpulResult_</span></span>
  
> <span data-ttu-id="982e3-118">[out]比較の結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="982e3-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="982e3-119">2 つのエントリの識別子が同じオブジェクトを参照する場合は TRUE。それ以外の場合、FALSE です。</span><span class="sxs-lookup"><span data-stu-id="982e3-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="982e3-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="982e3-120">Return value</span></span>

<span data-ttu-id="982e3-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="982e3-121">S_OK</span></span> 
  
> <span data-ttu-id="982e3-122">比較は正常に終了しました。</span><span class="sxs-lookup"><span data-stu-id="982e3-122">The comparison was successful.</span></span>
    
<span data-ttu-id="982e3-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="982e3-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="982e3-124">いずれかまたは両方のパラメーターとして指定されているエントリの識別子を参照しない有効なオブジェクトは、可能性がありますが現在開かれていないと使用できないためです。</span><span class="sxs-lookup"><span data-stu-id="982e3-124">One or both of the entry identifiers specified as parameters do not refer to valid objects, possibly because they are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="982e3-125">注釈</span><span class="sxs-lookup"><span data-stu-id="982e3-125">Remarks</span></span>

<span data-ttu-id="982e3-126">アドレス帳、メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::CompareEntryIDs**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="982e3-126">The **IMAPISupport::CompareEntryIDs** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="982e3-127">**CompareEntryIDs**は、同じオブジェクトを参照しているかどうかを決定する 1 つのサービス プロバイダーに属している 2 つのエントリ id を比較します。</span><span class="sxs-lookup"><span data-stu-id="982e3-127">**CompareEntryIDs** compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="982e3-128">MAPI では、オブジェクトを担当するサービス ・ プロバイダーを決定するエントリの識別子から[MAPIUID](mapiuid.md)の部分を抽出します。</span><span class="sxs-lookup"><span data-stu-id="982e3-128">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects.</span></span> <span data-ttu-id="982e3-129">MAPI は、比較を実行するよう、ログオン オブジェクトの**CompareEntryIDs**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="982e3-129">MAPI then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="982e3-130">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="982e3-130">Notes to callers</span></span>

 <span data-ttu-id="982e3-131">**CompareEntryIDs**は、オブジェクトが 1 つ以上の有効なエントリ id を持つことができますので便利です。</span><span class="sxs-lookup"><span data-stu-id="982e3-131">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="982e3-132">このような状況には、たとえば、サービス ・ プロバイダーの新しいバージョンをインストールした後が発生します。</span><span class="sxs-lookup"><span data-stu-id="982e3-132">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="982e3-133">**CompareEntryIDs**がエラーを返した場合は、比較の結果に基づいてアクションになりません。</span><span class="sxs-lookup"><span data-stu-id="982e3-133">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="982e3-134">代わりにかかる可能性のある最も保守的なアプローチをします。</span><span class="sxs-lookup"><span data-stu-id="982e3-134">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="982e3-135">**CompareEntryIDs**は、エントリの識別子のいずれかで無効な**MAPIUID**構造が含まれているなどの場合に失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="982e3-135">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="982e3-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="982e3-136">See also</span></span>



[<span data-ttu-id="982e3-137">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="982e3-137">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="982e3-138">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="982e3-138">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

