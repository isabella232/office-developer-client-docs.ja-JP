---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: ユーザー Id パラメーターに一致する 1 つまたは複数の人物を表す文字列を取得します。
ms.openlocfilehash: 0b7525f853f7d97a991e2996a4e715cc53756d4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804360"
---
# <a name="isocialsessionfindperson"></a><span data-ttu-id="47792-103">ISocialSession::FindPerson</span><span class="sxs-lookup"><span data-stu-id="47792-103">ISocialSession::FindPerson</span></span>

<span data-ttu-id="47792-104">_ユーザー Id_パラメーターに一致する 1 つまたは複数の人物を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="47792-104">Gets a string that represents one or more persons who match the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="47792-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="47792-105">Parameters</span></span>

<span data-ttu-id="47792-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="47792-106">_userId_</span></span>
  
> <span data-ttu-id="47792-107">[in]ソーシャル ネットワークのユーザー ID では、SMTP アドレス、またはユーザーの名前を表示します。</span><span class="sxs-lookup"><span data-stu-id="47792-107">[in] A social network user ID, SMTP address, or display name of a person.</span></span>
    
<span data-ttu-id="47792-108">_result_</span><span class="sxs-lookup"><span data-stu-id="47792-108">_result_</span></span>
  
> <span data-ttu-id="47792-109">[out]_ユーザー Id_パラメーターで指定された識別情報に一致する 1 つまたは複数の担当者を表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="47792-109">[out] An XML string that represents one or more persons who match the identification information specified by the  _userId_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="47792-110">注釈</span><span class="sxs-lookup"><span data-stu-id="47792-110">Remarks</span></span>

<span data-ttu-id="47792-111">1 つまたは複数の担当者には、 **FindPerson**要求が一致すると、このメソッドは、_結果_のパラメーターにしている人の情報を返します。</span><span class="sxs-lookup"><span data-stu-id="47792-111">If one or more persons match the **FindPerson** request, this method returns the information for those persons in the  _result_ parameter.</span></span> <span data-ttu-id="47792-112">_結果_の XML 文字列は、Outlook ソーシャル コネクタ (OSC) プロバイダーの機能拡張のスキーマで定義されている**友人**のスキーマ定義に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="47792-112">The  _result_ XML string must comply with the schema definition for **friends**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47792-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="47792-113">See also</span></span>

- [<span data-ttu-id="47792-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47792-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

