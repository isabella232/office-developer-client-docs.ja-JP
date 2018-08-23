---
title: メッセージ ストア プロバイダーの構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2f78428b8067b7937e9bd2ee36934cc29a16bfb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804047"
---
# <a name="structure-of-message-store-providers"></a><span data-ttu-id="91bef-103">メッセージ ストア プロバイダーの構造</span><span class="sxs-lookup"><span data-stu-id="91bef-103">Structure of message store providers</span></span>
  
<span data-ttu-id="91bef-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="91bef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="91bef-105">メモリで実行されているとき、メッセージのストア プロバイダーは、 [IMSProvider: IUnknown](imsprovideriunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="91bef-105">A message store provider, when it is running in memory, is an [IMSProvider : IUnknown](imsprovideriunknown.md) interface.</span></span> <span data-ttu-id="91bef-106">**IMSProvider**インタ フェースにより、クライアント アプリケーションと MAPI スプーラーを無効にして、メッセージ ・ ストアからログオンします。</span><span class="sxs-lookup"><span data-stu-id="91bef-106">The **IMSProvider** interface allows client applications and the MAPI spooler to log on to and off of the message store.</span></span> <span data-ttu-id="91bef-107">フォルダーとメッセージ ・ ストア内のメッセージにアクセスするクライアント アプリケーションと MAPI スプーラーを使用しているインタ フェースは、 [IMSLogon](imslogoniunknown.md)と[IMsgStore](imsgstoreimapiprop.md)のインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="91bef-107">The interfaces that client applications and the MAPI spooler use to access folders and messages in the message store are [IMSLogon](imslogoniunknown.md) and [IMsgStore](imsgstoreimapiprop.md) interfaces.</span></span> <span data-ttu-id="91bef-108">これらのインタ フェースは通常、メッセージ ・ ストアが最初にログオンしているときに、作成、メッセージの[MSProviderInit](msproviderinit.md)エントリ ポイントの格納が DLL 可能性がありますも作成します。</span><span class="sxs-lookup"><span data-stu-id="91bef-108">These interfaces are typically created when the message store is first logged on to, although the [MSProviderInit](msproviderinit.md) entry point of the message store DLL could also create them.</span></span> 
  
<span data-ttu-id="91bef-109">**IMSLogon**および**IMsgStore**インターフェイスは、いくつかの方法を共有するため、両方のこれらのインターフェイスから継承する 1 つのクラス オブジェクトを作成するより簡単があります。</span><span class="sxs-lookup"><span data-stu-id="91bef-109">Because the **IMSLogon** and **IMsgStore** interfaces share some methods, it may be easier to create one class object that inherits from both of these interfaces.</span></span> <span data-ttu-id="91bef-110">それぞれ別のオブジェクトでは、これらのインタ フェースを実装し、 **IMSLogon**および**IMsgStore**インタ フェース内のメソッドから呼び出すことができますし、共有メソッドを実装する DLL の内部ヘルパー関数を作成できます。</span><span class="sxs-lookup"><span data-stu-id="91bef-110">You can also implement these interfaces in separate objects, and write helper functions internal to your DLL that implement the shared methods that can then be called from the methods in the **IMSLogon** and **IMsgStore** interfaces.</span></span> 
  
<span data-ttu-id="91bef-111">次の図は、実行中のメッセージ ・ ストア内のオブジェクト階層の上位レベルのアウトラインを示します。</span><span class="sxs-lookup"><span data-stu-id="91bef-111">The following illustration shows a high-level outline of the object hierarchy within a running message store.</span></span>
  
<span data-ttu-id="91bef-112">**メッセージ ストアのオブジェクト階層**</span><span class="sxs-lookup"><span data-stu-id="91bef-112">**Message store object hierarchy**</span></span>
  
<span data-ttu-id="91bef-113">![メッセージ オブジェクトの階層を格納します。](media/storeobj.gif "メッセージ オブジェクトの階層を格納します。")</span><span class="sxs-lookup"><span data-stu-id="91bef-113">![Message store object hierarchy](media/storeobj.gif "Message store object hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="91bef-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="91bef-114">See also</span></span>

- <span data-ttu-id="91bef-115">[MAPI ���b�Z�[�W �X�g�A �v���o�C�_�[�̊J��](developing-a-mapi-message-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="91bef-115">[Developing a MAPI Message Store Provider](developing-a-mapi-message-store-provider.md)</span></span>

