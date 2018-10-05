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
ms.openlocfilehash: 12d854b72632653d9e1081c9e726c0fe7087bc27
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388050"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a><span data-ttu-id="51c49-103">フォーム サーバー用 IClassFactory インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="51c49-103">Implementing the IClassFactory Interface for Form Servers</span></span>

  
  
<span data-ttu-id="51c49-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51c49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51c49-105">[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx)は、フォーム サーバーのメッセージ クラスの新しいフォームのオブジェクトを作成するクライアント アプリケーションを使用している OLE インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="51c49-105">[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) is the OLE interface that client applications use to create new form objects of your form server's message class.</span></span> <span data-ttu-id="51c49-106">必要な**IClassFactory**メソッドを次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="51c49-106">The following table lists the **IClassFactory** methods that are required.</span></span> 
  
|<span data-ttu-id="51c49-107">**メソッド**</span><span class="sxs-lookup"><span data-stu-id="51c49-107">**Method**</span></span>|<span data-ttu-id="51c49-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="51c49-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="51c49-109">CreateInstance</span><span class="sxs-lookup"><span data-stu-id="51c49-109">CreateInstance</span></span>](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="51c49-110">新しいフォーム オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="51c49-110">Creates a new form object.</span></span>  <br/> |
|[<span data-ttu-id="51c49-111">LockServer</span><span class="sxs-lookup"><span data-stu-id="51c49-111">LockServer</span></span>](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="51c49-112">複数のフォーム オブジェクトが作成されたときに、起動時のオーバーヘッドを回避できますようにメモリ内でフォームのサーバーをロックします。</span><span class="sxs-lookup"><span data-stu-id="51c49-112">Locks the form server in memory so that startup overhead can be avoided when multiple form objects are created.</span></span>  <br/> |
   
<span data-ttu-id="51c49-113">についてはすべて、これらのメソッドを実装するために必要な Windows SDK で、COM および ActiveX オブジェクト サービスのセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="51c49-113">For all the information necessary to implement these methods, see the COM and ActiveX Object Services section in the Windows SDK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="51c49-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="51c49-114">See also</span></span>



[<span data-ttu-id="51c49-115">フォーム サーバー コードの記述</span><span class="sxs-lookup"><span data-stu-id="51c49-115">Writing Form Server Code</span></span>](writing-form-server-code.md)

