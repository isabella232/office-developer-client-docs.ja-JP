---
title: テストとデバッグ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0afceb1f-9086-4cc9-8ce4-fb9256a81a9c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8e1f15ae354894aede4e8418e6428d0524ccb70d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316485"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="2d4e7-103">テストとデバッグ</span><span class="sxs-lookup"><span data-stu-id="2d4e7-103">Testing and Debugging</span></span>

  
  
<span data-ttu-id="2d4e7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d4e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d4e7-105">テスト方法は、クライアントまたはサービスプロバイダーを開発しているかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-105">Testing strategies differ depending on whether you are developing a client or service provider.</span></span> <span data-ttu-id="2d4e7-106">クライアントアプリケーションでは、1つ以上のサービスプロバイダーが動作する必要があるため、さまざまなサービスプロバイダーのセットを備えた環境でクライアントをテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-106">Because a client application requires one or more service providers to operate, clients should be tested in an environment with different sets of service providers.</span></span>
  
<span data-ttu-id="2d4e7-107">ただし、サービスプロバイダーは、他のプロバイダーと統合する前に、分離してテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-107">Service providers, however, should be tested in isolation before being integrated with other providers.</span></span> <span data-ttu-id="2d4e7-108">MAPI は、特定の種類のサービスプロバイダーの機能をテストするためのツールを提供します。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-108">MAPI provides tools that are meant to test the features of a service provider of a particular type.</span></span> <span data-ttu-id="2d4e7-109">[mfcmapi](https://go.microsoft.com/fwlink/?LinkId=124154)サンプルアプリケーションは、アドレス帳プロバイダーの機能をテストし、メッセージストアプロバイダーと連携する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-109">The [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154) sample application shows how to test the features of an address book provider and works with a message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2d4e7-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="2d4e7-110">See also</span></span>



[<span data-ttu-id="2d4e7-111">MAPI プログラミングの概要</span><span class="sxs-lookup"><span data-stu-id="2d4e7-111">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
  
<span data-ttu-id="2d4e7-112">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="2d4e7-112">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

