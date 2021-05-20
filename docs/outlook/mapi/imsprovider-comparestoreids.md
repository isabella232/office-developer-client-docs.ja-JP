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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431709"
---
# <a name="imsprovidercomparestoreids"></a><span data-ttu-id="b9921-103">IMSProvider::CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="b9921-103">IMSProvider::CompareStoreIDs</span></span>

  
  
<span data-ttu-id="b9921-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9921-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9921-105">2 つのメッセージ ストア エントリ識別子を比較して、同じストア オブジェクトを参照するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="b9921-105">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b9921-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b9921-106">Parameters</span></span>

 <span data-ttu-id="b9921-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="b9921-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="b9921-108">[in]  _lpEntryID1_ パラメーターが指すエントリ識別子のサイズ (バイト  _単位)。_</span><span class="sxs-lookup"><span data-stu-id="b9921-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="b9921-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="b9921-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="b9921-110">[in]比較する最初のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b9921-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="b9921-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="b9921-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="b9921-112">[in]  _lpEntryID2_ パラメーターが指すエントリ識別子のサイズ (バイト  _単位)。_</span><span class="sxs-lookup"><span data-stu-id="b9921-112">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="b9921-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="b9921-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="b9921-114">[in]比較する 2 番目のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b9921-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="b9921-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b9921-115">_ulFlags_</span></span>
  
> <span data-ttu-id="b9921-116">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="b9921-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b9921-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="b9921-117">_lpulResult_</span></span>
  
> <span data-ttu-id="b9921-118">[out]比較の返される結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b9921-118">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="b9921-119">2 つのエントリ識別子が同じオブジェクトを参照する場合は TRUE。それ以外の場合は FALSE。</span><span class="sxs-lookup"><span data-stu-id="b9921-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b9921-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="b9921-120">Return value</span></span>

<span data-ttu-id="b9921-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="b9921-121">S_OK</span></span> 
  
> <span data-ttu-id="b9921-122">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="b9921-122">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b9921-123">注釈</span><span class="sxs-lookup"><span data-stu-id="b9921-123">Remarks</span></span>

<span data-ttu-id="b9921-124">MAPI は [、IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)メソッドへの呼び出しを処理するときに **、IMSProvider::CompareStoreIDs** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b9921-124">MAPI calls the **IMSProvider::CompareStoreIDs** method when it processes a call to the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="b9921-125">**この時点で CompareStoreIDs** が呼び出され、開いているメッセージ ストアに関連付けられているプロファイル セクション (ある場合) が特定されます。</span><span class="sxs-lookup"><span data-stu-id="b9921-125">**CompareStoreIDs** is called at this point to determine which profile section, if any, is associated with the message store being opened.</span></span> <span data-ttu-id="b9921-126">**CompareStoreIDs 呼** び出しは、特定のストア プロバイダーに対して開いているメッセージ ストアがない場合に行います。</span><span class="sxs-lookup"><span data-stu-id="b9921-126">A **CompareStoreIDs** call can be made when no message stores are open for a particular store provider.</span></span> <span data-ttu-id="b9921-127">さらに、MAPI は[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)メソッドへのストア プロバイダー呼び出しを処理するときに CompareStoreIDs も呼び出します。 </span><span class="sxs-lookup"><span data-stu-id="b9921-127">In addition, MAPI also calls **CompareStoreIDs** when it processes a store provider call to the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method.</span></span> 
  
<span data-ttu-id="b9921-128">**CompareStoreIDs** で比較されるエントリ識別子は、現在のストア プロバイダーのダイナミック リンク ライブラリ (DLL) の両方のエントリ識別子であり、両方ともラップされていないストア エントリ識別子です。</span><span class="sxs-lookup"><span data-stu-id="b9921-128">The entry identifiers compared by **CompareStoreIDs** are both for the current store provider's dynamic-link library (DLL) and are both unwrapped store entry identifiers.</span></span> <span data-ttu-id="b9921-129">ストア エントリ識別子の折り返しの詳細については [、「IMAPISupport::WrapStoreEntryID」を参照してください](imapisupport-wrapstoreentryid.md)。</span><span class="sxs-lookup"><span data-stu-id="b9921-129">For more information about wrapping store entry identifiers, see [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span></span>
  
<span data-ttu-id="b9921-130">エントリ識別子の比較は、オブジェクトが複数の有効なエントリ識別子を持つ可能性がある場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="b9921-130">Comparing entry identifiers is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="b9921-131">これは、たとえば、メッセージ ストア プロバイダーの新しいバージョンがインストールされた後に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b9921-131">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b9921-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="b9921-132">See also</span></span>



[<span data-ttu-id="b9921-133">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="b9921-133">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="b9921-134">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="b9921-134">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="b9921-135">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="b9921-135">IMAPISupport::WrapStoreEntryID</span></span>](imapisupport-wrapstoreentryid.md)
  
[<span data-ttu-id="b9921-136">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9921-136">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

