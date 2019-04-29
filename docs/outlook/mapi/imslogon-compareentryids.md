---
title: IMSLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: 481812d6-8e94-4510-b288-55501dd5757c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4196ed8b949ecb9e23c4bd34380db9cc5a369e23
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410134"
---
# <a name="imslogoncompareentryids"></a><span data-ttu-id="0568e-103">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="0568e-103">IMSLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="0568e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0568e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0568e-105">2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="0568e-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> <span data-ttu-id="0568e-106">MAPI では、両方のエントリ識別子の一意識別子 (uid) がそのプロバイダによって処理される場合にのみ、サービスプロバイダへの呼び出しを参照します。</span><span class="sxs-lookup"><span data-stu-id="0568e-106">MAPI refers this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="0568e-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0568e-107">Parameters</span></span>

 <span data-ttu-id="0568e-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="0568e-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="0568e-109">順番_lpEntryID1_パラメーターによって示されるエントリ識別子のバイト単位のサイズ _。_</span><span class="sxs-lookup"><span data-stu-id="0568e-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="0568e-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="0568e-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="0568e-111">順番比較する最初のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0568e-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="0568e-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="0568e-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="0568e-113">順番_lpEntryID2_パラメーターによって示されるエントリ識別子のバイト単位のサイズ _。_</span><span class="sxs-lookup"><span data-stu-id="0568e-113">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="0568e-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="0568e-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="0568e-115">順番比較する2番目のエントリ id へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0568e-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="0568e-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0568e-116">_ulFlags_</span></span>
  
> <span data-ttu-id="0568e-117">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="0568e-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="0568e-118">_lルー result_</span><span class="sxs-lookup"><span data-stu-id="0568e-118">_lpulResult_</span></span>
  
> <span data-ttu-id="0568e-119">読み上げ返された比較結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0568e-119">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="0568e-120">2つのエントリ識別子が同じオブジェクトを参照している場合は TRUE。それ以外の場合は FALSE。</span><span class="sxs-lookup"><span data-stu-id="0568e-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0568e-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="0568e-121">Return value</span></span>

<span data-ttu-id="0568e-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="0568e-122">S_OK</span></span> 
  
> <span data-ttu-id="0568e-123">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="0568e-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0568e-124">注釈</span><span class="sxs-lookup"><span data-stu-id="0568e-124">Remarks</span></span>

<span data-ttu-id="0568e-125">メッセージストアプロバイダーは、 **IMSLogon:: compareentryids**メソッドを実装して、メッセージストア内の指定されたエントリの2つのエントリ識別子を比較し、それらが同じオブジェクトを参照しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="0568e-125">Message store providers implement the **IMSLogon::CompareEntryIDs** method to compare two entry identifiers for a given entry in a message store to determine whether they refer to the same object.</span></span> <span data-ttu-id="0568e-126">2つのエントリ識別子が同じオブジェクトを参照している場合、 **compareentryids**は_lpulresult_パラメーターを TRUE に設定します。別のオブジェクトを参照している場合、 **compareentryids**は_lpulresult_を FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="0568e-126">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets  _lpulResult_ to FALSE.</span></span> 
  
 <span data-ttu-id="0568e-127">**compareentryids**は、1つのオブジェクトが複数の有効なエントリ識別子を持つことができるので便利です。</span><span class="sxs-lookup"><span data-stu-id="0568e-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="0568e-128">これは、たとえば、新しいバージョンのメッセージストアプロバイダーがインストールされた後に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0568e-128">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0568e-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="0568e-129">See also</span></span>



[<span data-ttu-id="0568e-130">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0568e-130">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

