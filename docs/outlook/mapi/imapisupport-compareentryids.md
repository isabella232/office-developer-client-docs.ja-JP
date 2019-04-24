---
title: imapisupportcompareentryids
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6c79943792c8c17ee007c39b5c5c215a6fbc0699
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331571"
---
# <a name="imapisupportcompareentryids"></a><span data-ttu-id="3d393-103">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="3d393-103">IMAPISupport::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="3d393-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d393-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d393-105">2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="3d393-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="3d393-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3d393-106">Parameters</span></span>

 <span data-ttu-id="3d393-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="3d393-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="3d393-108">順番_lpEntryID1_パラメーターによって指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="3d393-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="3d393-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="3d393-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="3d393-110">順番比較する最初のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3d393-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="3d393-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="3d393-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="3d393-112">順番_lpEntryID2_パラメーターによって指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="3d393-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="3d393-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="3d393-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="3d393-114">順番比較する2番目のエントリ id へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3d393-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="3d393-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3d393-115">_ulFlags_</span></span>
  
> <span data-ttu-id="3d393-116">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="3d393-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="3d393-117">_lルー result_</span><span class="sxs-lookup"><span data-stu-id="3d393-117">_lpulResult_</span></span>
  
> <span data-ttu-id="3d393-118">読み上げ比較結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3d393-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="3d393-119">2つのエントリ識別子が同じオブジェクトを参照している場合は TRUE。それ以外の場合は FALSE。</span><span class="sxs-lookup"><span data-stu-id="3d393-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3d393-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="3d393-120">Return value</span></span>

<span data-ttu-id="3d393-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="3d393-121">S_OK</span></span> 
  
> <span data-ttu-id="3d393-122">比較に成功しました。</span><span class="sxs-lookup"><span data-stu-id="3d393-122">The comparison was successful.</span></span>
    
<span data-ttu-id="3d393-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="3d393-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="3d393-124">パラメーターとして指定されたいずれかまたは両方のエントリ識別子が有効なオブジェクトを参照していません。現在、使用できない状態である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3d393-124">One or both of the entry identifiers specified as parameters do not refer to valid objects, possibly because they are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3d393-125">解説</span><span class="sxs-lookup"><span data-stu-id="3d393-125">Remarks</span></span>

<span data-ttu-id="3d393-126">**imapisupport:: compareentryids**メソッドは、アドレス帳およびメッセージストアプロバイダーのサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="3d393-126">The **IMAPISupport::CompareEntryIDs** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="3d393-127">**compareentryids**は、1つのサービスプロバイダーに属する2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="3d393-127">**CompareEntryIDs** compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="3d393-128">MAPI は、エントリ識別子から[MAPIUID](mapiuid.md)部分を抽出して、オブジェクトを処理するサービスプロバイダーを決定します。</span><span class="sxs-lookup"><span data-stu-id="3d393-128">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects.</span></span> <span data-ttu-id="3d393-129">MAPI は、そのログオンオブジェクトの**compareentryids**メソッドを呼び出して、比較を実行します。</span><span class="sxs-lookup"><span data-stu-id="3d393-129">MAPI then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3d393-130">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="3d393-130">Notes to callers</span></span>

 <span data-ttu-id="3d393-131">**compareentryids**は、1つのオブジェクトが複数の有効なエントリ識別子を持つことができるので便利です。</span><span class="sxs-lookup"><span data-stu-id="3d393-131">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="3d393-132">このような状況は、サービスプロバイダーの新しいバージョンがインストールされた後などに発生します。</span><span class="sxs-lookup"><span data-stu-id="3d393-132">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="3d393-133">**compareentryids**がエラーを返す場合は、比較の結果に基づいてアクションを実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="3d393-133">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="3d393-134">その代わりに、可能な限り最も厳しい方法を採用します。</span><span class="sxs-lookup"><span data-stu-id="3d393-134">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="3d393-135">たとえば、エントリ識別子の一方または両方に無効な**MAPIUID**構造が含まれている場合、 **compareentryids**は失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3d393-135">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3d393-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d393-136">See also</span></span>



[<span data-ttu-id="3d393-137">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="3d393-137">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="3d393-138">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3d393-138">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

