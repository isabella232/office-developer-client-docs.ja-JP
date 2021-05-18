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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9ffaab1e9cc381be2abfb389f4b72067dca2438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405913"
---
# <a name="msgcallrelease"></a><span data-ttu-id="2904e-103">MSGCALLRELEASE</span><span class="sxs-lookup"><span data-stu-id="2904e-103">MSGCALLRELEASE</span></span>

  
  
<span data-ttu-id="2904e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2904e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2904e-105">[OpenIMsgOnIStg](openimsgonistg.md)関数を使用して、その上に構築された **IMessage** オブジェクトの最終リリース後に **IStorage** インターフェイスを解放できるコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="2904e-105">Defines a callback function that can free an **IStorage** interface after the final release of an **IMessage** object built on top of it with the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2904e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2904e-106">Header file:</span></span>  <br/> |<span data-ttu-id="2904e-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="2904e-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="2904e-108">定義された関数は、次の方法で実装されます。</span><span class="sxs-lookup"><span data-stu-id="2904e-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="2904e-109">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="2904e-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="2904e-110">によって呼び出される定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="2904e-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="2904e-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="2904e-111">MAPI</span></span>  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a><span data-ttu-id="2904e-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2904e-112">Parameters</span></span>

 <span data-ttu-id="2904e-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="2904e-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="2904e-114">[in]IMessage インターフェイスに関する呼び出し元 **のアプリケーション情報が含** まれる。</span><span class="sxs-lookup"><span data-stu-id="2904e-114">[in] Contains calling application information about the **IMessage** interface.</span></span> 
    
 <span data-ttu-id="2904e-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="2904e-115">_lpMessage_</span></span>
  
> <span data-ttu-id="2904e-116">[in]リリースされたトップ レベルのメッセージと添付ファイルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2904e-116">[in] Pointer to the top-level message and attachments that have been released.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2904e-117">Return value</span><span class="sxs-lookup"><span data-stu-id="2904e-117">Return value</span></span>

<span data-ttu-id="2904e-118">なし。</span><span class="sxs-lookup"><span data-stu-id="2904e-118">None.</span></span>
  

