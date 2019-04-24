---
title: IMsgServiceAdminGetMsgServiceTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetMsgServiceTable
api_type:
- COM
ms.assetid: 064dd5ca-0108-4045-b17b-0bb29cb93346
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fcaebb96d4dca4e6bfbee7491dabeafcbd93a2eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309976"
---
# <a name="imsgserviceadmingetmsgservicetable"></a><span data-ttu-id="8d5bc-103">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="8d5bc-103">IMsgServiceAdmin::GetMsgServiceTable</span></span>

  
  
<span data-ttu-id="8d5bc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d5bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d5bc-105">メッセージサービステーブル (プロファイル内のメッセージサービスのリスト) へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="8d5bc-105">Provides access to the message service table, a list of the message services in the profile.</span></span>
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="8d5bc-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8d5bc-106">Parameters</span></span>

 <span data-ttu-id="8d5bc-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8d5bc-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8d5bc-108">順番常に NULL。</span><span class="sxs-lookup"><span data-stu-id="8d5bc-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="8d5bc-109">_lpptable_</span><span class="sxs-lookup"><span data-stu-id="8d5bc-109">_lppTable_</span></span>
  
> <span data-ttu-id="8d5bc-110">読み上げメッセージサービステーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="8d5bc-110">[out] A pointer to a pointer to the message service table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8d5bc-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="8d5bc-111">Return value</span></span>

<span data-ttu-id="8d5bc-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d5bc-112">S_OK</span></span> 
  
> <span data-ttu-id="8d5bc-113">メッセージサービステーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="8d5bc-113">The message service table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d5bc-114">解説</span><span class="sxs-lookup"><span data-stu-id="8d5bc-114">Remarks</span></span>

<span data-ttu-id="8d5bc-115">**IMsgServiceAdmin:: getmsgservicetable**メソッドは、メッセージサービステーブルへのアクセスを提供します。これは、MAPI が管理するテーブルで、セッションプロファイルに現在インストールされているメッセージサービスを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="8d5bc-115">The **IMsgServiceAdmin::GetMsgServiceTable** method provides access to the message service table, a table that MAPI maintains that lists the message services currently installed in the session profile.</span></span> <span data-ttu-id="8d5bc-116">メッセージサービステーブルの列の完全な一覧については、「 [message service table](message-service-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d5bc-116">For a complete list of columns in the message service table, see [Message Service Table](message-service-tables.md).</span></span>
  
<span data-ttu-id="8d5bc-117">メッセージサービステーブルは静的です。</span><span class="sxs-lookup"><span data-stu-id="8d5bc-117">The message service table is static.</span></span> <span data-ttu-id="8d5bc-118">クライアントがアクセス権を付与されると、それ以降のメッセージサービスの追加または削除によって影響を受けることはありません。</span><span class="sxs-lookup"><span data-stu-id="8d5bc-118">After a client has been given access to it, subsequent message service additions or deletions will not affect it.</span></span> <span data-ttu-id="8d5bc-119">現在のプロファイルにメッセージサービスがない場合、 **getmsgservicetable**は0行のテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="8d5bc-119">If there are no message services in the current profile, **GetMsgServiceTable** returns a table with zero rows.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8d5bc-120">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="8d5bc-120">MFCMAPI reference</span></span>

<span data-ttu-id="8d5bc-121">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d5bc-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8d5bc-122">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="8d5bc-122">**File**</span></span>|<span data-ttu-id="8d5bc-123">**関数**</span><span class="sxs-lookup"><span data-stu-id="8d5bc-123">**Function**</span></span>|<span data-ttu-id="8d5bc-124">**コメント**</span><span class="sxs-lookup"><span data-stu-id="8d5bc-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8d5bc-125">MsgServiceTableDlg</span><span class="sxs-lookup"><span data-stu-id="8d5bc-125">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="8d5bc-126">CMsgServiceTableDlg:: onrefreshview</span><span class="sxs-lookup"><span data-stu-id="8d5bc-126">CMsgServiceTableDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="8d5bc-127">mfcmapi は、 **IMsgServiceAdmin:: getmsgservicetable**メソッドを使用して、ビューに表示するサービスの表をプロファイルに読み込みます。</span><span class="sxs-lookup"><span data-stu-id="8d5bc-127">MFCMAPI uses the **IMsgServiceAdmin::GetMsgServiceTable** method to load the table of services in a profile to render in the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d5bc-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="8d5bc-128">See also</span></span>



[<span data-ttu-id="8d5bc-129">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="8d5bc-129">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="8d5bc-130">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="8d5bc-130">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="8d5bc-131">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8d5bc-131">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


<span data-ttu-id="8d5bc-132">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="8d5bc-132">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

