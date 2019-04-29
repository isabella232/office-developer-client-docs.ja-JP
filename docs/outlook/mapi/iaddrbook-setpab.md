---
title: iaddrbooksetpab
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetPAB
api_type:
- COM
ms.assetid: 75daf9d4-6975-435f-91e5-1b41e0047ab7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 29677ce74f405e8ca03f1639f3d98288532e9653
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424617"
---
# <a name="iaddrbooksetpab"></a><span data-ttu-id="f4478-103">IAddrBook::SetPAB</span><span class="sxs-lookup"><span data-stu-id="f4478-103">IAddrBook::SetPAB</span></span>

  
  
<span data-ttu-id="f4478-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4478-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4478-105">特定のコンテナーを個人用アドレス帳 (PAB) として指定します。</span><span class="sxs-lookup"><span data-stu-id="f4478-105">Designates a particular container as the personal address book (PAB).</span></span>
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="f4478-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f4478-106">Parameters</span></span>

 <span data-ttu-id="f4478-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f4478-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="f4478-108">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="f4478-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f4478-109">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="f4478-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="f4478-110">順番PAB として指定するコンテナーのエントリ id へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f4478-110">[in] A pointer to the entry identifier of the container to be designated as the PAB.</span></span> <span data-ttu-id="f4478-111">_lな tryid_パラメーターを NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="f4478-111">The  _lpEntryID_ parameter cannot be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f4478-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="f4478-112">Return value</span></span>

<span data-ttu-id="f4478-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="f4478-113">S_OK</span></span> 
  
> <span data-ttu-id="f4478-114">指定したコンテナーは PAB として確立されています。</span><span class="sxs-lookup"><span data-stu-id="f4478-114">The specified container has been established as the PAB.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f4478-115">注釈</span><span class="sxs-lookup"><span data-stu-id="f4478-115">Remarks</span></span>

<span data-ttu-id="f4478-116">クライアントおよびサービスプロバイダーは、 **setpab**メソッドを呼び出して、特定のコンテナーを PAB として指定します。</span><span class="sxs-lookup"><span data-stu-id="f4478-116">Clients and service providers call the **SetPAB** method to designate a particular container as the PAB.</span></span> <span data-ttu-id="f4478-117">PAB は、他のコンテナーからコピーしたエントリと、新しいエントリで構成されるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="f4478-117">The PAB is a container that consists of entries copied from other containers as well as new entries.</span></span> 
  
<span data-ttu-id="f4478-118">**setpab**の呼び出しによって、コンテナーが pab として設定され、そのコンテナーが使用できなくなるか、またはその後の**setpab**への呼び出しによって新しいコンテナーが pab になります。</span><span class="sxs-lookup"><span data-stu-id="f4478-118">A call to **SetPAB** establishes a container as the PAB until that container is made unavailable or a new container becomes the PAB through a subsequent call to **SetPAB**.</span></span> 
  
<span data-ttu-id="f4478-119">クライアントとプロバイダーは、PAB を永続的に変更するために[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f4478-119">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the PAB change permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f4478-120">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="f4478-120">MFCMAPI reference</span></span>

<span data-ttu-id="f4478-121">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4478-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f4478-122">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="f4478-122">**File**</span></span>|<span data-ttu-id="f4478-123">**関数**</span><span class="sxs-lookup"><span data-stu-id="f4478-123">**Function**</span></span>|<span data-ttu-id="f4478-124">**コメント**</span><span class="sxs-lookup"><span data-stu-id="f4478-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f4478-125">abdlg</span><span class="sxs-lookup"><span data-stu-id="f4478-125">AbContDlg.cpp</span></span>  <br/> |<span data-ttu-id="f4478-126">cabコンテ dlg:: OnSetPAB</span><span class="sxs-lookup"><span data-stu-id="f4478-126">CAbContDlg::OnSetPAB</span></span>  <br/> |<span data-ttu-id="f4478-127">mfcmapi は、 **setpab**メソッドを使用して、指定されたコンテナーを PAB に設定します。</span><span class="sxs-lookup"><span data-stu-id="f4478-127">MFCMAPI uses the **SetPAB** method to make the specified container the PAB.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4478-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="f4478-128">See also</span></span>



[<span data-ttu-id="f4478-129">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="f4478-129">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="f4478-130">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="f4478-130">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="f4478-131">PidTagContainerFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f4478-131">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="f4478-132">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f4478-132">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="f4478-133">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="f4478-133">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

