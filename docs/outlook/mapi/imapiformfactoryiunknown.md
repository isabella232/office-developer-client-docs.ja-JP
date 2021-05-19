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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c60b542852653bd617b5b9f604bbc44d575e5cb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342120"
---
# <a name="imapiformfactory--iunknown"></a><span data-ttu-id="e632b-103">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e632b-103">IMAPIFormFactory : IUnknown</span></span>

  
  
<span data-ttu-id="e632b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e632b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e632b-105">分散コンピューティング環境での構成可能な実行時フォームの使用をサポートします。</span><span class="sxs-lookup"><span data-stu-id="e632b-105">Supports the use of configurable run-time forms in distributed computing environments.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e632b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e632b-106">Header file:</span></span>  <br/> |<span data-ttu-id="e632b-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="e632b-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="e632b-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="e632b-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="e632b-109">フォーム ファクトリ オブジェクト</span><span class="sxs-lookup"><span data-stu-id="e632b-109">Form factory objects</span></span>  <br/> |
|<span data-ttu-id="e632b-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="e632b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="e632b-111">フォーム サーバー</span><span class="sxs-lookup"><span data-stu-id="e632b-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="e632b-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="e632b-112">Called by:</span></span>  <br/> |<span data-ttu-id="e632b-113">フォーム ビューアー</span><span class="sxs-lookup"><span data-stu-id="e632b-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="e632b-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="e632b-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e632b-115">IID_IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="e632b-115">IID_IMAPIFormFactory</span></span>  <br/> |
|<span data-ttu-id="e632b-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="e632b-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="e632b-117">LPMAPIFORMFACTORY</span><span class="sxs-lookup"><span data-stu-id="e632b-117">LPMAPIFORMFACTORY</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e632b-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="e632b-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e632b-119">CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="e632b-119">CreateClassFactory</span></span>](imapiformfactory-createclassfactory.md) <br/> |<span data-ttu-id="e632b-120">フォームのクラス ファクトリ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="e632b-120">Returns a class factory object for the form.</span></span>  <br/> |
|[<span data-ttu-id="e632b-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="e632b-121">GetLastError</span></span>](imapiformfactory-getlasterror.md) <br/> |<span data-ttu-id="e632b-122">フォーム ファクトリ オブジェクトに発生した以前のエラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="e632b-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span>  <br/> |
|[<span data-ttu-id="e632b-123">LockServer</span><span class="sxs-lookup"><span data-stu-id="e632b-123">LockServer</span></span>](imapiformfactory-lockserver.md) <br/> |<span data-ttu-id="e632b-124">開いているフォーム サーバーをメモリに保持します。</span><span class="sxs-lookup"><span data-stu-id="e632b-124">Keeps an open form server in memory.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e632b-125">注釈</span><span class="sxs-lookup"><span data-stu-id="e632b-125">Remarks</span></span>

<span data-ttu-id="e632b-126">**IMAPIFormFactory** インターフェイスは [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx)インターフェイスに基づいており **、IMAPIFormFactory** を実装するオブジェクトも **IClassFactory から継承する必要があります**。</span><span class="sxs-lookup"><span data-stu-id="e632b-126">The **IMAPIFormFactory** interface is based on the [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) interface, and objects that implement **IMAPIFormFactory** should also inherit from **IClassFactory**.</span></span>
  
 <span data-ttu-id="e632b-127">**IMAPIFormFactory** は、フォーム サーバーが複数のメッセージ クラス (つまり、複数の種類のフォーム オブジェクト) をサポートする場合に、フォーム ビューアーが新しいフォーム オブジェクトを作成するために使用するインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="e632b-127">**IMAPIFormFactory** is the interface that form viewers use to create new form objects when a form server supports more than one message class (that is, more than one type of form object).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e632b-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="e632b-128">See also</span></span>



[<span data-ttu-id="e632b-129">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="e632b-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

