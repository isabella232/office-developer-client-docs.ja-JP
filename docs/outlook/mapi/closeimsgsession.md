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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c190691c8cfcb9b049bcf9ee4f21436e20955def
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799790"
---
# <a name="closeimsgsession"></a><span data-ttu-id="dad82-103">CloseIMsgSession</span><span class="sxs-lookup"><span data-stu-id="dad82-103">CloseIMsgSession</span></span>

  
  
<span data-ttu-id="dad82-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dad82-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dad82-105">メッセージ セッションおよびそのセッション内で作成されたすべてのメッセージを閉じます。</span><span class="sxs-lookup"><span data-stu-id="dad82-105">Closes a message session and all the messages created within that session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dad82-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="dad82-106">Header file:</span></span>  <br/> |<span data-ttu-id="dad82-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="dad82-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="dad82-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="dad82-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dad82-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dad82-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dad82-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="dad82-110">Called by:</span></span>  <br/> |<span data-ttu-id="dad82-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="dad82-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="dad82-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="dad82-112">Parameters</span></span>

 <span data-ttu-id="dad82-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="dad82-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="dad82-114">[in]メッセージ セッションの開始時に[OpenIMsgSession](openimsgsession.md)関数を使用して取得したメッセージのセッション オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="dad82-114">[in] Pointer to the message session object obtained using the [OpenIMsgSession](openimsgsession.md) function at the start of the message session.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dad82-115">Return value</span><span class="sxs-lookup"><span data-stu-id="dad82-115">Return value</span></span>

<span data-ttu-id="dad82-116">なし。</span><span class="sxs-lookup"><span data-stu-id="dad82-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dad82-117">備考</span><span class="sxs-lookup"><span data-stu-id="dad82-117">Remarks</span></span>

<span data-ttu-id="dad82-118">メッセージ セッションは、クライアント アプリケーションと基になる OLE **IStorage**オブジェクトの上に構築されたいくつかの関連する MAPI **IMessage**オブジェクトを処理するサービス プロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="dad82-118">A message session is used by client applications and service providers that want to deal with several related MAPI **IMessage** objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="dad82-119">クライアントまたはプロバイダーは、 [OpenIMsgSession](openimsgsession.md)と**CloseIMsgSession**関数を使用して、メッセージ セッション中には、このようなメッセージの作成をラップします。</span><span class="sxs-lookup"><span data-stu-id="dad82-119">The client or provider uses the [OpenIMsgSession](openimsgsession.md) and **CloseIMsgSession** functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="dad82-120">メッセージ セッションを開くと、クライアントまたはプロバイダーのポインターに渡します - **IStorage**オブジェクトの新しい**IMessage**を作成する[OpenIMsgOnIStg](openimsgonistg.md)への呼び出しで。</span><span class="sxs-lookup"><span data-stu-id="dad82-120">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="dad82-121">メッセージ セッションは、すべての添付ファイルとメッセージの他のプロパティだけでなく、セッションの期間中に開かれるすべての - 点灯 - **IMessage** **IStorage**オブジェクトの追跡します。</span><span class="sxs-lookup"><span data-stu-id="dad82-121">A message session keeps track of all **IMessage**-on- **IStorage** objects opened during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="dad82-122">クライアントまたはプロバイダーを呼び出すと**CloseIMsgSession**、これらすべてのオブジェクトを閉じます。</span><span class="sxs-lookup"><span data-stu-id="dad82-122">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="dad82-123">-点灯 - **IStorage**オブジェクト**IMessage**を終了する唯一の方法は、 **CloseIMsgSession**を呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="dad82-123">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  

