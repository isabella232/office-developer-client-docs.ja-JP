---
title: IPersistMessageGetClassID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetClassID
api_type:
- COM
ms.assetid: 77eeb468-3432-4ccd-9c1e-1df9ce605193
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3f0d98b8ffa13fe238fc0fcf8ff0ec76a3a284eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309626"
---
# <a name="ipersistmessagegetclassid"></a><span data-ttu-id="61cf7-103">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="61cf7-103">IPersistMessage::GetClassID</span></span>

  
  
<span data-ttu-id="61cf7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61cf7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61cf7-105">フォームを管理できるフォーム サーバーを表す識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="61cf7-105">Returns an identifier that represents the form server that can manage the form.</span></span> 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a><span data-ttu-id="61cf7-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="61cf7-106">Parameters</span></span>

 <span data-ttu-id="61cf7-107">_lpClassID_</span><span class="sxs-lookup"><span data-stu-id="61cf7-107">_lpClassID_</span></span>
  
> <span data-ttu-id="61cf7-108">[in, out]フォームのクラス識別子 (CLSID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="61cf7-108">[in, out] A pointer to the class identifier (CLSID) of the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="61cf7-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="61cf7-109">Return value</span></span>

<span data-ttu-id="61cf7-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="61cf7-110">S_OK</span></span> 
  
> <span data-ttu-id="61cf7-111">クラス識別子が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="61cf7-111">The class identifier was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="61cf7-112">注釈</span><span class="sxs-lookup"><span data-stu-id="61cf7-112">Remarks</span></span>

<span data-ttu-id="61cf7-113">**IPersistMessge::GetClassID** メソッドは _、lpClassID_ パラメーターの内容をフォーム サーバーのクラス識別子に設定し、S_OK。</span><span class="sxs-lookup"><span data-stu-id="61cf7-113">The **IPersistMessge::GetClassID** method sets the contents of the  _lpClassID_ parameter to the form server's class identifier and returns S_OK.</span></span> <span data-ttu-id="61cf7-114">フォーム ビューアーが **GetClassID** を呼び出して正常に返されると、フォームは初期化されていない [状態になります](uninitialized-state.md) 。</span><span class="sxs-lookup"><span data-stu-id="61cf7-114">When a form viewer calls **GetClassID** and it returns successfully, the form is placed in the [Uninitialized](uninitialized-state.md) state.</span></span> 
  
<span data-ttu-id="61cf7-115">構造化ストレージ オブジェクトでクラス識別子を使用する方法の詳細については [、IPersist::GetClassID](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) メソッドのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="61cf7-115">For more information about how class identifiers are used with structured storage objects, see the documentation for the [IPersist::GetClassID](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="61cf7-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="61cf7-116">See also</span></span>



[<span data-ttu-id="61cf7-117">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="61cf7-117">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

