---
title: IMSProviderCompareStoreIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.CompareStoreIDs
api_type:
- COM
ms.assetid: c3e3cfaa-9c4a-482a-9411-9c4ab01d312f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 734e53c1e897c902c72319aa6f2d3d7af2d23fb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317270"
---
# <a name="imsprovidercomparestoreids"></a><span data-ttu-id="3078b-103">IMSProvider::CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="3078b-103">IMSProvider::CompareStoreIDs</span></span>

  
  
<span data-ttu-id="3078b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3078b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3078b-105">2つのメッセージストアエントリ識別子を比較して、同じ store オブジェクトを参照しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="3078b-105">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>
  
```cpp
HRESULT CompareStoreIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="3078b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3078b-106">Parameters</span></span>

 <span data-ttu-id="3078b-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="3078b-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="3078b-108">順番_lpEntryID1_パラメーターによって示されるエントリ識別子のバイト単位のサイズ _。_</span><span class="sxs-lookup"><span data-stu-id="3078b-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="3078b-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="3078b-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="3078b-110">順番比較する最初のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3078b-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="3078b-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="3078b-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="3078b-112">順番_lpEntryID2_パラメーターによって示されるエントリ識別子のバイト単位のサイズ _。_</span><span class="sxs-lookup"><span data-stu-id="3078b-112">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="3078b-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="3078b-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="3078b-114">順番比較する2番目のエントリ id へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3078b-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="3078b-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3078b-115">_ulFlags_</span></span>
  
> <span data-ttu-id="3078b-116">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="3078b-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="3078b-117">_lルー result_</span><span class="sxs-lookup"><span data-stu-id="3078b-117">_lpulResult_</span></span>
  
> <span data-ttu-id="3078b-118">読み上げ返された比較結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3078b-118">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="3078b-119">2つのエントリ識別子が同じオブジェクトを参照している場合は TRUE。それ以外の場合は FALSE。</span><span class="sxs-lookup"><span data-stu-id="3078b-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3078b-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="3078b-120">Return value</span></span>

<span data-ttu-id="3078b-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="3078b-121">S_OK</span></span> 
  
> <span data-ttu-id="3078b-122">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="3078b-122">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3078b-123">解説</span><span class="sxs-lookup"><span data-stu-id="3078b-123">Remarks</span></span>

<span data-ttu-id="3078b-124">MAPI は、 [imapisession:: openmsgstore](imapisession-openmsgstore.md)メソッドへの呼び出しを処理するときに、 **IMSProvider:: comparestoreids**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3078b-124">MAPI calls the **IMSProvider::CompareStoreIDs** method when it processes a call to the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="3078b-125">**comparestoreids**はこの時点で呼び出され、開いているメッセージストアに関連付けられているプロファイルセクションがある場合は、それを判断します。</span><span class="sxs-lookup"><span data-stu-id="3078b-125">**CompareStoreIDs** is called at this point to determine which profile section, if any, is associated with the message store being opened.</span></span> <span data-ttu-id="3078b-126">**comparestoreids**呼び出しは、特定のストアプロバイダーに対してメッセージストアが開かれていない場合に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="3078b-126">A **CompareStoreIDs** call can be made when no message stores are open for a particular store provider.</span></span> <span data-ttu-id="3078b-127">さらに、MAPI は、 [imapisupport::](imapisupport-openprofilesection.md) openprofileupdatemethod へのストアプロバイダー呼び出しを処理するときに、 **comparestoreids**も呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3078b-127">In addition, MAPI also calls **CompareStoreIDs** when it processes a store provider call to the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method.</span></span> 
  
<span data-ttu-id="3078b-128">**comparestoreids**によって比較されるエントリ識別子は、現在のストアプロバイダーのダイナミックリンクライブラリ (DLL) と共に、かつ非ラップストアエントリ識別子の両方になります。</span><span class="sxs-lookup"><span data-stu-id="3078b-128">The entry identifiers compared by **CompareStoreIDs** are both for the current store provider's dynamic-link library (DLL) and are both unwrapped store entry identifiers.</span></span> <span data-ttu-id="3078b-129">ストアエントリ識別子のラッピングの詳細については、「 [imapisupport:: WrapStoreEntryID](imapisupport-wrapstoreentryid.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3078b-129">For more information about wrapping store entry identifiers, see [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span></span>
  
<span data-ttu-id="3078b-130">エントリ識別子の比較は、1つのオブジェクトが複数の有効なエントリ識別子を持つことができるので便利です。</span><span class="sxs-lookup"><span data-stu-id="3078b-130">Comparing entry identifiers is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="3078b-131">これは、たとえば、新しいバージョンのメッセージストアプロバイダーがインストールされた後に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3078b-131">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3078b-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="3078b-132">See also</span></span>



[<span data-ttu-id="3078b-133">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="3078b-133">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="3078b-134">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="3078b-134">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="3078b-135">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="3078b-135">IMAPISupport::WrapStoreEntryID</span></span>](imapisupport-wrapstoreentryid.md)
  
[<span data-ttu-id="3078b-136">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3078b-136">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

