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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 588a32cb2a468c84dfc513af5e4abf6a9a1d0286
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801024"
---
# <a name="imsgserviceadmingetmsgservicetable"></a><span data-ttu-id="9b994-103">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="9b994-103">IMsgServiceAdmin::GetMsgServiceTable</span></span>

  
  
<span data-ttu-id="9b994-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9b994-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9b994-105">メッセージ サービス テーブルで、[プロファイルのメッセージ サービスの一覧へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="9b994-105">Provides access to the message service table, a list of the message services in the profile.</span></span>
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="9b994-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="9b994-106">Parameters</span></span>

 <span data-ttu-id="9b994-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9b994-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9b994-108">[in]常に NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="9b994-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="9b994-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="9b994-109">_lppTable_</span></span>
  
> <span data-ttu-id="9b994-110">[out]メッセージ サービス テーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b994-110">[out] A pointer to a pointer to the message service table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9b994-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="9b994-111">Return value</span></span>

<span data-ttu-id="9b994-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b994-112">S_OK</span></span> 
  
> <span data-ttu-id="9b994-113">メッセージ サービス テーブルは正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="9b994-113">The message service table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9b994-114">備考</span><span class="sxs-lookup"><span data-stu-id="9b994-114">Remarks</span></span>

<span data-ttu-id="9b994-115">**IMsgServiceAdmin::GetMsgServiceTable**メソッドは、メッセージ サービス テーブルで、セッション ・ プロファイルに現在インストールされているメッセージ サービスを一覧表示する MAPI を保持するテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="9b994-115">The **IMsgServiceAdmin::GetMsgServiceTable** method provides access to the message service table, a table that MAPI maintains that lists the message services currently installed in the session profile.</span></span> <span data-ttu-id="9b994-116">メッセージ サービス テーブル内の列の一覧については、[メッセージ サービス テーブル](message-service-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b994-116">For a complete list of columns in the message service table, see [Message Service Table](message-service-tables.md).</span></span>
  
<span data-ttu-id="9b994-117">メッセージ サービス テーブルは静的です。</span><span class="sxs-lookup"><span data-stu-id="9b994-117">The message service table is static.</span></span> <span data-ttu-id="9b994-118">クライアント アクセスが許可されたことを後、それ以降のメッセージ サービスの追加または削除しないに影響します。</span><span class="sxs-lookup"><span data-stu-id="9b994-118">After a client has been given access to it, subsequent message service additions or deletions will not affect it.</span></span> <span data-ttu-id="9b994-119">現在のプロファイルでサービスのメッセージがない場合、 **GetMsgServiceTable**は、0 個の行を持つテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="9b994-119">If there are no message services in the current profile, **GetMsgServiceTable** returns a table with zero rows.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9b994-120">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="9b994-120">MFCMAPI reference</span></span>

<span data-ttu-id="9b994-121">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="9b994-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9b994-122">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="9b994-122">**File**</span></span>|<span data-ttu-id="9b994-123">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="9b994-123">**Function**</span></span>|<span data-ttu-id="9b994-124">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="9b994-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9b994-125">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9b994-125">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="9b994-126">CMsgServiceTableDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="9b994-126">CMsgServiceTableDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="9b994-127">MFCMAPI では、 **IMsgServiceAdmin::GetMsgServiceTable**メソッドを使用して、ビューに表示するプロファイル内のサービスのテーブルをロードします。</span><span class="sxs-lookup"><span data-stu-id="9b994-127">MFCMAPI uses the **IMsgServiceAdmin::GetMsgServiceTable** method to load the table of services in a profile to render in the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b994-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b994-128">See also</span></span>



[<span data-ttu-id="9b994-129">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="9b994-129">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="9b994-130">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="9b994-130">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="9b994-131">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b994-131">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


<span data-ttu-id="9b994-132">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="9b994-132">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

