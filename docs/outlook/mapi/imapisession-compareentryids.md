---
title: imapisessioncompareentryids
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4dfde82aa843072168288f4e0b0084dfccd5cd2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338459"
---
# <a name="imapisessioncompareentryids"></a><span data-ttu-id="91b09-103">IMAPISession::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="91b09-103">IMAPISession::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="91b09-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91b09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91b09-105">2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="91b09-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="91b09-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="91b09-106">Parameters</span></span>

 <span data-ttu-id="91b09-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="91b09-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="91b09-108">順番_lpEntryID1_パラメーターによって指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="91b09-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="91b09-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="91b09-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="91b09-110">順番比較する最初のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="91b09-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="91b09-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="91b09-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="91b09-112">順番_lpEntryID2_パラメーターによって指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="91b09-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="91b09-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="91b09-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="91b09-114">順番比較する2番目のエントリ id へのポインター。</span><span class="sxs-lookup"><span data-stu-id="91b09-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="91b09-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="91b09-115">_ulFlags_</span></span>
  
> <span data-ttu-id="91b09-116">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="91b09-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="91b09-117">_lルー result_</span><span class="sxs-lookup"><span data-stu-id="91b09-117">_lpulResult_</span></span>
  
> <span data-ttu-id="91b09-118">読み上げ比較結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="91b09-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="91b09-119">2つのエントリ識別子が同じオブジェクトを参照している場合は TRUE。それ以外の場合は FALSE。</span><span class="sxs-lookup"><span data-stu-id="91b09-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="91b09-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="91b09-120">Return value</span></span>

<span data-ttu-id="91b09-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="91b09-121">S_OK</span></span> 
  
> <span data-ttu-id="91b09-122">比較に成功しました。</span><span class="sxs-lookup"><span data-stu-id="91b09-122">The comparison was successful.</span></span>
    
<span data-ttu-id="91b09-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="91b09-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="91b09-124">パラメーターとして指定されたいずれかまたは両方のエントリ識別子がオブジェクトを参照していない可能性があります。これらのオブジェクトは現在開かれていないため、使用できない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="91b09-124">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because these objects are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="91b09-125">解説</span><span class="sxs-lookup"><span data-stu-id="91b09-125">Remarks</span></span>

<span data-ttu-id="91b09-126">**imapisession:: compareentryids**メソッドは、1つのサービスプロバイダーに属する2つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="91b09-126">The **IMAPISession::CompareEntryIDs** method compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="91b09-127">MAPI は、エントリ識別子から[MAPIUID](mapiuid.md)部分を抽出して、オブジェクトを処理するサービスプロバイダーを決定し、そのログオンオブジェクトの**compareentryids**メソッドを呼び出して比較を実行します。</span><span class="sxs-lookup"><span data-stu-id="91b09-127">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects and then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="91b09-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="91b09-128">Notes to callers</span></span>

<span data-ttu-id="91b09-129">**compareentryids**メソッドは、1つのオブジェクトが複数の有効なエントリ識別子を持つことができるので便利です。</span><span class="sxs-lookup"><span data-stu-id="91b09-129">The **CompareEntryIDs** method is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="91b09-130">このような状況は、サービスプロバイダーの新しいバージョンがインストールされた後などに発生します。</span><span class="sxs-lookup"><span data-stu-id="91b09-130">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="91b09-131">**compareentryids**がエラーを返す場合は、比較の結果に基づいてアクションを実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="91b09-131">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="91b09-132">その代わりに、可能な限り最も厳しい方法を採用します。</span><span class="sxs-lookup"><span data-stu-id="91b09-132">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="91b09-133">たとえば、エントリ識別子の一方または両方に無効な**MAPIUID**が含まれている場合、 **compareentryids**は失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="91b09-133">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="91b09-134">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="91b09-134">MFCMAPI reference</span></span>

<span data-ttu-id="91b09-135">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="91b09-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="91b09-136">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="91b09-136">**File**</span></span>|<span data-ttu-id="91b09-137">**関数**</span><span class="sxs-lookup"><span data-stu-id="91b09-137">**Function**</span></span>|<span data-ttu-id="91b09-138">**コメント**</span><span class="sxs-lookup"><span data-stu-id="91b09-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="91b09-139">basedialog</span><span class="sxs-lookup"><span data-stu-id="91b09-139">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="91b09-140">cbasedialog:: oncompareentryids</span><span class="sxs-lookup"><span data-stu-id="91b09-140">CbaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="91b09-141">mfcmapi は、 **imapisession:: compareentryids**メソッドを使用して、ユーザーが入力する2つのエントリ id を比較します。</span><span class="sxs-lookup"><span data-stu-id="91b09-141">MFCMAPI uses the **IMAPISession::CompareEntryIDs** method to compare two entry IDs that a user enters.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91b09-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="91b09-142">See also</span></span>



[<span data-ttu-id="91b09-143">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="91b09-143">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="91b09-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="91b09-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="91b09-145">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="91b09-145">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

