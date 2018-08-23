---
title: テストとデバッグ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0afceb1f-9086-4cc9-8ce4-fb9256a81a9c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ae9b49717fd7981d653e9852ed02d50bef7c7846
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590688"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="aa384-103">テストとデバッグ</span><span class="sxs-lookup"><span data-stu-id="aa384-103">Testing and Debugging</span></span>

  
  
<span data-ttu-id="aa384-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa384-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa384-105">テスト戦略は、クライアントまたはサービス プロバイダーを開発しているかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="aa384-105">Testing strategies differ depending on whether you are developing a client or service provider.</span></span> <span data-ttu-id="aa384-106">クライアント アプリケーションは、動作する 1 つまたは複数のサービス プロバイダーを必要とするため、さまざまなサービス ・ プロバイダーのセットがある環境でクライアントをテストしてください。</span><span class="sxs-lookup"><span data-stu-id="aa384-106">Because a client application requires one or more service providers to operate, clients should be tested in an environment with different sets of service providers.</span></span>
  
<span data-ttu-id="aa384-107">ただし、サービス ・ プロバイダーの場合は、他のプロバイダーと統合することの前に単独でテストしてください。</span><span class="sxs-lookup"><span data-stu-id="aa384-107">Service providers, however, should be tested in isolation before being integrated with other providers.</span></span> <span data-ttu-id="aa384-108">MAPI には、特定の種類のサービス ・ プロバイダーの機能をテストするツールが用意されています。</span><span class="sxs-lookup"><span data-stu-id="aa384-108">MAPI provides tools that are meant to test the features of a service provider of a particular type.</span></span> <span data-ttu-id="aa384-109">[MFCMAPI](http://go.microsoft.com/fwlink/?LinkId=124154)サンプル アプリケーションは、アドレス帳プロバイダーの機能をテストする方法を示していて、メッセージとの連携がプロバイダーを格納します。</span><span class="sxs-lookup"><span data-stu-id="aa384-109">The [MFCMAPI](http://go.microsoft.com/fwlink/?LinkId=124154) sample application shows how to test the features of an address book provider and works with a message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aa384-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="aa384-110">See also</span></span>



[<span data-ttu-id="aa384-111">MAPI �v���O���~���O�̊T�v</span><span class="sxs-lookup"><span data-stu-id="aa384-111">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
  
<span data-ttu-id="aa384-112">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="aa384-112">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

