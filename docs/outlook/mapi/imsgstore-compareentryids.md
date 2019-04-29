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
# <a name="imsgstorecompareentryids"></a><span data-ttu-id="1422e-103">IMsgStore::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="1422e-103">IMsgStore::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="1422e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1422e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1422e-105">2つのエントリ識別子を比較して、メッセージストア内の同じエントリを参照しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="1422e-105">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span> <span data-ttu-id="1422e-106">MAPI は、両方のエントリ識別子の一意識別子 (uid) がそのプロバイダーによって処理される場合にのみ、この呼び出しをサービスプロバイダーに渡します。</span><span class="sxs-lookup"><span data-stu-id="1422e-106">MAPI passes this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="1422e-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1422e-107">Parameters</span></span>

 <span data-ttu-id="1422e-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="1422e-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="1422e-109">順番_lpEntryID1_パラメーターによって指定されたエントリ識別子のバイト数 _。_</span><span class="sxs-lookup"><span data-stu-id="1422e-109">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="1422e-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="1422e-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="1422e-111">順番比較する最初のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1422e-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="1422e-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="1422e-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="1422e-113">順番_lpEntryID2_パラメーターによって指定されたエントリ識別子のバイト数 _。_</span><span class="sxs-lookup"><span data-stu-id="1422e-113">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="1422e-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="1422e-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="1422e-115">順番比較する2番目のエントリ id へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1422e-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="1422e-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1422e-116">_ulFlags_</span></span>
  
> <span data-ttu-id="1422e-117">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="1422e-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1422e-118">_lルー result_</span><span class="sxs-lookup"><span data-stu-id="1422e-118">_lpulResult_</span></span>
  
> <span data-ttu-id="1422e-119">読み上げ比較結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1422e-119">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="1422e-120">2つのエントリ識別子が同じオブジェクトを参照している場合は TRUE。それ以外の場合は FALSE。</span><span class="sxs-lookup"><span data-stu-id="1422e-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1422e-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="1422e-121">Return value</span></span>

<span data-ttu-id="1422e-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="1422e-122">S_OK</span></span> 
  
> <span data-ttu-id="1422e-123">比較に成功しました。</span><span class="sxs-lookup"><span data-stu-id="1422e-123">The comparison was successful.</span></span>
    
<span data-ttu-id="1422e-124">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1422e-124">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="1422e-125">パラメーターとして指定されたいずれかまたは両方のエントリ識別子がオブジェクトを参照していない可能性があります。対応するオブジェクトは未開封であり、現在は使用できないためです。</span><span class="sxs-lookup"><span data-stu-id="1422e-125">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because the corresponding objects are unopened and unavailable at present.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1422e-126">注釈</span><span class="sxs-lookup"><span data-stu-id="1422e-126">Remarks</span></span>

<span data-ttu-id="1422e-127">**IMsgStore:: compareentryids**メソッドは、メッセージストアに属する2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="1422e-127">The **IMsgStore::CompareEntryIDs** method compares two entry identifiers that belong to the message store to determine whether they refer to the same object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1422e-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="1422e-128">Notes to callers</span></span>

 <span data-ttu-id="1422e-129">**compareentryids**は、1つのオブジェクトが複数の有効なエントリ識別子を持つことができるので便利です (たとえば、新しいバージョンのメッセージストアプロバイダーがインストールされた後)。</span><span class="sxs-lookup"><span data-stu-id="1422e-129">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier (for example, after a new version of a message store provider is installed).</span></span> 
  
<span data-ttu-id="1422e-130">**compareentryids**がエラーを返す場合は、比較の結果に基づいてアクションを実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="1422e-130">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="1422e-131">その代わりに、可能な限り最も厳しい方法を採用します。</span><span class="sxs-lookup"><span data-stu-id="1422e-131">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="1422e-132">たとえば、エントリ識別子の一方または両方に無効な**MAPIUID**が含まれている場合、 **compareentryids**は失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1422e-132">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contains an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1422e-133">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="1422e-133">MFCMAPI reference</span></span>

<span data-ttu-id="1422e-134">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1422e-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1422e-135">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="1422e-135">**File**</span></span>|<span data-ttu-id="1422e-136">**関数**</span><span class="sxs-lookup"><span data-stu-id="1422e-136">**Function**</span></span>|<span data-ttu-id="1422e-137">**コメント**</span><span class="sxs-lookup"><span data-stu-id="1422e-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1422e-138">basedialog</span><span class="sxs-lookup"><span data-stu-id="1422e-138">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="1422e-139">cbasedialog:: oncompareentryids</span><span class="sxs-lookup"><span data-stu-id="1422e-139">CBaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="1422e-140">mfcmapi は、 **IMsgStore:: compareentryids**メソッドを使用してエントリ id を比較します。</span><span class="sxs-lookup"><span data-stu-id="1422e-140">MFCMAPI uses the **IMsgStore::CompareEntryIDs** method to compare entry IDs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1422e-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="1422e-141">See also</span></span>



[<span data-ttu-id="1422e-142">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="1422e-142">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="1422e-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1422e-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="1422e-144">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="1422e-144">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

