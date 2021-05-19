---
title: IAddrBookGetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetPAB
api_type:
- COM
ms.assetid: 9830e09c-700f-469b-a54d-4e4e0583aa84
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6c565c088fd4ef7d5df141bf770c560f79535998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419899"
---
# <a name="iaddrbookgetpab"></a><span data-ttu-id="c9476-103">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="c9476-103">IAddrBook::GetPAB</span></span>

  
  
<span data-ttu-id="c9476-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9476-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9476-105">個人用アドレス帳 (PAB) として指定されているコンテナーのエントリ識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="c9476-105">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="c9476-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c9476-106">Parameters</span></span>

 <span data-ttu-id="c9476-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c9476-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="c9476-108">[out]  _lppEntryID_ パラメーターが指すエントリ識別子内のバイト 数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c9476-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c9476-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="c9476-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="c9476-110">[out]PAB のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c9476-110">[out] A pointer to a pointer to the entry identifier of the PAB.</span></span> <span data-ttu-id="c9476-111">コンテナーが PAB として指定されていない場合  _、lppEntryID_ パラメーターには 0 が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c9476-111">The  _lppEntryID_ parameter contains zero if no container has been designated as the PAB.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c9476-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="c9476-112">Return value</span></span>

<span data-ttu-id="c9476-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9476-113">S_OK</span></span> 
  
> <span data-ttu-id="c9476-114">PAB のエントリ識別子が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="c9476-114">The entry identifier of the PAB was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c9476-115">注釈</span><span class="sxs-lookup"><span data-stu-id="c9476-115">Remarks</span></span>

<span data-ttu-id="c9476-116">クライアントは **GetPAB メソッドを呼** び出して、PAB として指定されたコンテナーのエントリ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="c9476-116">Clients call the **GetPAB** method to retrieve the entry identifier of the container designated as the PAB.</span></span> <span data-ttu-id="c9476-117">PAB がプロファイルに確立されていない場合、MAPI は変更を許可するアドレス帳階層の最初のコンテナーとして PAB として選択します。</span><span class="sxs-lookup"><span data-stu-id="c9476-117">If a PAB has not been established in the profile, MAPI selects as the PAB the first container in the address book hierarchy that allows modifications.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c9476-118">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="c9476-118">MFCMAPI reference</span></span>

<span data-ttu-id="c9476-119">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9476-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c9476-120">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="c9476-120">**File**</span></span>|<span data-ttu-id="c9476-121">**関数**</span><span class="sxs-lookup"><span data-stu-id="c9476-121">**Function**</span></span>|<span data-ttu-id="c9476-122">**コメント**</span><span class="sxs-lookup"><span data-stu-id="c9476-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c9476-123">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c9476-123">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="c9476-124">CMainDlg::OnOpenPAB</span><span class="sxs-lookup"><span data-stu-id="c9476-124">CMainDlg::OnOpenPAB</span></span>  <br/> |<span data-ttu-id="c9476-125">MFCMAPI は **GetPAB** メソッドを使用して、ユーザーの個人用アドレス帳の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="c9476-125">MFCMAPI uses the **GetPAB** method to get the ID for the user's personal address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9476-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="c9476-126">See also</span></span>



[<span data-ttu-id="c9476-127">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="c9476-127">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="c9476-128">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c9476-128">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c9476-129">PidTagContainerFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c9476-129">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="c9476-130">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c9476-130">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="c9476-131">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="c9476-131">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

