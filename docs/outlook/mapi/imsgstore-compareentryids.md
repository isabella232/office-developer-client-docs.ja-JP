---
title: IMsgStoreCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.CompareEntryIDs
api_type:
- COM
ms.assetid: 33d70748-0d3f-4be4-bcb5-7ec048887944
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a1c5cdc67bc64f20dd8ba0a5e8682c5e2f97294f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800997"
---
# <a name="imsgstorecompareentryids"></a><span data-ttu-id="077a9-103">IMsgStore::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="077a9-103">IMsgStore::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="077a9-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="077a9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="077a9-105">メッセージ ストアの同じエントリを参照しているかどうかを決定する 2 つのエントリ id を比較します。</span><span class="sxs-lookup"><span data-stu-id="077a9-105">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span> <span data-ttu-id="077a9-106">MAPI は、両方のエントリの識別子を比較するには、一意の識別子 (Uid) がそのプロバイダーによって処理される場合にのみ、サービス ・ プロバイダーへの呼び出しを渡します。</span><span class="sxs-lookup"><span data-stu-id="077a9-106">MAPI passes this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="077a9-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="077a9-107">Parameters</span></span>

 <span data-ttu-id="077a9-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="077a9-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="077a9-109">[in]_._ _LpEntryID1_パラメーターで指定されたエントリの識別子のバイト数</span><span class="sxs-lookup"><span data-stu-id="077a9-109">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="077a9-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="077a9-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="077a9-111">[in]比較する最初のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="077a9-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="077a9-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="077a9-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="077a9-113">[in]_._ _LpEntryID2_パラメーターで指定されたエントリの識別子のバイト数</span><span class="sxs-lookup"><span data-stu-id="077a9-113">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="077a9-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="077a9-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="077a9-115">[in]比較する 2 番目のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="077a9-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="077a9-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="077a9-116">_ulFlags_</span></span>
  
> <span data-ttu-id="077a9-117">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="077a9-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="077a9-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="077a9-118">_lpulResult_</span></span>
  
> <span data-ttu-id="077a9-119">[out]比較の結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="077a9-119">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="077a9-120">2 つのエントリの識別子が同じオブジェクトを参照する場合は TRUE。それ以外の場合、FALSE です。</span><span class="sxs-lookup"><span data-stu-id="077a9-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="077a9-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="077a9-121">Return value</span></span>

<span data-ttu-id="077a9-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="077a9-122">S_OK</span></span> 
  
> <span data-ttu-id="077a9-123">比較は正常に終了しました。</span><span class="sxs-lookup"><span data-stu-id="077a9-123">The comparison was successful.</span></span>
    
<span data-ttu-id="077a9-124">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="077a9-124">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="077a9-125">一方または両方のパラメーターを参照しないオブジェクトでは、場合によって対応するオブジェクトが開かれていないとには利用できませんので、指定されたエントリの識別子が表示されます。</span><span class="sxs-lookup"><span data-stu-id="077a9-125">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because the corresponding objects are unopened and unavailable at present.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="077a9-126">備考</span><span class="sxs-lookup"><span data-stu-id="077a9-126">Remarks</span></span>

<span data-ttu-id="077a9-127">**IMsgStore::CompareEntryIDs**メソッドは、同じオブジェクトを参照しているかどうかを確認するメッセージ ・ ストアに属する 2 つのエントリ id を比較します。</span><span class="sxs-lookup"><span data-stu-id="077a9-127">The **IMsgStore::CompareEntryIDs** method compares two entry identifiers that belong to the message store to determine whether they refer to the same object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="077a9-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="077a9-128">Notes to callers</span></span>

 <span data-ttu-id="077a9-129">**CompareEntryIDs**は、オブジェクト (たとえば、メッセージ ストア プロバイダーの新しいバージョンをインストールした後) の 2 つ以上の有効なエントリ id を持つことができますので便利です。</span><span class="sxs-lookup"><span data-stu-id="077a9-129">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier (for example, after a new version of a message store provider is installed).</span></span> 
  
<span data-ttu-id="077a9-130">**CompareEntryIDs**がエラーを返した場合は、比較の結果に基づいてアクションになりません。</span><span class="sxs-lookup"><span data-stu-id="077a9-130">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="077a9-131">代わりにかかる可能性のある最も保守的なアプローチをします。</span><span class="sxs-lookup"><span data-stu-id="077a9-131">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="077a9-132">**CompareEntryIDs**は、一方または両方のエントリの識別子で、無効な**MAPIUID**が含まれているなどの場合に失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="077a9-132">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contains an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="077a9-133">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="077a9-133">MFCMAPI reference</span></span>

<span data-ttu-id="077a9-134">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="077a9-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="077a9-135">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="077a9-135">**File**</span></span>|<span data-ttu-id="077a9-136">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="077a9-136">**Function**</span></span>|<span data-ttu-id="077a9-137">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="077a9-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="077a9-138">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="077a9-138">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="077a9-139">CBaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="077a9-139">CBaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="077a9-140">MFCMAPI では、 **IMsgStore::CompareEntryIDs**メソッドを使用して、エントリ Id を比較します。</span><span class="sxs-lookup"><span data-stu-id="077a9-140">MFCMAPI uses the **IMsgStore::CompareEntryIDs** method to compare entry IDs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="077a9-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="077a9-141">See also</span></span>



[<span data-ttu-id="077a9-142">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="077a9-142">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="077a9-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="077a9-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="077a9-144">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="077a9-144">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

