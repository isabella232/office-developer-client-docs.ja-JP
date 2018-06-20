---
title: 送信し、名前付きプロパティのコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a5d2244270463fcc2fe0a9786112590e741a8a66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804125"
---
# <a name="transmitting-and-copying-named-properties"></a><span data-ttu-id="d8f27-103">送信し、名前付きプロパティのコピー</span><span class="sxs-lookup"><span data-stu-id="d8f27-103">Transmitting and Copying Named Properties</span></span>

  
  
<span data-ttu-id="d8f27-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d8f27-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d8f27-105">名前付きプロパティが送信されるたびに移動すると、コピー、または、名前は変わりませんが目的のオブジェクトへのマッピングに準拠する識別子を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8f27-105">Whenever a named property is sent, moved, or copied, the name remains constant but the identifier must change to adhere to the mapping of the destination object.</span></span> <span data-ttu-id="d8f27-106">この規則の唯一の例外は、ソースとターゲットのシグネチャを持つ、同じマッピング、ときに再マッピングを不要にすることです。</span><span class="sxs-lookup"><span data-stu-id="d8f27-106">The only exception to this rule is when the source and destination have the same mapping signature, making remapping unnecessary.</span></span>
  
<span data-ttu-id="d8f27-107">ターゲットで動作する適切な識別子を転送の名前付きプロパティの名前を再マップするトランスポート プロバイダーの役割です。</span><span class="sxs-lookup"><span data-stu-id="d8f27-107">It is the responsibility of the transport provider to remap the names of transmitted named properties to appropriate identifiers that work at the destination.</span></span> <span data-ttu-id="d8f27-108">適切なマッピングとは、宛先に送信側のトランスポート プロバイダーを知ることはできません。名前を送信し、動作する識別子にマップするのには受信側のトランスポート プロバイダーに依存して、必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8f27-108">The sending transport provider cannot know what the correct mapping is at the destination; it must transmit the names and rely on the receiving transport provider to map them to identifiers that work.</span></span> <span data-ttu-id="d8f27-109">TNEF の MAPI 実装では、トランスポート プロバイダーの名前付きプロパティの再割り当てを処理します。</span><span class="sxs-lookup"><span data-stu-id="d8f27-109">The MAPI implementation of TNEF handles the remapping of named properties for transport providers.</span></span> <span data-ttu-id="d8f27-110">トランスポート プロバイダー再マッピングを手動で処理か、TNEF の実装を使用します。</span><span class="sxs-lookup"><span data-stu-id="d8f27-110">Transport providers can either handle the remapping manually or use the TNEF implementation.</span></span> 
  
<span data-ttu-id="d8f27-111">これらのプロパティがメッセージ ストア間でコピーされると、名前付きプロパティの再マッピングのような必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8f27-111">A similar remapping of named properties must occur when these properties are copied between message stores.</span></span> <span data-ttu-id="d8f27-112">ただし、メッセージ ストア プロバイダーは、識別子のマッピング先の名前を取得できる、ため、プロパティをすぐに再マップし、メッセージの保存先のストアに依存していませんが。</span><span class="sxs-lookup"><span data-stu-id="d8f27-112">However, because message store providers can retrieve the name to identifier mapping of the destination, they can remap the properties right away and not have to rely on the destination message store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d8f27-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="d8f27-113">See also</span></span>



[<span data-ttu-id="d8f27-114">MAPI ���O�t���v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="d8f27-114">MAPI Named Properties</span></span>](mapi-named-properties.md)

