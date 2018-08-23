---
title: IAddrBookCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBookCompareEntryIDs
api_type:
- COM
ms.assetid: 7dabc1d3-5ea4-482f-91a9-9ef3009eddd2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 807e592cf535ac060fd275075035ae8beb7d6e78
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800361"
---
# <a name="iaddrbookcompareentryids"></a><span data-ttu-id="2fbde-103">IAddrBook::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="2fbde-103">IAddrBook::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="2fbde-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2fbde-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2fbde-105">同じアドレス帳オブジェクトを参照しているかどうかを判断するのには、特定のアドレス帳プロバイダーに属している 2 つのエントリ id を比較します。</span><span class="sxs-lookup"><span data-stu-id="2fbde-105">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="2fbde-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2fbde-106">Parameters</span></span>

 <span data-ttu-id="2fbde-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="2fbde-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="2fbde-108">[in]_LpEntryID1_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="2fbde-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="2fbde-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="2fbde-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="2fbde-110">[in]比較する最初のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2fbde-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="2fbde-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="2fbde-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="2fbde-112">[in]_LpEntryID2_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="2fbde-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="2fbde-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="2fbde-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="2fbde-114">[in]比較する 2 番目のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2fbde-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="2fbde-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2fbde-115">_ulFlags_</span></span>
  
> <span data-ttu-id="2fbde-116">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="2fbde-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="2fbde-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="2fbde-117">_lpulResult_</span></span>
  
> <span data-ttu-id="2fbde-118">[out]比較の結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2fbde-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="2fbde-119">_LpulResult_の内容が TRUE に設定される場合は 2 つのエントリの識別子が同じオブジェクトを参照してください。それ以外の場合、内容は、FALSE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="2fbde-119">The contents of  _lpulResult_ are set to TRUE if the two entry identifiers refer to the same object; otherwise, the contents are set to FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2fbde-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="2fbde-120">Return value</span></span>

<span data-ttu-id="2fbde-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="2fbde-121">S_OK</span></span> 
  
> <span data-ttu-id="2fbde-122">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="2fbde-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="2fbde-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2fbde-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="2fbde-124">_LpEntryID1_または_lpEntryID2_パラメーターで渡されたエントリ id の一方または両方が、アドレス帳プロバイダーで認識されません。</span><span class="sxs-lookup"><span data-stu-id="2fbde-124">One or both of the entry identifiers passed in with the  _lpEntryID1_ or  _lpEntryID2_ parameters are not recognized by any address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2fbde-125">注釈</span><span class="sxs-lookup"><span data-stu-id="2fbde-125">Remarks</span></span>

<span data-ttu-id="2fbde-126">クライアント アプリケーションとサービス プロバイダーの呼び出し、 **CompareEntryIDs**メソッド 2 つのエントリ id を比較するのには同じオブジェクトを参照しているかどうかを決定する 1 つのアドレス帳プロバイダーに属しています。</span><span class="sxs-lookup"><span data-stu-id="2fbde-126">Client applications and service providers call the **CompareEntryIDs** method to compare two entry identifiers that belongs to a single address book provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="2fbde-127">**CompareEntryIDs**は、オブジェクトが 1 つ以上の有効なエントリ id を持つことができますので便利です。</span><span class="sxs-lookup"><span data-stu-id="2fbde-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="2fbde-128">このような状況には、たとえば、アドレス帳プロバイダーの新しいバージョンをインストールした後が発生します。</span><span class="sxs-lookup"><span data-stu-id="2fbde-128">This situation can occur, for example, after a new version of an address book provider is installed.</span></span> 
  
<span data-ttu-id="2fbde-129">MAPI アドレス帳プロバイダーに、エントリの識別子で登録されている**MAPIUID**構造を持つエントリの識別子の[MAPIUID](mapiuid.md)構造を照合することによって適切なプロバイダーを決定するには、この呼び出しを渡します、プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="2fbde-129">MAPI passes this call to the address book provider that is responsible for the entry identifiers, determining the appropriate provider by matching the [MAPIUID](mapiuid.md) structure in the entry identifiers with the **MAPIUID** structure registered by the provider.</span></span> 
  
<span data-ttu-id="2fbde-130">**CompareEntryIDs**が TRUE に_lpulResult_パラメーターの内容を設定する場合は 2 つのエントリの識別子は、同じオブジェクトを参照してください、別のオブジェクトを参照している場合、 **CompareEntryIDs**は false を指定する内容を設定します。</span><span class="sxs-lookup"><span data-stu-id="2fbde-130">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the contents of the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets the contents to FALSE.</span></span> <span data-ttu-id="2fbde-131">どちらの場合では、 **CompareEntryIDs**は、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="2fbde-131">In either case, **CompareEntryIDs** returns S_OK.</span></span> <span data-ttu-id="2fbde-132">**CompareEntryIDs**エントリの識別子に一致する**MAPIUID**構造体を登録されているアドレス帳プロバイダーがない場合に発生する、エラーを取得する場合は、クライアントとプロバイダーはかかりません操作の結果に基づいて、比較します。</span><span class="sxs-lookup"><span data-stu-id="2fbde-132">If **CompareEntryIDs** returns an error, which can occur if no address book provider has registered a **MAPIUID** structure that matches the one in the entry identifiers, clients and providers should not take any action based on the result of the comparison.</span></span> <span data-ttu-id="2fbde-133">実行中のアクションを最も保守的なアプローチを受講する必要があります代わりにします。</span><span class="sxs-lookup"><span data-stu-id="2fbde-133">They should instead take the most conservative approach to the action being performed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2fbde-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="2fbde-134">See also</span></span>



[<span data-ttu-id="2fbde-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2fbde-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

