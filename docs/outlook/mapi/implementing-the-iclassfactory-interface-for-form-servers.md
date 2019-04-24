---
title: フォームサーバー用の IClassFactory インターフェイスの実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 12d854b72632653d9e1081c9e726c0fe7087bc27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310032"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a><span data-ttu-id="84575-103">フォームサーバー用の IClassFactory インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="84575-103">Implementing the IClassFactory Interface for Form Servers</span></span>

  
  
<span data-ttu-id="84575-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84575-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84575-105">[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx)は、クライアントアプリケーションがフォームサーバーのメッセージクラスの新しいフォームオブジェクトを作成するために使用する OLE インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="84575-105">[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) is the OLE interface that client applications use to create new form objects of your form server's message class.</span></span> <span data-ttu-id="84575-106">次の表に、必要な**IClassFactory**メソッドを示します。</span><span class="sxs-lookup"><span data-stu-id="84575-106">The following table lists the **IClassFactory** methods that are required.</span></span> 
  
|<span data-ttu-id="84575-107">**方法**</span><span class="sxs-lookup"><span data-stu-id="84575-107">**Method**</span></span>|<span data-ttu-id="84575-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="84575-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84575-109">CreateInstance</span><span class="sxs-lookup"><span data-stu-id="84575-109">CreateInstance</span></span>](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="84575-110">新しい form オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="84575-110">Creates a new form object.</span></span>  <br/> |
|[<span data-ttu-id="84575-111">lockserver</span><span class="sxs-lookup"><span data-stu-id="84575-111">LockServer</span></span>](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="84575-112">複数のフォームオブジェクトが作成されたときに起動のオーバーヘッドを回避できるように、フォームサーバーをメモリ内にロックします。</span><span class="sxs-lookup"><span data-stu-id="84575-112">Locks the form server in memory so that startup overhead can be avoided when multiple form objects are created.</span></span>  <br/> |
   
<span data-ttu-id="84575-113">これらのメソッドを実装するために必要なすべての情報については、Windows SDK の「COM および ActiveX のオブジェクトサービス」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="84575-113">For all the information necessary to implement these methods, see the COM and ActiveX Object Services section in the Windows SDK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="84575-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="84575-114">See also</span></span>



[<span data-ttu-id="84575-115">フォームサーバーコードの記述</span><span class="sxs-lookup"><span data-stu-id="84575-115">Writing Form Server Code</span></span>](writing-form-server-code.md)

