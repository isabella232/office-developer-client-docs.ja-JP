---
title: フォーム サーバー用 IClassFactory インターフェイスの実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ecae23d8631c818fb3d1c6786b2d180e9f32a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800952"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a><span data-ttu-id="27770-103">フォーム サーバー用 IClassFactory インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="27770-103">Implementing the IClassFactory Interface for Form Servers</span></span>

  
  
<span data-ttu-id="27770-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27770-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="27770-105">[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx)は、フォーム サーバーのメッセージ クラスの新しいフォームのオブジェクトを作成するクライアント アプリケーションを使用している OLE インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="27770-105">[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) is the OLE interface that client applications use to create new form objects of your form server's message class.</span></span> <span data-ttu-id="27770-106">必要な**IClassFactory**メソッドを次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="27770-106">The following table lists the **IClassFactory** methods that are required.</span></span> 
  
|<span data-ttu-id="27770-107">**メソッド**</span><span class="sxs-lookup"><span data-stu-id="27770-107">**Method**</span></span>|<span data-ttu-id="27770-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="27770-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27770-109">CreateInstance</span><span class="sxs-lookup"><span data-stu-id="27770-109">CreateInstance</span></span>](http://msdn.microsoft.com/en-us/library/ms682215%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="27770-110">新しいフォーム オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="27770-110">Creates a new form object.</span></span>  <br/> |
|[<span data-ttu-id="27770-111">LockServer</span><span class="sxs-lookup"><span data-stu-id="27770-111">LockServer</span></span>](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="27770-112">複数のフォーム オブジェクトが作成されたときに、起動時のオーバーヘッドを回避できますようにメモリ内でフォームのサーバーをロックします。</span><span class="sxs-lookup"><span data-stu-id="27770-112">Locks the form server in memory so that startup overhead can be avoided when multiple form objects are created.</span></span>  <br/> |
   
<span data-ttu-id="27770-113">についてはすべて、これらのメソッドを実装するために必要な Windows SDK で、COM および ActiveX オブジェクト サービスのセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="27770-113">For all the information necessary to implement these methods, see the COM and ActiveX Object Services section in the Windows SDK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="27770-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="27770-114">See also</span></span>



[<span data-ttu-id="27770-115">フォーム サーバー コードの記述</span><span class="sxs-lookup"><span data-stu-id="27770-115">Writing Form Server Code</span></span>](writing-form-server-code.md)

