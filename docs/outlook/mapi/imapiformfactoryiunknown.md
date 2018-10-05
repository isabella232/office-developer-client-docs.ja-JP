---
title: IMAPIFormFactory IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory
api_type:
- COM
ms.assetid: 637be364-c393-430a-84b3-2c96aa553c22
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c60b542852653bd617b5b9f604bbc44d575e5cb3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384767"
---
# <a name="imapiformfactory--iunknown"></a><span data-ttu-id="ff158-103">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff158-103">IMAPIFormFactory : IUnknown</span></span>

  
  
<span data-ttu-id="ff158-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff158-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff158-105">分散コンピューティング環境では、構成可能な実行時のフォームの使用をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ff158-105">Supports the use of configurable run-time forms in distributed computing environments.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff158-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ff158-106">Header file:</span></span>  <br/> |<span data-ttu-id="ff158-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="ff158-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="ff158-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="ff158-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="ff158-109">ファクトリ オブジェクトのフォーム</span><span class="sxs-lookup"><span data-stu-id="ff158-109">Form factory objects</span></span>  <br/> |
|<span data-ttu-id="ff158-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="ff158-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ff158-111">フォーム サーバー</span><span class="sxs-lookup"><span data-stu-id="ff158-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="ff158-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="ff158-112">Called by:</span></span>  <br/> |<span data-ttu-id="ff158-113">フォームの閲覧者</span><span class="sxs-lookup"><span data-stu-id="ff158-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="ff158-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="ff158-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ff158-115">IID_IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="ff158-115">IID_IMAPIFormFactory</span></span>  <br/> |
|<span data-ttu-id="ff158-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="ff158-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="ff158-117">LPMAPIFORMFACTORY</span><span class="sxs-lookup"><span data-stu-id="ff158-117">LPMAPIFORMFACTORY</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ff158-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="ff158-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ff158-119">CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="ff158-119">CreateClassFactory</span></span>](imapiformfactory-createclassfactory.md) <br/> |<span data-ttu-id="ff158-120">フォームのクラス ファクトリ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="ff158-120">Returns a class factory object for the form.</span></span>  <br/> |
|[<span data-ttu-id="ff158-121">発生しました</span><span class="sxs-lookup"><span data-stu-id="ff158-121">GetLastError</span></span>](imapiformfactory-getlasterror.md) <br/> |<span data-ttu-id="ff158-122">前の工場出荷時のフォーム オブジェクトに発生したエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="ff158-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span>  <br/> |
|[<span data-ttu-id="ff158-123">LockServer</span><span class="sxs-lookup"><span data-stu-id="ff158-123">LockServer</span></span>](imapiformfactory-lockserver.md) <br/> |<span data-ttu-id="ff158-124">開いているフォームのサーバーは、メモリ内に保持します。</span><span class="sxs-lookup"><span data-stu-id="ff158-124">Keeps an open form server in memory.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff158-125">備考</span><span class="sxs-lookup"><span data-stu-id="ff158-125">Remarks</span></span>

<span data-ttu-id="ff158-126">[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx)インターフェイスは、 **IMAPIFormFactory**インターフェイスがベースし、 **IMAPIFormFactory**を実装するオブジェクトは、 **IClassFactory**からも継承する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff158-126">The **IMAPIFormFactory** interface is based on the [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) interface, and objects that implement **IMAPIFormFactory** should also inherit from **IClassFactory**.</span></span>
  
 <span data-ttu-id="ff158-127">**IMAPIFormFactory**は、フォーム サーバーが 1 つ以上のメッセージ クラスをサポートしている場合、新しいフォーム オブジェクトを作成するフォームの閲覧者が使用するインターフェイス (つまり、1 つ以上の入力フォームのオブジェクトの)。</span><span class="sxs-lookup"><span data-stu-id="ff158-127">**IMAPIFormFactory** is the interface that form viewers use to create new form objects when a form server supports more than one message class (that is, more than one type of form object).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ff158-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="ff158-128">See also</span></span>



[<span data-ttu-id="ff158-129">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ff158-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

