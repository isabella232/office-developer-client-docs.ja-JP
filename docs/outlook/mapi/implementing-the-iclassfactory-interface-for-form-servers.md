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
ms.openlocfilehash: ff8766c6211d9820a2beed1fed871f82089b82fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566783"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a><span data-ttu-id="092c4-103">フォーム サーバー用 IClassFactory インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="092c4-103">Implementing the IClassFactory Interface for Form Servers</span></span>

  
  
<span data-ttu-id="092c4-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="092c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="092c4-105">[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx)は、フォーム サーバーのメッセージ クラスの新しいフォームのオブジェクトを作成するクライアント アプリケーションを使用している OLE インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="092c4-105">[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) is the OLE interface that client applications use to create new form objects of your form server's message class.</span></span> <span data-ttu-id="092c4-106">必要な**IClassFactory**メソッドを次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="092c4-106">The following table lists the **IClassFactory** methods that are required.</span></span> 
  
|<span data-ttu-id="092c4-107">**メソッド**</span><span class="sxs-lookup"><span data-stu-id="092c4-107">**Method**</span></span>|<span data-ttu-id="092c4-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="092c4-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="092c4-109">CreateInstance</span><span class="sxs-lookup"><span data-stu-id="092c4-109">CreateInstance</span></span>](http://msdn.microsoft.com/en-us/library/ms682215%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="092c4-110">新しいフォーム オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="092c4-110">Creates a new form object.</span></span>  <br/> |
|[<span data-ttu-id="092c4-111">LockServer</span><span class="sxs-lookup"><span data-stu-id="092c4-111">LockServer</span></span>](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="092c4-112">複数のフォーム オブジェクトが作成されたときに、起動時のオーバーヘッドを回避できますようにメモリ内でフォームのサーバーをロックします。</span><span class="sxs-lookup"><span data-stu-id="092c4-112">Locks the form server in memory so that startup overhead can be avoided when multiple form objects are created.</span></span>  <br/> |
   
<span data-ttu-id="092c4-113">についてはすべて、これらのメソッドを実装するために必要な Windows SDK で、COM および ActiveX オブジェクト サービスのセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="092c4-113">For all the information necessary to implement these methods, see the COM and ActiveX Object Services section in the Windows SDK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="092c4-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="092c4-114">See also</span></span>



[<span data-ttu-id="092c4-115">フォーム サーバー コードの記述</span><span class="sxs-lookup"><span data-stu-id="092c4-115">Writing Form Server Code</span></span>](writing-form-server-code.md)

