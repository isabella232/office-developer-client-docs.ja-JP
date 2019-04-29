---
title: i入力 alsessionfindperson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: userID パラメーターに一致する1人以上の人物を表す文字列を取得します。
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434796"
---
# <a name="isocialsessionfindperson"></a><span data-ttu-id="2a641-103">ISocialSession::FindPerson</span><span class="sxs-lookup"><span data-stu-id="2a641-103">ISocialSession::FindPerson</span></span>

<span data-ttu-id="2a641-104">_userID_パラメーターに一致する1人以上の人物を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2a641-104">Gets a string that represents one or more persons who match the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="2a641-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2a641-105">Parameters</span></span>

<span data-ttu-id="2a641-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="2a641-106">_userId_</span></span>
  
> <span data-ttu-id="2a641-107">順番個人のソーシャルネットワークユーザー ID、SMTP アドレス、または表示名。</span><span class="sxs-lookup"><span data-stu-id="2a641-107">[in] A social network user ID, SMTP address, or display name of a person.</span></span>
    
<span data-ttu-id="2a641-108">_result_</span><span class="sxs-lookup"><span data-stu-id="2a641-108">_result_</span></span>
  
> <span data-ttu-id="2a641-109">読み上げ_userId_パラメーターで指定された id 情報に一致する人物を表す XML 文字列。</span><span class="sxs-lookup"><span data-stu-id="2a641-109">[out] An XML string that represents one or more persons who match the identification information specified by the  _userId_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2a641-110">注釈</span><span class="sxs-lookup"><span data-stu-id="2a641-110">Remarks</span></span>

<span data-ttu-id="2a641-111">1人以上の人物が**findperson**要求に一致した場合、このメソッドは_result_パラメーターでその人物の情報を返します。</span><span class="sxs-lookup"><span data-stu-id="2a641-111">If one or more persons match the **FindPerson** request, this method returns the information for those persons in the  _result_ parameter.</span></span> <span data-ttu-id="2a641-112">_result_ XML 文字列は、Outlook Social Connector (.osc) プロバイダー拡張機能のスキーマで定義されているように、**フレンド**のスキーマ定義に準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a641-112">The  _result_ XML string must comply with the schema definition for **friends**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2a641-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="2a641-113">See also</span></span>

- [<span data-ttu-id="2a641-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2a641-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

