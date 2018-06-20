---
title: MSGCALLRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGCALLRELEASE
api_type:
- COM
ms.assetid: 23c08597-41f0-4f48-a63e-79962fa812bc
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: aaa1adaa170349c3df3a2256802a502cb2512b20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801647"
---
# <a name="msgcallrelease"></a><span data-ttu-id="5f7c0-103">MSGCALLRELEASE</span><span class="sxs-lookup"><span data-stu-id="5f7c0-103">MSGCALLRELEASE</span></span>

  
  
<span data-ttu-id="5f7c0-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f7c0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f7c0-105">[OpenIMsgOnIStg](openimsgonistg.md)関数を使用してその上に構築された**IMessage**オブジェクトの最終的なリリース後**IStorage**インターフェイスを解放するコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-105">Defines a callback function that can free an **IStorage** interface after the final release of an **IMessage** object built on top of it with the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5f7c0-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5f7c0-106">Header file:</span></span>  <br/> |<span data-ttu-id="5f7c0-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="5f7c0-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="5f7c0-108">によって実装される関数の定義:</span><span class="sxs-lookup"><span data-stu-id="5f7c0-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="5f7c0-109">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="5f7c0-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="5f7c0-110">によって呼び出される関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="5f7c0-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="5f7c0-111">MAPI</span></span>  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a><span data-ttu-id="5f7c0-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="5f7c0-112">Parameters</span></span>

 <span data-ttu-id="5f7c0-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="5f7c0-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="5f7c0-114">[in]**IMessage**インターフェイスの呼び出し元のアプリケーションの情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-114">[in] Contains calling application information about the **IMessage** interface.</span></span> 
    
 <span data-ttu-id="5f7c0-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="5f7c0-115">_lpMessage_</span></span>
  
> <span data-ttu-id="5f7c0-116">[in]最上位のメッセージおよびリリースされた添付ファイルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-116">[in] Pointer to the top-level message and attachments that have been released.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5f7c0-117">Return value</span><span class="sxs-lookup"><span data-stu-id="5f7c0-117">Return value</span></span>

<span data-ttu-id="5f7c0-118">なし。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-118">None.</span></span>
  

