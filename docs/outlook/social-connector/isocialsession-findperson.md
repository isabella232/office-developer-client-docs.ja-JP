---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: userID パラメーターに一致する 1 人または複数のユーザーを表す文字列を取得します。
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434796"
---
# <a name="isocialsessionfindperson"></a><span data-ttu-id="91d32-103">ISocialSession::FindPerson</span><span class="sxs-lookup"><span data-stu-id="91d32-103">ISocialSession::FindPerson</span></span>

<span data-ttu-id="91d32-104">userID パラメーターに一致する 1 人または複数のユーザーを表す  _文字列を取得_ します。</span><span class="sxs-lookup"><span data-stu-id="91d32-104">Gets a string that represents one or more persons who match the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="91d32-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="91d32-105">Parameters</span></span>

<span data-ttu-id="91d32-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="91d32-106">_userId_</span></span>
  
> <span data-ttu-id="91d32-107">[in]ソーシャル ネットワーク のユーザー ID、SMTP アドレス、またはユーザーの表示名。</span><span class="sxs-lookup"><span data-stu-id="91d32-107">[in] A social network user ID, SMTP address, or display name of a person.</span></span>
    
<span data-ttu-id="91d32-108">_result_</span><span class="sxs-lookup"><span data-stu-id="91d32-108">_result_</span></span>
  
> <span data-ttu-id="91d32-109">[out]  _userId_ パラメーターで指定された識別情報に一致する 1 人または複数のユーザーを表す XML 文字列。</span><span class="sxs-lookup"><span data-stu-id="91d32-109">[out] An XML string that represents one or more persons who match the identification information specified by the  _userId_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="91d32-110">注釈</span><span class="sxs-lookup"><span data-stu-id="91d32-110">Remarks</span></span>

<span data-ttu-id="91d32-111">1 人または複数のユーザーが **FindPerson** 要求と一致する場合、このメソッドは result パラメーター内のそれらのユーザーの情報を  _返_ します。</span><span class="sxs-lookup"><span data-stu-id="91d32-111">If one or more persons match the **FindPerson** request, this method returns the information for those persons in the  _result_ parameter.</span></span> <span data-ttu-id="91d32-112">結果 _の_ XML 文字列は、ソーシャル コネクタ(OSC) プロバイダーの機能拡張のスキーマで定義されているフレンドのスキーマ定義Outlook準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="91d32-112">The  _result_ XML string must comply with the schema definition for **friends**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="91d32-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="91d32-113">See also</span></span>

- [<span data-ttu-id="91d32-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="91d32-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

