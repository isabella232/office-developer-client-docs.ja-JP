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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: df6347298aab5404ec69bd9ac876863e31b741d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800698"
---
# <a name="imapisessioncompareentryids"></a><span data-ttu-id="e2cb3-103">IMAPISession::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="e2cb3-103">IMAPISession::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="e2cb3-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e2cb3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e2cb3-105">同じオブジェクトを参照しているかどうかを決定する 2 つのエントリ id を比較します。</span><span class="sxs-lookup"><span data-stu-id="e2cb3-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="e2cb3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e2cb3-106">Parameters</span></span>

 <span data-ttu-id="e2cb3-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="e2cb3-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="e2cb3-108">[in]_LpEntryID1_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="e2cb3-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="e2cb3-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="e2cb3-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="e2cb3-110">[in]比較する最初のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e2cb3-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="e2cb3-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="e2cb3-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="e2cb3-112">[in]_LpEntryID2_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="e2cb3-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="e2cb3-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="e2cb3-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="e2cb3-114">[in]比較する 2 番目のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e2cb3-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="e2cb3-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e2cb3-115">_ulFlags_</span></span>
  
> <span data-ttu-id="e2cb3-116">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="e2cb3-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="e2cb3-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="e2cb3-117">_lpulResult_</span></span>
  
> <span data-ttu-id="e2cb3-118">[out]比較の結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e2cb3-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="e2cb3-119">2 つのエントリの識別子が同じオブジェクトを参照する場合は TRUE。それ以外の場合、FALSE です。</span><span class="sxs-lookup"><span data-stu-id="e2cb3-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e2cb3-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e2cb3-120">Return value</span></span>

<span data-ttu-id="e2cb3-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2cb3-121">S_OK</span></span> 
  
> <span data-ttu-id="e2cb3-122">比較は正常に終了しました。</span><span class="sxs-lookup"><span data-stu-id="e2cb3-122">The comparison was successful.</span></span>
    
<span data-ttu-id="e2cb3-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e2cb3-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="e2cb3-124">いずれかまたは両方のパラメーターとして指定されているエントリの識別子を参照しないオブジェクト、可能性のあるこれらのオブジェクトは、現在開かれていないと使用できないためです。</span><span class="sxs-lookup"><span data-stu-id="e2cb3-124">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because these objects are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2cb3-125">注釈</span><span class="sxs-lookup"><span data-stu-id="e2cb3-125">Remarks</span></span>

<span data-ttu-id="e2cb3-126">**IMAPISession::CompareEntryIDs**メソッドは、同じオブジェクトを参照しているかどうかを決定する 1 つのサービス プロバイダーに属している 2 つのエントリ id を比較します。</span><span class="sxs-lookup"><span data-stu-id="e2cb3-126">The **IMAPISession::CompareEntryIDs** method compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="e2cb3-127">MAPI は、オブジェクトを担当するサービス ・ プロバイダーを決定するエントリの識別子から[MAPIUID](mapiuid.md)の部分を抽出し、比較を実行するのには、そのログオン オブジェクトの**CompareEntryIDs**メソッドを呼び出して、します。</span><span class="sxs-lookup"><span data-stu-id="e2cb3-127">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects and then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e2cb3-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e2cb3-128">Notes to callers</span></span>

<span data-ttu-id="e2cb3-129">**CompareEntryIDs**メソッドは、オブジェクトが 1 つ以上の有効なエントリ id を持つことができますので便利です。</span><span class="sxs-lookup"><span data-stu-id="e2cb3-129">The **CompareEntryIDs** method is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="e2cb3-130">このような状況には、たとえば、サービス ・ プロバイダーの新しいバージョンをインストールした後が発生します。</span><span class="sxs-lookup"><span data-stu-id="e2cb3-130">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="e2cb3-131">**CompareEntryIDs**がエラーを返した場合は、比較の結果に基づいてアクションになりません。</span><span class="sxs-lookup"><span data-stu-id="e2cb3-131">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="e2cb3-132">代わりにかかる可能性のある最も保守的なアプローチをします。</span><span class="sxs-lookup"><span data-stu-id="e2cb3-132">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="e2cb3-133">**CompareEntryIDs**は、一方または両方のエントリの識別子で、無効な**MAPIUID**が含まれているなどの場合に失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e2cb3-133">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e2cb3-134">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="e2cb3-134">MFCMAPI reference</span></span>

<span data-ttu-id="e2cb3-135">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="e2cb3-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e2cb3-136">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="e2cb3-136">**File**</span></span>|<span data-ttu-id="e2cb3-137">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="e2cb3-137">**Function**</span></span>|<span data-ttu-id="e2cb3-138">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="e2cb3-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e2cb3-139">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="e2cb3-139">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="e2cb3-140">CbaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="e2cb3-140">CbaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="e2cb3-141">MFCMAPI では、 **IMAPISession::CompareEntryIDs**メソッドを使用して、ユーザーが入力した 2 つのエントリ Id を比較します。</span><span class="sxs-lookup"><span data-stu-id="e2cb3-141">MFCMAPI uses the **IMAPISession::CompareEntryIDs** method to compare two entry IDs that a user enters.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2cb3-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2cb3-142">See also</span></span>



[<span data-ttu-id="e2cb3-143">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="e2cb3-143">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="e2cb3-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2cb3-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="e2cb3-145">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="e2cb3-145">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

