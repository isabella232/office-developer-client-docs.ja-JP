---
title: IAddrBookSetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetDefaultDir
api_type:
- COM
ms.assetid: d5d60150-15e4-41ff-bfb0-0c67e2abcacc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ab01f189734ac30b4c027f4e5596c88031b5f99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341700"
---
# <a name="iaddrbooksetdefaultdir"></a><span data-ttu-id="a31c2-103">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="a31c2-103">IAddrBook::SetDefaultDir</span></span>

  
  
<span data-ttu-id="a31c2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a31c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a31c2-105">指定したコンテナーを既定のアドレス帳コンテナーとして確立します。</span><span class="sxs-lookup"><span data-stu-id="a31c2-105">Establishes the specified container as the default address book container.</span></span>
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="a31c2-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a31c2-106">Parameters</span></span>

 <span data-ttu-id="a31c2-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a31c2-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="a31c2-108">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="a31c2-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a31c2-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="a31c2-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="a31c2-110">[in]既定のアドレス帳コンテナーのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a31c2-110">[in] A pointer to the entry identifier of the default address book container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a31c2-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="a31c2-111">Return value</span></span>

<span data-ttu-id="a31c2-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="a31c2-112">S_OK</span></span> 
  
> <span data-ttu-id="a31c2-113">既定のアドレス帳コンテナーが正常に設定されました。</span><span class="sxs-lookup"><span data-stu-id="a31c2-113">The default address book container was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a31c2-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a31c2-114">Remarks</span></span>

<span data-ttu-id="a31c2-115">クライアントとサービス プロバイダーは **、SetDefaultDir** メソッドを呼び出して、新しい既定のアドレス帳コンテナーを確立します。</span><span class="sxs-lookup"><span data-stu-id="a31c2-115">Clients and service providers call the **SetDefaultDir** method to establish a new default address book container.</span></span> <span data-ttu-id="a31c2-116">既定のコンテナーは、ユーザーがアドレス帳を最初に開いたときにアドレス帳に表示されるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="a31c2-116">The default container is the container that the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="a31c2-117">**SetDefaultDir は** 、既定のコンテナーをプロファイルのエントリとして保存します。</span><span class="sxs-lookup"><span data-stu-id="a31c2-117">**SetDefaultDir** saves the default container as an entry in the profile.</span></span> <span data-ttu-id="a31c2-118">**SetDefaultDir** への別の呼び出しが同じセッションまたは別のセッションで行われたか、コンテナーが削除されるまで、コンテナーは既定のままです。</span><span class="sxs-lookup"><span data-stu-id="a31c2-118">The container remains as the default until either another call to **SetDefaultDir** is made in the same session or in another session, or the container is removed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a31c2-119">[[PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY]](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)プロパティは、[アドレス帳のオプション]**ダイアログの**[自動的に選択する] 設定に対応します。</span><span class="sxs-lookup"><span data-stu-id="a31c2-119">The [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="a31c2-120">このプロパティが IID_CAPONE_PROF プロファイル セクションに存在し **、true** に設定されている場合、アドレス帳ダイアログは **SetDefaultDir** で指定されたコンテナーに既定で設定されなくなりましたが、Microsoft [Outlook](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx)がダイアログが表示されたコンテキストに適したアドレス帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="a31c2-120">When this property exists in the [IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by **SetDefaultDir**, but chooses an address book that Microsoft Outlook considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="a31c2-121">これにより、サードパーティのアドレス帳プロバイダーのエクスペリエンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a31c2-121">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a31c2-122">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="a31c2-122">MFCMAPI reference</span></span>

<span data-ttu-id="a31c2-123">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a31c2-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a31c2-124">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="a31c2-124">**File**</span></span>|<span data-ttu-id="a31c2-125">**関数**</span><span class="sxs-lookup"><span data-stu-id="a31c2-125">**Function**</span></span>|<span data-ttu-id="a31c2-126">**コメント**</span><span class="sxs-lookup"><span data-stu-id="a31c2-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a31c2-127">Abcontdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a31c2-127">Abcontdlg.cpp</span></span>  <br/> |<span data-ttu-id="a31c2-128">CAbContDlg::OnSetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="a31c2-128">CAbContDlg::OnSetDefaultDir</span></span>  <br/> |<span data-ttu-id="a31c2-129">MFCMAPI は **SetDefaultDir** メソッドを使用して、指定したアドレス帳コンテナーを既定のアドレス帳コンテナーにします。</span><span class="sxs-lookup"><span data-stu-id="a31c2-129">MFCMAPI uses the **SetDefaultDir** method to make the specified address book container the default one.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a31c2-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="a31c2-130">See also</span></span>



[<span data-ttu-id="a31c2-131">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="a31c2-131">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="a31c2-132">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="a31c2-132">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="a31c2-133">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="a31c2-133">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="a31c2-134">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="a31c2-134">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="a31c2-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a31c2-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="a31c2-136">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="a31c2-136">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

