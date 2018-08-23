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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c2e6600af66f3dab8ff0fbb5442a1354687a3cbb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801038"
---
# <a name="imslogoncompareentryids"></a><span data-ttu-id="fc49c-103">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="fc49c-103">IMSLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="fc49c-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fc49c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fc49c-105">同じオブジェクトを参照しているかどうかを決定する 2 つのエントリ id を比較します。</span><span class="sxs-lookup"><span data-stu-id="fc49c-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> <span data-ttu-id="fc49c-106">MAPI は、両方のエントリの識別子を比較するには、一意の識別子 (Uid) がそのプロバイダーによって処理される場合にのみ、サービス ・ プロバイダーへの呼び出しを意味します。</span><span class="sxs-lookup"><span data-stu-id="fc49c-106">MAPI refers this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="fc49c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fc49c-107">Parameters</span></span>

 <span data-ttu-id="fc49c-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="fc49c-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="fc49c-109">[in]_._ _LpEntryID1_パラメーターで指定されたエントリの識別子のバイト単位のサイズ</span><span class="sxs-lookup"><span data-stu-id="fc49c-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="fc49c-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="fc49c-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="fc49c-111">[in]比較する最初のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fc49c-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="fc49c-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="fc49c-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="fc49c-113">[in]_._ _LpEntryID2_パラメーターで指定されたエントリの識別子のバイト単位のサイズ</span><span class="sxs-lookup"><span data-stu-id="fc49c-113">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="fc49c-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="fc49c-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="fc49c-115">[in]比較する 2 番目のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fc49c-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="fc49c-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fc49c-116">_ulFlags_</span></span>
  
> <span data-ttu-id="fc49c-117">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="fc49c-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="fc49c-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="fc49c-118">_lpulResult_</span></span>
  
> <span data-ttu-id="fc49c-119">[out]比較の結果が返されましたへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fc49c-119">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="fc49c-120">2 つのエントリの識別子が同じオブジェクトを参照する場合は TRUE。それ以外の場合、FALSE です。</span><span class="sxs-lookup"><span data-stu-id="fc49c-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fc49c-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="fc49c-121">Return value</span></span>

<span data-ttu-id="fc49c-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc49c-122">S_OK</span></span> 
  
> <span data-ttu-id="fc49c-123">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="fc49c-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc49c-124">����</span><span class="sxs-lookup"><span data-stu-id="fc49c-124">Remarks</span></span>

<span data-ttu-id="fc49c-125">メッセージ ストア プロバイダーは、同じオブジェクトを参照しているかどうかを確認するメッセージ ・ ストア内の指定されたエントリの 2 つのエントリ id を比較する**IMSLogon::CompareEntryIDs**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="fc49c-125">Message store providers implement the **IMSLogon::CompareEntryIDs** method to compare two entry identifiers for a given entry in a message store to determine whether they refer to the same object.</span></span> <span data-ttu-id="fc49c-126">**CompareEntryIDs**が TRUE に_lpulResult_パラメーターを設定する場合は 2 つのエントリの識別子は、同じオブジェクトを参照してください、別のオブジェクトを参照している場合、 **CompareEntryIDs**は false を指定する_lpulResult_を設定します。</span><span class="sxs-lookup"><span data-stu-id="fc49c-126">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets  _lpulResult_ to FALSE.</span></span> 
  
 <span data-ttu-id="fc49c-127">**CompareEntryIDs**は、オブジェクトが 1 つ以上の有効なエントリ id を持つことができますので便利です。</span><span class="sxs-lookup"><span data-stu-id="fc49c-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="fc49c-128">これは、たとえば、メッセージ ストア プロバイダーの新しいバージョンをインストールした後に発生します。</span><span class="sxs-lookup"><span data-stu-id="fc49c-128">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fc49c-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="fc49c-129">See also</span></span>



[<span data-ttu-id="fc49c-130">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fc49c-130">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

