---
title: IMAPISessionCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.CompareEntryIDs
api_type:
- COM
ms.assetid: 319f10e9-db8d-4d16-aa1f-6cf5fef493eb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4dfde82aa843072168288f4e0b0084dfccd5cd2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427816"
---
# <a name="imapisessioncompareentryids"></a><span data-ttu-id="aa366-103">IMAPISession::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="aa366-103">IMAPISession::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="aa366-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa366-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa366-105">2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="aa366-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="aa366-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="aa366-106">Parameters</span></span>

 <span data-ttu-id="aa366-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="aa366-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="aa366-108">[in]  _lpEntryID1_ パラメーターが指すエントリ識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="aa366-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="aa366-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="aa366-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="aa366-110">[in]比較する最初のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="aa366-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="aa366-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="aa366-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="aa366-112">[in]  _lpEntryID2_ パラメーターが指すエントリ識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="aa366-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="aa366-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="aa366-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="aa366-114">[in]比較する 2 番目のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="aa366-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="aa366-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aa366-115">_ulFlags_</span></span>
  
> <span data-ttu-id="aa366-116">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="aa366-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="aa366-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="aa366-117">_lpulResult_</span></span>
  
> <span data-ttu-id="aa366-118">[out]比較の結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="aa366-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="aa366-119">2 つのエントリ識別子が同じオブジェクトを参照する場合は TRUE。それ以外の場合は FALSE。</span><span class="sxs-lookup"><span data-stu-id="aa366-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aa366-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="aa366-120">Return value</span></span>

<span data-ttu-id="aa366-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa366-121">S_OK</span></span> 
  
> <span data-ttu-id="aa366-122">比較は成功しました。</span><span class="sxs-lookup"><span data-stu-id="aa366-122">The comparison was successful.</span></span>
    
<span data-ttu-id="aa366-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="aa366-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="aa366-124">パラメーターとして指定されたエントリ識別子の 1 つまたは両方は、オブジェクトを参照しません。これらのオブジェクトは現在開かないので、使用できません。</span><span class="sxs-lookup"><span data-stu-id="aa366-124">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because these objects are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aa366-125">注釈</span><span class="sxs-lookup"><span data-stu-id="aa366-125">Remarks</span></span>

<span data-ttu-id="aa366-126">**IMAPISession::CompareEntryIDs** メソッドは、単一のサービス プロバイダーに属する 2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="aa366-126">The **IMAPISession::CompareEntryIDs** method compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="aa366-127">MAPI は [、MAPIUID](mapiuid.md) 部分をエントリ識別子から抽出して、オブジェクトを担当するサービス プロバイダーを特定し、そのログオン オブジェクトの **CompareEntryIDs** メソッドを呼び出して比較を実行します。</span><span class="sxs-lookup"><span data-stu-id="aa366-127">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects and then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="aa366-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="aa366-128">Notes to callers</span></span>

<span data-ttu-id="aa366-129">**CompareEntryIDs** メソッドは、オブジェクトが複数の有効なエントリ識別子を持つ可能性がある場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="aa366-129">The **CompareEntryIDs** method is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="aa366-130">この状況は、たとえば、サービス プロバイダーの新しいバージョンがインストールされた後に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="aa366-130">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="aa366-131">**CompareEntryIDs が** エラーを返す場合は、比較の結果に基づいてアクションを実行しない。</span><span class="sxs-lookup"><span data-stu-id="aa366-131">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="aa366-132">代わりに、可能な限り最も保守的なアプローチを取ってください。</span><span class="sxs-lookup"><span data-stu-id="aa366-132">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="aa366-133">たとえば、エントリ識別子の一方または両方に無効な MAPIUID が含まれている場合 **、CompareEntryIDs** が **失敗する可能性があります**。</span><span class="sxs-lookup"><span data-stu-id="aa366-133">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="aa366-134">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="aa366-134">MFCMAPI reference</span></span>

<span data-ttu-id="aa366-135">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa366-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="aa366-136">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="aa366-136">**File**</span></span>|<span data-ttu-id="aa366-137">**関数**</span><span class="sxs-lookup"><span data-stu-id="aa366-137">**Function**</span></span>|<span data-ttu-id="aa366-138">**コメント**</span><span class="sxs-lookup"><span data-stu-id="aa366-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aa366-139">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="aa366-139">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="aa366-140">CbaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="aa366-140">CbaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="aa366-141">MFCMAPI は **IMAPISession::CompareEntryIDs** メソッドを使用して、ユーザーが入力した 2 つのエントリ ID を比較します。</span><span class="sxs-lookup"><span data-stu-id="aa366-141">MFCMAPI uses the **IMAPISession::CompareEntryIDs** method to compare two entry IDs that a user enters.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa366-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="aa366-142">See also</span></span>



[<span data-ttu-id="aa366-143">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="aa366-143">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="aa366-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="aa366-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="aa366-145">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="aa366-145">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

