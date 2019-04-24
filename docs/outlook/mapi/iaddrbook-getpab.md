---
title: iaddrbookgetpab
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6c565c088fd4ef7d5df141bf770c560f79535998
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349302"
---
# <a name="iaddrbookgetpab"></a><span data-ttu-id="3547d-103">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="3547d-103">IAddrBook::GetPAB</span></span>

  
  
<span data-ttu-id="3547d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3547d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3547d-105">個人用アドレス帳 (PAB) として指定されているコンテナーのエントリ識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="3547d-105">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="3547d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3547d-106">Parameters</span></span>

 <span data-ttu-id="3547d-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="3547d-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="3547d-108">読み上げ_lppentryid_パラメーターによって指定されたエントリ識別子のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3547d-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="3547d-109">_lppentryid_</span><span class="sxs-lookup"><span data-stu-id="3547d-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="3547d-110">読み上げPAB のエントリ識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3547d-110">[out] A pointer to a pointer to the entry identifier of the PAB.</span></span> <span data-ttu-id="3547d-111">PAB として指定されているコンテナーがない場合、 _lppentryid_パラメーターには0が格納されます。</span><span class="sxs-lookup"><span data-stu-id="3547d-111">The  _lppEntryID_ parameter contains zero if no container has been designated as the PAB.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3547d-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="3547d-112">Return value</span></span>

<span data-ttu-id="3547d-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="3547d-113">S_OK</span></span> 
  
> <span data-ttu-id="3547d-114">PAB のエントリ識別子が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="3547d-114">The entry identifier of the PAB was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3547d-115">解説</span><span class="sxs-lookup"><span data-stu-id="3547d-115">Remarks</span></span>

<span data-ttu-id="3547d-116">クライアントは、 **getpab**メソッドを呼び出して、pab として指定されたコンテナーのエントリ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="3547d-116">Clients call the **GetPAB** method to retrieve the entry identifier of the container designated as the PAB.</span></span> <span data-ttu-id="3547d-117">pab がプロファイルで確立されていない場合、MAPI は、変更を許可するアドレス帳階層の最初のコンテナーを pab として選択します。</span><span class="sxs-lookup"><span data-stu-id="3547d-117">If a PAB has not been established in the profile, MAPI selects as the PAB the first container in the address book hierarchy that allows modifications.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3547d-118">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="3547d-118">MFCMAPI reference</span></span>

<span data-ttu-id="3547d-119">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3547d-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3547d-120">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="3547d-120">**File**</span></span>|<span data-ttu-id="3547d-121">**関数**</span><span class="sxs-lookup"><span data-stu-id="3547d-121">**Function**</span></span>|<span data-ttu-id="3547d-122">**コメント**</span><span class="sxs-lookup"><span data-stu-id="3547d-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3547d-123">maindlg .cpp</span><span class="sxs-lookup"><span data-stu-id="3547d-123">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="3547d-124">CMainDlg:: onopenpab</span><span class="sxs-lookup"><span data-stu-id="3547d-124">CMainDlg::OnOpenPAB</span></span>  <br/> |<span data-ttu-id="3547d-125">mfcmapi は、 **getpab**メソッドを使用して、ユーザーの個人用アドレス帳の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="3547d-125">MFCMAPI uses the **GetPAB** method to get the ID for the user's personal address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3547d-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="3547d-126">See also</span></span>



[<span data-ttu-id="3547d-127">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="3547d-127">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="3547d-128">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3547d-128">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3547d-129">PidTagContainerFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3547d-129">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="3547d-130">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3547d-130">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="3547d-131">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="3547d-131">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

