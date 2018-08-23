---
title: CloseIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CloseIMsgSession
api_type:
- COM
ms.assetid: a0a17309-fc59-4822-be9b-b6f623b68bb1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f358467d72f2a9f395762f529244041a5d9d8d6a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575981"
---
# <a name="closeimsgsession"></a><span data-ttu-id="aa85f-103">CloseIMsgSession</span><span class="sxs-lookup"><span data-stu-id="aa85f-103">CloseIMsgSession</span></span>

  
  
<span data-ttu-id="aa85f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa85f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa85f-105">メッセージ セッションおよびそのセッション内で作成されたすべてのメッセージを閉じます。</span><span class="sxs-lookup"><span data-stu-id="aa85f-105">Closes a message session and all the messages created within that session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aa85f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="aa85f-106">Header file:</span></span>  <br/> |<span data-ttu-id="aa85f-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="aa85f-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="aa85f-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="aa85f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="aa85f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="aa85f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="aa85f-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="aa85f-110">Called by:</span></span>  <br/> |<span data-ttu-id="aa85f-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="aa85f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="aa85f-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="aa85f-112">Parameters</span></span>

 <span data-ttu-id="aa85f-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="aa85f-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="aa85f-114">[in]メッセージ セッションの開始時に[OpenIMsgSession](openimsgsession.md)関数を使用して取得したメッセージのセッション オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="aa85f-114">[in] Pointer to the message session object obtained using the [OpenIMsgSession](openimsgsession.md) function at the start of the message session.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="aa85f-115">Return value</span><span class="sxs-lookup"><span data-stu-id="aa85f-115">Return value</span></span>

<span data-ttu-id="aa85f-116">なし。</span><span class="sxs-lookup"><span data-stu-id="aa85f-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aa85f-117">注釈</span><span class="sxs-lookup"><span data-stu-id="aa85f-117">Remarks</span></span>

<span data-ttu-id="aa85f-118">メッセージ セッションは、クライアント アプリケーションと基になる OLE **IStorage**オブジェクトの上に構築されたいくつかの関連する MAPI **IMessage**オブジェクトを処理するサービス プロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="aa85f-118">A message session is used by client applications and service providers that want to deal with several related MAPI **IMessage** objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="aa85f-119">クライアントまたはプロバイダーは、 [OpenIMsgSession](openimsgsession.md)と**CloseIMsgSession**関数を使用して、メッセージ セッション中には、このようなメッセージの作成をラップします。</span><span class="sxs-lookup"><span data-stu-id="aa85f-119">The client or provider uses the [OpenIMsgSession](openimsgsession.md) and **CloseIMsgSession** functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="aa85f-120">メッセージ セッションを開くと、クライアントまたはプロバイダーのポインターに渡します - **IStorage**オブジェクトの新しい**IMessage**を作成する[OpenIMsgOnIStg](openimsgonistg.md)への呼び出しで。</span><span class="sxs-lookup"><span data-stu-id="aa85f-120">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="aa85f-121">メッセージ セッションは、すべての添付ファイルとメッセージの他のプロパティだけでなく、セッションの期間中に開かれるすべての - 点灯 - **IMessage** **IStorage**オブジェクトの追跡します。</span><span class="sxs-lookup"><span data-stu-id="aa85f-121">A message session keeps track of all **IMessage**-on- **IStorage** objects opened during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="aa85f-122">クライアントまたはプロバイダーを呼び出すと**CloseIMsgSession**、これらすべてのオブジェクトを閉じます。</span><span class="sxs-lookup"><span data-stu-id="aa85f-122">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="aa85f-123">-点灯 - **IStorage**オブジェクト**IMessage**を終了する唯一の方法は、 **CloseIMsgSession**を呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="aa85f-123">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  

