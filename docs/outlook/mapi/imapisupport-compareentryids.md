---
title: IMAPISupportCompareEntryIDs
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431044"
---
# <a name="imapisupportcompareentryids"></a><span data-ttu-id="b4e41-103">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="b4e41-103">IMAPISupport::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="b4e41-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4e41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4e41-105">2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="b4e41-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="b4e41-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b4e41-106">Parameters</span></span>

 <span data-ttu-id="b4e41-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="b4e41-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="b4e41-108">[in]  _lpEntryID1_ パラメーターが指すエントリ識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="b4e41-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="b4e41-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="b4e41-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="b4e41-110">[in]比較する最初のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b4e41-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="b4e41-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="b4e41-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="b4e41-112">[in]  _lpEntryID2_ パラメーターが指すエントリ識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="b4e41-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="b4e41-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="b4e41-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="b4e41-114">[in]比較する 2 番目のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b4e41-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="b4e41-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b4e41-115">_ulFlags_</span></span>
  
> <span data-ttu-id="b4e41-116">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="b4e41-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b4e41-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="b4e41-117">_lpulResult_</span></span>
  
> <span data-ttu-id="b4e41-118">[out]比較の結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b4e41-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="b4e41-119">2 つのエントリ識別子が同じオブジェクトを参照する場合は TRUE。それ以外の場合は FALSE。</span><span class="sxs-lookup"><span data-stu-id="b4e41-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b4e41-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="b4e41-120">Return value</span></span>

<span data-ttu-id="b4e41-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="b4e41-121">S_OK</span></span> 
  
> <span data-ttu-id="b4e41-122">比較は成功しました。</span><span class="sxs-lookup"><span data-stu-id="b4e41-122">The comparison was successful.</span></span>
    
<span data-ttu-id="b4e41-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b4e41-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="b4e41-124">パラメーターとして指定されたエントリ識別子の 1 つまたは両方は、有効なオブジェクトを参照しません。これは、現在開かないので、使用できない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b4e41-124">One or both of the entry identifiers specified as parameters do not refer to valid objects, possibly because they are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b4e41-125">注釈</span><span class="sxs-lookup"><span data-stu-id="b4e41-125">Remarks</span></span>

<span data-ttu-id="b4e41-126">**IMAPISupport::CompareEntryIDs** メソッドは、アドレス帳およびメッセージ ストア プロバイダーのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="b4e41-126">The **IMAPISupport::CompareEntryIDs** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="b4e41-127">**CompareEntryIDs は** 、1 つのサービス プロバイダーに属する 2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="b4e41-127">**CompareEntryIDs** compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="b4e41-128">MAPI は [、MAPIUID](mapiuid.md) 部分をエントリ識別子から抽出して、オブジェクトを担当するサービス プロバイダーを決定します。</span><span class="sxs-lookup"><span data-stu-id="b4e41-128">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects.</span></span> <span data-ttu-id="b4e41-129">MAPI は、そのログオン オブジェクトの **CompareEntryIDs** メソッドを呼び出して比較を実行します。</span><span class="sxs-lookup"><span data-stu-id="b4e41-129">MAPI then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b4e41-130">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="b4e41-130">Notes to callers</span></span>

 <span data-ttu-id="b4e41-131">**CompareEntryIDs は** 、オブジェクトが複数の有効なエントリ識別子を持つ可能性がある場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="b4e41-131">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="b4e41-132">この状況は、たとえば、サービス プロバイダーの新しいバージョンがインストールされた後に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b4e41-132">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="b4e41-133">**CompareEntryIDs が** エラーを返す場合は、比較の結果に基づいてアクションを実行しない。</span><span class="sxs-lookup"><span data-stu-id="b4e41-133">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="b4e41-134">代わりに、可能な限り最も保守的なアプローチを取ってください。</span><span class="sxs-lookup"><span data-stu-id="b4e41-134">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="b4e41-135">たとえば、エントリ識別子の一方または両方に無効な MAPIUID 構造が含まれている場合 **、CompareEntryIDs** は **失敗する可能性** があります。</span><span class="sxs-lookup"><span data-stu-id="b4e41-135">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b4e41-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="b4e41-136">See also</span></span>



[<span data-ttu-id="b4e41-137">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="b4e41-137">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="b4e41-138">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b4e41-138">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

