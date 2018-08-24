---
title: IConverterSessionSetAdrBook
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
ms.openlocfilehash: ae00fd0711b8fcae01db6a89da7607d79d8757c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584360"
---
# <a name="iconvertersessionsetadrbook"></a><span data-ttu-id="96b27-103">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="96b27-103">IConverterSession::SetAdrBook</span></span>

  
  
<span data-ttu-id="96b27-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96b27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96b27-105">MAPI メッセージを MIME ストリームに変換するときにあいまいなアドレスを解決するのには MIME コンバーターに MAPI を使用して MAPI アドレス帳を指定します。</span><span class="sxs-lookup"><span data-stu-id="96b27-105">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a><span data-ttu-id="96b27-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="96b27-106">Parameters</span></span>

 <span data-ttu-id="96b27-107">_個人用アドレス帳_</span><span class="sxs-lookup"><span data-stu-id="96b27-107">_pab_</span></span>
  
> <span data-ttu-id="96b27-108">[in]ポインター、 [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) 、MAPI MIME への変換からに使用するインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="96b27-108">[in] Pointer to an [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface to be used in the MAPI to MIME conversion.</span></span> <span data-ttu-id="96b27-109">アドレス帳は必要がなくなったとき、このパラメーターを**null**に設定します。これは、インターフェイスを解放し、コンバーターをリセットし、任意のアドレス帳を使用していません。</span><span class="sxs-lookup"><span data-stu-id="96b27-109">Set this parameter to **null** when you no longer need the Address Book; this releases the interface and resets the converter to not using any Address Book.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="96b27-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="96b27-110">Return value</span></span>

<span data-ttu-id="96b27-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="96b27-111">S_OK</span></span>
  
> <span data-ttu-id="96b27-112">関数の呼び出しが成功します。</span><span class="sxs-lookup"><span data-stu-id="96b27-112">The function call is successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="96b27-113">注釈</span><span class="sxs-lookup"><span data-stu-id="96b27-113">Remarks</span></span>

<span data-ttu-id="96b27-114">MAPI に変換するメッセージを MIME ストリームを一般的には必要ありません MAPI プロファイルにログオンします。</span><span class="sxs-lookup"><span data-stu-id="96b27-114">Converting a MAPI message to MIME stream generally does not require logging on to a MAPI profile.</span></span> <span data-ttu-id="96b27-115">ただし、変換するための MAPI アドレス帳を指定する場合は、アドレス帳を取得するのにはプロファイルにログオンしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="96b27-115">However, specifying a MAPI Address Book for conversion requires logging on to a profile to obtain the Address Book.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="96b27-116">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="96b27-116">MFCMAPI reference</span></span>

<span data-ttu-id="96b27-117">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="96b27-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="96b27-118">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="96b27-118">**File**</span></span>|<span data-ttu-id="96b27-119">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="96b27-119">**Function**</span></span>|<span data-ttu-id="96b27-120">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="96b27-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="96b27-121">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="96b27-121">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="96b27-122">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="96b27-122">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="96b27-123">MFCMAPI では、MimeToMAPI を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="96b27-123">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="96b27-124">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="96b27-124">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="96b27-125">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="96b27-125">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="96b27-126">MFCMAPI では、MAPIToMIMEStm を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="96b27-126">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="96b27-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="96b27-127">See also</span></span>



[<span data-ttu-id="96b27-128">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="96b27-128">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="96b27-129">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="96b27-129">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="96b27-130">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="96b27-130">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="96b27-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="96b27-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="96b27-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="96b27-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="96b27-133">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="96b27-133">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="96b27-134">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="96b27-134">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

