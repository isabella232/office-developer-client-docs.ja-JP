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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2a2439bae79b497f018391983e2c4b03a35eee70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424253"
---
# <a name="imsgstorecompareentryids"></a><span data-ttu-id="a4799-103">IMsgStore::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="a4799-103">IMsgStore::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="a4799-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4799-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4799-105">2 つのエントリ識別子を比較して、メッセージ ストア内の同じエントリを参照するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="a4799-105">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span> <span data-ttu-id="a4799-106">MAPI は、比較する両方のエントリ識別子の一意識別子 (UID) が、そのプロバイダーによって処理される場合にのみ、この呼び出しをサービス プロバイダーに渡します。</span><span class="sxs-lookup"><span data-stu-id="a4799-106">MAPI passes this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="a4799-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a4799-107">Parameters</span></span>

 <span data-ttu-id="a4799-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="a4799-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="a4799-109">[in]  _lpEntryID1_ パラメーターが指すエントリ識別子のバイト 数  _です。_</span><span class="sxs-lookup"><span data-stu-id="a4799-109">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="a4799-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="a4799-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="a4799-111">[in]比較する最初のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a4799-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="a4799-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="a4799-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="a4799-113">[in]  _lpEntryID2_ パラメーターが指すエントリ識別子のバイト 数  _です。_</span><span class="sxs-lookup"><span data-stu-id="a4799-113">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="a4799-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="a4799-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="a4799-115">[in]比較する 2 番目のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a4799-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="a4799-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a4799-116">_ulFlags_</span></span>
  
> <span data-ttu-id="a4799-117">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="a4799-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a4799-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="a4799-118">_lpulResult_</span></span>
  
> <span data-ttu-id="a4799-119">[out]比較の結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a4799-119">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="a4799-120">2 つのエントリ識別子が同じオブジェクトを参照する場合は TRUE。それ以外の場合は FALSE。</span><span class="sxs-lookup"><span data-stu-id="a4799-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a4799-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="a4799-121">Return value</span></span>

<span data-ttu-id="a4799-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="a4799-122">S_OK</span></span> 
  
> <span data-ttu-id="a4799-123">比較は成功しました。</span><span class="sxs-lookup"><span data-stu-id="a4799-123">The comparison was successful.</span></span>
    
<span data-ttu-id="a4799-124">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a4799-124">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="a4799-125">パラメーターとして指定されたエントリ識別子の 1 つまたは両方は、対応するオブジェクトが開かないので、現在は使用できない可能性があるオブジェクトを参照しません。</span><span class="sxs-lookup"><span data-stu-id="a4799-125">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because the corresponding objects are unopened and unavailable at present.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a4799-126">注釈</span><span class="sxs-lookup"><span data-stu-id="a4799-126">Remarks</span></span>

<span data-ttu-id="a4799-127">**IMsgStore::CompareEntryIDs** メソッドは、メッセージ ストアに属する 2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="a4799-127">The **IMsgStore::CompareEntryIDs** method compares two entry identifiers that belong to the message store to determine whether they refer to the same object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a4799-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a4799-128">Notes to callers</span></span>

 <span data-ttu-id="a4799-129">**CompareEntryIDs** は、オブジェクトに複数の有効なエントリ識別子 (たとえば、メッセージ ストア プロバイダーの新しいバージョンがインストールされた後) を持つ可能性がある場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="a4799-129">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier (for example, after a new version of a message store provider is installed).</span></span> 
  
<span data-ttu-id="a4799-130">**CompareEntryIDs が** エラーを返す場合は、比較の結果に基づいてアクションを実行しない。</span><span class="sxs-lookup"><span data-stu-id="a4799-130">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="a4799-131">代わりに、可能な限り最も保守的なアプローチを取ってください。</span><span class="sxs-lookup"><span data-stu-id="a4799-131">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="a4799-132">たとえば、エントリ識別子の一方または両方に無効な MAPIUID が含まれている場合 **、CompareEntryIDs** は **失敗する可能性があります**。</span><span class="sxs-lookup"><span data-stu-id="a4799-132">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contains an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a4799-133">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="a4799-133">MFCMAPI reference</span></span>

<span data-ttu-id="a4799-134">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a4799-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a4799-135">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="a4799-135">**File**</span></span>|<span data-ttu-id="a4799-136">**関数**</span><span class="sxs-lookup"><span data-stu-id="a4799-136">**Function**</span></span>|<span data-ttu-id="a4799-137">**コメント**</span><span class="sxs-lookup"><span data-stu-id="a4799-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a4799-138">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="a4799-138">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="a4799-139">CBaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="a4799-139">CBaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="a4799-140">MFCMAPI は **、IMsgStore::CompareEntryIDs** メソッドを使用してエントリの ID を比較します。</span><span class="sxs-lookup"><span data-stu-id="a4799-140">MFCMAPI uses the **IMsgStore::CompareEntryIDs** method to compare entry IDs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4799-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="a4799-141">See also</span></span>



[<span data-ttu-id="a4799-142">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="a4799-142">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="a4799-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a4799-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="a4799-144">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="a4799-144">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

