---
title: iconvertersessionsetadrbook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetAdrBook
api_type:
- COM
ms.assetid: d276ab19-17f4-01c7-4b44-b578e631b5fe
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7645208e6a0256957deb3a71ba3e04ad125a6b61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326895"
---
# <a name="iconvertersessionsetadrbook"></a><span data-ttu-id="4c33c-103">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="4c33c-103">IConverterSession::SetAdrBook</span></span>

  
  
<span data-ttu-id="4c33c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c33c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c33c-105">mapi メッセージを mime ストリームに変換するときに、あいまいなアドレスを解決するために mapi から mime コンバータが使用するオプションの mapi アドレス帳を指定します。</span><span class="sxs-lookup"><span data-stu-id="4c33c-105">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a><span data-ttu-id="4c33c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4c33c-106">Parameters</span></span>

 <span data-ttu-id="4c33c-107">_個人_</span><span class="sxs-lookup"><span data-stu-id="4c33c-107">_pab_</span></span>
  
> <span data-ttu-id="4c33c-108">順番MAPI から MIME への変換で使用される[IAddrBook: imapiprop](iaddrbookimapiprop.md)インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4c33c-108">[in] Pointer to an [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface to be used in the MAPI to MIME conversion.</span></span> <span data-ttu-id="4c33c-109">アドレス帳を必要としなくなった場合は、このパラメーターを**null**に設定します。これにより、インターフェイスが解放され、すべてのアドレス帳を使用しないようにコンバータがリセットされます。</span><span class="sxs-lookup"><span data-stu-id="4c33c-109">Set this parameter to **null** when you no longer need the Address Book; this releases the interface and resets the converter to not using any Address Book.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4c33c-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="4c33c-110">Return value</span></span>

<span data-ttu-id="4c33c-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="4c33c-111">S_OK</span></span>
  
> <span data-ttu-id="4c33c-112">関数呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="4c33c-112">The function call is successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4c33c-113">解説</span><span class="sxs-lookup"><span data-stu-id="4c33c-113">Remarks</span></span>

<span data-ttu-id="4c33c-114">mapi メッセージを MIME ストリームに変換する必要はありません。通常、mapi プロファイルにログオンする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4c33c-114">Converting a MAPI message to MIME stream generally does not require logging on to a MAPI profile.</span></span> <span data-ttu-id="4c33c-115">ただし、変換に MAPI アドレス帳を指定するには、アドレス帳を取得するためにプロファイルにログオンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c33c-115">However, specifying a MAPI Address Book for conversion requires logging on to a profile to obtain the Address Book.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4c33c-116">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="4c33c-116">MFCMAPI reference</span></span>

<span data-ttu-id="4c33c-117">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c33c-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4c33c-118">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="4c33c-118">**File**</span></span>|<span data-ttu-id="4c33c-119">**関数**</span><span class="sxs-lookup"><span data-stu-id="4c33c-119">**Function**</span></span>|<span data-ttu-id="4c33c-120">**コメント**</span><span class="sxs-lookup"><span data-stu-id="4c33c-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4c33c-121">mapimime .cpp</span><span class="sxs-lookup"><span data-stu-id="4c33c-121">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="4c33c-122">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="4c33c-122">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="4c33c-123">mfcmapi は MimeToMAPI を使用して、EML ファイルを MAPI メッセージに変換します。</span><span class="sxs-lookup"><span data-stu-id="4c33c-123">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="4c33c-124">mapimime .cpp</span><span class="sxs-lookup"><span data-stu-id="4c33c-124">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="4c33c-125">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="4c33c-125">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="4c33c-126">mfcmapi は、MAPIToMIMEStm を使用して MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="4c33c-126">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4c33c-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="4c33c-127">See also</span></span>



[<span data-ttu-id="4c33c-128">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4c33c-128">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="4c33c-129">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="4c33c-129">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="4c33c-130">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="4c33c-130">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="4c33c-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="4c33c-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="4c33c-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="4c33c-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="4c33c-133">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="4c33c-133">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="4c33c-134">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="4c33c-134">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

