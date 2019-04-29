---
title: IMAPIMessageSiteGetFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFolder
api_type:
- COM
ms.assetid: 9f4b4147-ed98-47cb-a799-ddf028f8e826
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 24461099877af683109c8627eacd22a657d6e156
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430568"
---
# <a name="imapimessagesitegetfolder"></a><span data-ttu-id="b6004-103">IMAPIMessageSite::GetFolder</span><span class="sxs-lookup"><span data-stu-id="b6004-103">IMAPIMessageSite::GetFolder</span></span>

  
  
<span data-ttu-id="b6004-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6004-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6004-105">現在のメッセージが作成または開かれたフォルダー (そのフォルダーが存在する場合) を返します。</span><span class="sxs-lookup"><span data-stu-id="b6004-105">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span> <span data-ttu-id="b6004-106">このメソッドは、埋め込みメッセージの_ppfolder_パラメーターで NULL を返します。これは、フォルダー内に直接格納されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="b6004-106">This method returns NULL in the  _ppFolder_ parameter for embedded messages, which are not stored directly in a folder.</span></span> 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="b6004-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b6004-107">Parameters</span></span>

 <span data-ttu-id="b6004-108">_ppfolder_</span><span class="sxs-lookup"><span data-stu-id="b6004-108">_ppFolder_</span></span>
  
> <span data-ttu-id="b6004-109">読み上げ返されるフォルダーへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b6004-109">[out] A pointer to a pointer to the returned folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b6004-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="b6004-110">Return value</span></span>

<span data-ttu-id="b6004-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="b6004-111">S_OK</span></span> 
  
> <span data-ttu-id="b6004-112">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="b6004-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b6004-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="b6004-113">S_FALSE</span></span> 
  
> <span data-ttu-id="b6004-114">メッセージのフォルダーが存在しません。</span><span class="sxs-lookup"><span data-stu-id="b6004-114">No folder exists for the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b6004-115">注釈</span><span class="sxs-lookup"><span data-stu-id="b6004-115">Remarks</span></span>

<span data-ttu-id="b6004-116">フォームサーバーに関連するインターフェイスの一覧については、「 [MAPI フォームインターフェイス](mapi-form-interfaces.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6004-116">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b6004-117">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="b6004-117">MFCMAPI reference</span></span>

<span data-ttu-id="b6004-118">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6004-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b6004-119">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="b6004-119">**File**</span></span>|<span data-ttu-id="b6004-120">**関数**</span><span class="sxs-lookup"><span data-stu-id="b6004-120">**Function**</span></span>|<span data-ttu-id="b6004-121">**コメント**</span><span class="sxs-lookup"><span data-stu-id="b6004-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b6004-122">MyMAPIFormViewer</span><span class="sxs-lookup"><span data-stu-id="b6004-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="b6004-123">cmymapiformviewer:: getfolder</span><span class="sxs-lookup"><span data-stu-id="b6004-123">CMyMAPIFormViewer::GetFolder</span></span>  <br/> |<span data-ttu-id="b6004-124">mfcmapi は、 **IMAPIMessageSite:: getfolder**メソッドを使用して、現在キャッシュされているポインターを指定のフォルダーに返します。</span><span class="sxs-lookup"><span data-stu-id="b6004-124">MFCMAPI uses the **IMAPIMessageSite::GetFolder** method to return the currently cached pointer to the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6004-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="b6004-125">See also</span></span>



[<span data-ttu-id="b6004-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b6004-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="b6004-127">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="b6004-127">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="b6004-128">MAPI フォームインターフェイス</span><span class="sxs-lookup"><span data-stu-id="b6004-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

