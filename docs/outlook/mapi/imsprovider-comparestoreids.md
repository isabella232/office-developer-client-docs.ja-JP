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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9905a4e972f0e599629aac74b6fbc8bae06c93b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801049"
---
# <a name="imsprovidercomparestoreids"></a><span data-ttu-id="148b5-103">IMSProvider::CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="148b5-103">IMSProvider::CompareStoreIDs</span></span>

  
  
<span data-ttu-id="148b5-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="148b5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="148b5-105">比較 2 つのメッセージが同じストア オブジェクトを参照しているかどうかを判断するのには、ストア エントリ id です。</span><span class="sxs-lookup"><span data-stu-id="148b5-105">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="148b5-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="148b5-106">Parameters</span></span>

 <span data-ttu-id="148b5-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="148b5-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="148b5-108">[in]_._ _LpEntryID1_パラメーターで指定されたエントリの識別子のバイト単位のサイズ</span><span class="sxs-lookup"><span data-stu-id="148b5-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="148b5-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="148b5-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="148b5-110">[in]比較する最初のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="148b5-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="148b5-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="148b5-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="148b5-112">[in]_._ _LpEntryID2_パラメーターで指定されたエントリの識別子のバイト単位のサイズ</span><span class="sxs-lookup"><span data-stu-id="148b5-112">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="148b5-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="148b5-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="148b5-114">[in]比較する 2 番目のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="148b5-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="148b5-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="148b5-115">_ulFlags_</span></span>
  
> <span data-ttu-id="148b5-116">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="148b5-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="148b5-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="148b5-117">_lpulResult_</span></span>
  
> <span data-ttu-id="148b5-118">[out]比較の結果が返されましたへのポインター。</span><span class="sxs-lookup"><span data-stu-id="148b5-118">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="148b5-119">2 つのエントリの識別子が同じオブジェクトを参照する場合は TRUE。それ以外の場合、FALSE です。</span><span class="sxs-lookup"><span data-stu-id="148b5-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="148b5-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="148b5-120">Return value</span></span>

<span data-ttu-id="148b5-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="148b5-121">S_OK</span></span> 
  
> <span data-ttu-id="148b5-122">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="148b5-122">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="148b5-123">����</span><span class="sxs-lookup"><span data-stu-id="148b5-123">Remarks</span></span>

<span data-ttu-id="148b5-124">MAPI は、 [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)メソッドの呼び出しを処理するときに、 **IMSProvider::CompareStoreIDs**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="148b5-124">MAPI calls the **IMSProvider::CompareStoreIDs** method when it processes a call to the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="148b5-125">**CompareStoreIDs**は、どのプロファイルのセクションでは、存在する場合に関連付けられています開かれているメッセージ ・ ストアを決定するこの時点で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="148b5-125">**CompareStoreIDs** is called at this point to determine which profile section, if any, is associated with the message store being opened.</span></span> <span data-ttu-id="148b5-126">特定のストア プロバイダーの開いているメッセージ ・ ストアがない場合、 **CompareStoreIDs**の呼び出しを作成できます。</span><span class="sxs-lookup"><span data-stu-id="148b5-126">A **CompareStoreIDs** call can be made when no message stores are open for a particular store provider.</span></span> <span data-ttu-id="148b5-127">さらに、MAPI ではまた**CompareStoreIDs**を呼び出しして、ストア プロバイダーの[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)メソッド呼び出しを処理するとき。</span><span class="sxs-lookup"><span data-stu-id="148b5-127">In addition, MAPI also calls **CompareStoreIDs** when it processes a store provider call to the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method.</span></span> 
  
<span data-ttu-id="148b5-128">エントリ id が**CompareStoreIDs**の比較には、プロバイダーのダイナミック リンク ライブラリ (DLL) を格納し、両方のラップ解除済みストア エントリ id は、現在の両方です。</span><span class="sxs-lookup"><span data-stu-id="148b5-128">The entry identifiers compared by **CompareStoreIDs** are both for the current store provider's dynamic-link library (DLL) and are both unwrapped store entry identifiers.</span></span> <span data-ttu-id="148b5-129">ストア エントリ id の折り返しの詳細については、 [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="148b5-129">For more information about wrapping store entry identifiers, see [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span></span>
  
<span data-ttu-id="148b5-130">エントリ id を比較することは、オブジェクトが 1 つ以上の有効なエントリ id を持つことができますので便利です。</span><span class="sxs-lookup"><span data-stu-id="148b5-130">Comparing entry identifiers is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="148b5-131">これは、たとえば、メッセージ ストア プロバイダーの新しいバージョンをインストールした後に発生します。</span><span class="sxs-lookup"><span data-stu-id="148b5-131">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="148b5-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="148b5-132">See also</span></span>



[<span data-ttu-id="148b5-133">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="148b5-133">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="148b5-134">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="148b5-134">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="148b5-135">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="148b5-135">IMAPISupport::WrapStoreEntryID</span></span>](imapisupport-wrapstoreentryid.md)
  
[<span data-ttu-id="148b5-136">IMSProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="148b5-136">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

